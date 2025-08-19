## `bash:devel`

```console
$ docker pull bash@sha256:dd7cc675731e994b2318bcf32d4da4fe896ce9b860996bfb1a0f64919e4fcf4b
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
$ docker pull bash@sha256:e3042d57b470f0e09f0ce10a5a51663237ad12e74c66d58566ffc943e09a8f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6798460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c03a415c6027e84200b2bc4c0f4f874ff7a8e064c0bb4b624ed1225ad138367`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_COMMIT=3160c0b89ce4f3934e791de94f9370b6cfc26ae5
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_VERSION=devel-20250814
# Tue, 19 Aug 2025 04:18:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7e16eca0bdfccd549e753eed57a8bd9c7b0361ea80aef8a9c894706a5e1c25`  
		Last Modified: Tue, 19 Aug 2025 17:10:40 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3130d9d560c4b60fc68c16c1c25134fc1138818aa792407316d535cbbac9daa`  
		Last Modified: Tue, 19 Aug 2025 17:10:41 GMT  
		Size: 3.0 MB (2997982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4f78257a83d46391e18845c3330eba883b7abd4412054100298346b340ae52`  
		Last Modified: Tue, 19 Aug 2025 17:10:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:247d1b15e4f9b09bc558740f8a355429c45dca99c4ee8177ec3d9659557edbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 KB (136491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473f7b1ef677dc770c63be924a18da6cef11dc3866a179111ce28a84b12367b8`

```dockerfile
```

-	Layers:
	-	`sha256:14103b0fcc137fa6f0d4f67d6a4b22d1db250ae9acd8927c91d52c2478616481`  
		Last Modified: Tue, 19 Aug 2025 18:02:49 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3522bb35765326f63152eced455bd013c93f47506e239fc29f19dcbea97a46ef`  
		Last Modified: Tue, 19 Aug 2025 18:02:50 GMT  
		Size: 18.1 KB (18062 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:a2cbbd81e25b50e45aa624aa23a901690789890bc6893460863a0d84b5c357a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6437751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16a87fc7f7ad364b3b12b62d7bfbd94adeb6e837955d9d4007725eed362c96d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 04:39:00 GMT
ENV _BASH_COMMIT=ff6cfb1464a39b964204a4f83caab2b8484829a6
# Tue, 12 Aug 2025 04:39:00 GMT
ENV _BASH_VERSION=devel-20250808
# Tue, 12 Aug 2025 04:39:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 04:39:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24ffdbb65ab87dd158bd5004e983e7efabb24f8ba37db7ffa1599cf714f638`  
		Last Modified: Tue, 22 Jul 2025 18:03:32 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e31f09e1689752403f8161752da16f7a7f0187d2259b7f846d83ee00b821b7`  
		Last Modified: Tue, 12 Aug 2025 18:24:47 GMT  
		Size: 2.9 MB (2936055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3f17ce7f9197242da8f74425b4e95b35c9924ee2c8474600f2965c6cfc8059`  
		Last Modified: Tue, 12 Aug 2025 18:24:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:88710a365b0f4b4c418e3285ee0cd16b51ef27cfe8fa51bb26b989599b31bf25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (17984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0854203fb297eb7a8324e69a9511cffbbf4ba9cafb649bf1d6c4b7961bc802b`

```dockerfile
```

-	Layers:
	-	`sha256:a7774de805e585b2245be507bfa24221ff7f4fbce3cf8e371374b97f0db01689`  
		Last Modified: Tue, 12 Aug 2025 21:02:56 GMT  
		Size: 18.0 KB (17984 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:054f5a4e67223b6d11502c5134c536d832a3c73667e2acac2936ade24b5b4294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6108057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4870da0d4f1269227cdb8df5e18cb275a713634f370e7af833d658cf1a78b4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 04:39:00 GMT
ENV _BASH_COMMIT=ff6cfb1464a39b964204a4f83caab2b8484829a6
# Tue, 12 Aug 2025 04:39:00 GMT
ENV _BASH_VERSION=devel-20250808
# Tue, 12 Aug 2025 04:39:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 04:39:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae91dfc30adc9b9b9b47e1a22df7eee110ca2b5b6b2b08aff0eb4210851f6d`  
		Last Modified: Tue, 05 Aug 2025 20:59:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0f1471bc17d7919c79abdca45be9cab499160758ebc3946e2c190e28391574`  
		Last Modified: Tue, 12 Aug 2025 18:44:50 GMT  
		Size: 2.9 MB (2888230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df27c1f88c41820b057f47578bc08c07b3b3b22f7c6587fa8a2727e2cee1a3aa`  
		Last Modified: Tue, 12 Aug 2025 18:44:49 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:e39d4db36d4d062a7f9fac5a30c97706bdf87341362fc4124363e34f8f4036f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 KB (136664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c39372ca8ab4fe9c127d344f700bcce92ca20c223a3a957ee5d3c66d9ae8282`

```dockerfile
```

-	Layers:
	-	`sha256:053bbd5d4df42bf615de4df33b338f7dbd0be8695932665ae07c946ccbc3a7f2`  
		Last Modified: Tue, 12 Aug 2025 21:02:59 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5404a6950cc3cedf9ce5e1f7b306c7ef1d72cd763f1d9314cfe673c79fef7d9d`  
		Last Modified: Tue, 12 Aug 2025 21:03:00 GMT  
		Size: 18.2 KB (18199 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:2a93638015587322ae1954f947dfe5e28c759b4c2b4ea33601df26fc76efef73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38327e2d18f82b2b40ed66e3940fb7917bc63fac8acf63a9cdcffc02b08b044a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 04:39:00 GMT
ENV _BASH_COMMIT=ff6cfb1464a39b964204a4f83caab2b8484829a6
# Tue, 12 Aug 2025 04:39:00 GMT
ENV _BASH_VERSION=devel-20250808
# Tue, 12 Aug 2025 04:39:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 04:39:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7043c48c5146969f453ef5c4a8a82a24b8625dd4b6259e162c487a1874f73a89`  
		Last Modified: Tue, 05 Aug 2025 20:59:22 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b21617df8c238b83b9c66e30d193b222c1c3f354b55ef2299c676cd8d45c2`  
		Last Modified: Tue, 12 Aug 2025 22:15:34 GMT  
		Size: 3.1 MB (3087353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3671e0768dfc790e783bf41dea25cda4684ac4e1dc45cd342fa0f514da385c82`  
		Last Modified: Tue, 12 Aug 2025 22:15:40 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:e47649022a2f3db3d9c3eadc9c6029feb11dd6bfefb21c06286e0ac66787a5a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 KB (136711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0c199988441d6d9d6a033ceca073a84af5ee69d522e42e6f8b46b081a27dfe`

```dockerfile
```

-	Layers:
	-	`sha256:2b0a0df94866c59d4f6a477edb71fb2977acd44123c5012456ad351ed2c2e848`  
		Last Modified: Wed, 13 Aug 2025 00:02:48 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d146e514da8b1c9351136bd75eb9e8f2f8303a1c34f8215de6439f1261bb0c6e`  
		Last Modified: Wed, 13 Aug 2025 00:02:49 GMT  
		Size: 18.2 KB (18226 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:2d11a837591cf5be96a12918a6f9568816c10e8644904b6af5b73bc008a55680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6540593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092a35cf3e049ce9757149662e2e7919ca41f2a55ef310ca40901c76c7d53786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_COMMIT=3160c0b89ce4f3934e791de94f9370b6cfc26ae5
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_VERSION=devel-20250814
# Tue, 19 Aug 2025 04:18:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18231143459242c90b1fcbae33e7b63065871453a1307eb1da29a6d31ead3b9e`  
		Last Modified: Tue, 19 Aug 2025 17:10:42 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e12dc8483509fa907582e53408a9798072a3f4721b951adb5bf6a3a8cfd338`  
		Last Modified: Tue, 19 Aug 2025 17:10:43 GMT  
		Size: 2.9 MB (2924798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f7849cb29ad3034818bf099388bc2c2d31da4ced3a5923aec1f03d1235896`  
		Last Modified: Tue, 19 Aug 2025 17:10:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ccf3f5714abef436808b9c2bc5b2e25c9f8892e1f4c3fa7da20bb98d628780ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 KB (136435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cddd335796620ae09979e2eb596952d74bd4cf9b2a90b2e530ef6bafb045043`

```dockerfile
```

-	Layers:
	-	`sha256:d3bb881a3f4a016398f965d34899649c97a8e0555f1f95b42aff55f124f48b22`  
		Last Modified: Tue, 19 Aug 2025 18:02:53 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:901f83f3bbf14084593f0ff91dc07d627367e8ff3d853af0e1041d5628ac2e11`  
		Last Modified: Tue, 19 Aug 2025 18:02:54 GMT  
		Size: 18.0 KB (18031 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:b6fe7a3681d3e389d5827afdd4ff31a6df3031ce51b221457644e5c9570b6227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6999781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b5dd0aa8f33d4ab57739b2f33429f29692573a7064d317469a8e94309c6709`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_COMMIT=3160c0b89ce4f3934e791de94f9370b6cfc26ae5
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_VERSION=devel-20250814
# Tue, 19 Aug 2025 04:18:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ff06a1a69f7247d5e96a6980c0e47c568e805fafbc8fc62a80e2fceeaa7d7a`  
		Last Modified: Tue, 19 Aug 2025 17:10:41 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac2eb4b6b597c5f4b78a43289860442863059dc1cba6dad1f064703f034968a`  
		Last Modified: Tue, 19 Aug 2025 17:10:41 GMT  
		Size: 3.3 MB (3271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8080e740b64625753bc26a06a1c5231b0d7cd039d1c0c515467165a3e9a4e3a4`  
		Last Modified: Tue, 19 Aug 2025 17:10:41 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5dd9607d8778ff4492ea50e1fb1d8ee54dd176fafc6c8659b4813b734391d78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e655407a2dc55980a9245ec459afa986009a59aef9d1cffba578cecbd0834867`

```dockerfile
```

-	Layers:
	-	`sha256:5a1024fa6eceb22781adf12b72d4bc1f4470593e9123191b4b46a0ba8907d19e`  
		Last Modified: Tue, 19 Aug 2025 18:02:57 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6006f556d200de47597fd8616223a66dbb3c64bd896f0ed7babef1647686c621`  
		Last Modified: Tue, 19 Aug 2025 18:02:58 GMT  
		Size: 18.1 KB (18107 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:5383a0fa89075899662c88bf5e24c61ffab842ebaff1d4d22142ac7158ea6531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3239651c5772dbc746858154cc0f5a482f69fd59fc3aa6a32e3c684e9199fb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 04:39:00 GMT
ENV _BASH_COMMIT=ff6cfb1464a39b964204a4f83caab2b8484829a6
# Tue, 12 Aug 2025 04:39:00 GMT
ENV _BASH_VERSION=devel-20250808
# Tue, 12 Aug 2025 04:39:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 04:39:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08916afe3caa2ed348637f41ce6ab48c5deef82e96aa5cb6b35d8eb843812b1`  
		Last Modified: Tue, 22 Jul 2025 18:12:32 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ccefba3126f73f4fb2ac5a856cc8bd9804cbd10916692e4d1ffd540fb3b172`  
		Last Modified: Tue, 12 Aug 2025 20:43:45 GMT  
		Size: 2.9 MB (2947892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eb5e0cd94da1ee4692264a213b1f0630b64a10f238799c5d74f26293655aa2`  
		Last Modified: Tue, 12 Aug 2025 20:43:46 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d8dd1d0f06bd04a2044f57fa73e8eae6a527c1f64dec5e06a3d6a9bf6baf970f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ebf744a564563d5d8cce9c356bf3257bc823d5505c582777c053a17f4a96ca`

```dockerfile
```

-	Layers:
	-	`sha256:cee0e8566550b13dd91964f8ceed696b278cecea85d2bf948521eecad1944998`  
		Last Modified: Wed, 13 Aug 2025 00:02:59 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d3334b2ecc90b29ecc98d347154a3ee4016eae5ea5a8cecfd4d577103c04859`  
		Last Modified: Wed, 13 Aug 2025 00:03:00 GMT  
		Size: 18.2 KB (18167 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:859a36db48f93eaa139b37afc7c7a2a8ff8ddbccd64b46ec9896a74508580945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6737061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d01792221d73afdc4626794c2fa0ed50c456f9d29596a00afc3339ba59e2e36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 12 Aug 2025 04:39:00 GMT
ENV _BASH_COMMIT=ff6cfb1464a39b964204a4f83caab2b8484829a6
# Tue, 12 Aug 2025 04:39:00 GMT
ENV _BASH_VERSION=devel-20250808
# Tue, 12 Aug 2025 04:39:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Aug 2025 04:39:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Aug 2025 04:39:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff48bd6928885910431b6e0489662466b25ea5508cfe8eda7a55614df5a611b0`  
		Last Modified: Tue, 05 Aug 2025 20:59:53 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b8809de9a03983f8d6f31b8a8505358903c1bde05ad9dca9f4ed25bafdd70a`  
		Last Modified: Tue, 12 Aug 2025 18:41:47 GMT  
		Size: 3.1 MB (3091290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80648254db8006551a7fa37f58c579c7106fef72375f29a4d40acdce8e0657cf`  
		Last Modified: Tue, 12 Aug 2025 18:41:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a207a525df18c97efb3e75d5e684530e2ec94eda60880cdca5de4ac7ffce048b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e6304b98c89cb84bfe3fb04d2c09b420299647324fd067f1b8a431ff460343`

```dockerfile
```

-	Layers:
	-	`sha256:8c51613b7c03bdf310af575d1b37b80cdbcb3bf173094e4b5e8f38100f8f8f1b`  
		Last Modified: Tue, 12 Aug 2025 21:03:09 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfb7719d4ba5b1a933e5b45e7a35caf5ddb262d0c41e4431aa8314dd01605145`  
		Last Modified: Tue, 12 Aug 2025 21:03:09 GMT  
		Size: 18.1 KB (18123 bytes)  
		MIME: application/vnd.in-toto+json
