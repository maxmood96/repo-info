## `bash:devel-alpine3.22`

```console
$ docker pull bash@sha256:2582536389697e8aae4e22cd42c12d1618eb0b25111c6ab884c83c57115ba6f5
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

### `bash:devel-alpine3.22` - linux; amd64

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

### `bash:devel-alpine3.22` - unknown; unknown

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

### `bash:devel-alpine3.22` - linux; arm variant v6

```console
$ docker pull bash@sha256:e7102dce4fba0dd49985016b3a80a83b80145e001b6e39c4a24c0c557440d99a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c8d4f941f6d10c2cf89ecbf2740554b6eaab563ae12a3d6e3fce0380fb491`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
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
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24ffdbb65ab87dd158bd5004e983e7efabb24f8ba37db7ffa1599cf714f638`  
		Last Modified: Tue, 22 Jul 2025 18:03:32 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d45e998bbd4c22cc46c35782895b3bb7b132993c048aa8ff063d1f7628e6c8`  
		Last Modified: Tue, 19 Aug 2025 17:24:59 GMT  
		Size: 2.9 MB (2936518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bbe6f9b9f304fbfce55255de12609aa069fda3d9c723088923ea079f16b4b7`  
		Last Modified: Tue, 19 Aug 2025 17:24:59 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:73cf4678f9f23d5d4b15a84f3c681187f5b56dee79e493e0d80dee5bda475d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e9bc1e46ad4f329dabae84c7a7f76473f200b92b1b2c40cdae9d40295012e5`

```dockerfile
```

-	Layers:
	-	`sha256:870a70b2c3ad87c922331e7040ba8e8ae6537baf56ad2052b1439cf3cc3989b9`  
		Last Modified: Tue, 19 Aug 2025 21:02:54 GMT  
		Size: 17.9 KB (17924 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm variant v7

```console
$ docker pull bash@sha256:3ff5bbbfdcbbe4162ab370df46f1e0543874e9414cfabcc580a675eda97bc2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6107986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f4f438b53e3f862fdba4b2fec9b9d789e1bab1a957c6f4b439ac720db7344d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
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
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae91dfc30adc9b9b9b47e1a22df7eee110ca2b5b6b2b08aff0eb4210851f6d`  
		Last Modified: Tue, 05 Aug 2025 20:59:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32dccf2f164f68ad5d7a28f9f8e068b43316e0df02da2da4d7c0b2848e181185`  
		Last Modified: Tue, 19 Aug 2025 17:28:47 GMT  
		Size: 2.9 MB (2888159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56403290fe10e51a959263a314987277f90a661a7aed5bf579046a62ad71c8c`  
		Last Modified: Tue, 19 Aug 2025 17:28:46 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:028d0e2eeb2216d23b8735a761c5ce8b842c56ac4717f4e8bb215fd5985cca9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 KB (136604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbe8bc1841205d890fe30224fd47381a3b37b1e41054a4f5190a33fbb5d50d1`

```dockerfile
```

-	Layers:
	-	`sha256:2708ca86d8146e083d50e8b3dbddf450c0f1fd72c5559400b2004f2603b10c41`  
		Last Modified: Tue, 19 Aug 2025 21:02:57 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:daa07e432ada27ae87ffbeb37a6f87db9d6f8c6a32fb26940726d57abb0b2352`  
		Last Modified: Tue, 19 Aug 2025 21:02:58 GMT  
		Size: 18.1 KB (18139 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:7c9887af88be7c0d0057fbc198a52f91d9cc88005a066334889652b8e36f51d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc5ae9b5d1ccc84f12f266ea043c3b097da7b508a1cfcfea336e9e2a5ffe3d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
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
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f356adcc1e2f7c23bb13d19a6c6dcad633feec39ccf3a1f0c0b94e91c0ac22b6`  
		Last Modified: Tue, 19 Aug 2025 17:25:00 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3022fcfb0ce82418008f3867dca28c0ceff7a246fd479d32b4549a0f76991509`  
		Last Modified: Tue, 19 Aug 2025 17:25:00 GMT  
		Size: 3.1 MB (3086543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0d60f1fe2f5c9ffbf43bba18834481963cb5a9c32183a79c37e4d0f7fc539f`  
		Last Modified: Tue, 19 Aug 2025 17:25:00 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:e8db2f4977aadef2f5e8f11679daf866b095e7252ba320e4911760ee9f71da6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 KB (136652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:681c54b3ddb4cf97859bf6dc3bf727ab51b4e9689ad125d8161527e0bd287221`

```dockerfile
```

-	Layers:
	-	`sha256:8e188222802fc558ff8b98627a5a9ad8a66224555b3a3a24d34541359d77c98f`  
		Last Modified: Tue, 19 Aug 2025 21:03:01 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4210ff3c82016b44fcf7b50140bb706b20a37d477264c53422c898f623e0258c`  
		Last Modified: Tue, 19 Aug 2025 21:03:02 GMT  
		Size: 18.2 KB (18167 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; 386

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

### `bash:devel-alpine3.22` - unknown; unknown

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

### `bash:devel-alpine3.22` - linux; ppc64le

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

### `bash:devel-alpine3.22` - unknown; unknown

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

### `bash:devel-alpine3.22` - linux; riscv64

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

### `bash:devel-alpine3.22` - unknown; unknown

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

### `bash:devel-alpine3.22` - linux; s390x

```console
$ docker pull bash@sha256:e892afbf78f56fa87454805dba0066197f4cf0a2876b453fd54d88c2f2aac156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6736363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b3a695fa12c875e5b3edf76acc159df1956776ee3f1ded3a0c3c3489870cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
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
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b1b190044ded906085aee05c868ec0e93762863e2a98ae5db4bcce2817516d`  
		Last Modified: Tue, 19 Aug 2025 17:32:11 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339a24d4717ec43ae5979eb3eb1a3c9cc8154fa6086275471392ac2d053a6f8d`  
		Last Modified: Tue, 19 Aug 2025 17:32:11 GMT  
		Size: 3.1 MB (3090599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be20a8279bbd116d632a8bc2b85d99661bcc8a2df103ff483c3fe4d01578613`  
		Last Modified: Tue, 19 Aug 2025 17:32:12 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:0e0c1e4f484700befa1ed8d6fe938d2541ba88eefba754883b66899792c0d452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7364d0e342c3a3f4e89c4d900b9343b34a292d99d2326c3d8a1bdcdbc1f15b`

```dockerfile
```

-	Layers:
	-	`sha256:96b7ea4e407ab5a5f6016f259b93902b7fecf25f044ba0fb3fd2923285125958`  
		Last Modified: Tue, 19 Aug 2025 21:03:10 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbaa3db78b21805ed5e444c63048ad9ad87df4a2a7f44e5a6d3d9ab1a6dec266`  
		Last Modified: Tue, 19 Aug 2025 21:03:11 GMT  
		Size: 18.1 KB (18062 bytes)  
		MIME: application/vnd.in-toto+json
