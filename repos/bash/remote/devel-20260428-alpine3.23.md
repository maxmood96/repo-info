## `bash:devel-20260428-alpine3.23`

```console
$ docker pull bash@sha256:3303b8f91427383ce90161efd5219770b5f3e23eb8ed2c01874c81cc4e579db9
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

### `bash:devel-20260428-alpine3.23` - linux; amd64

```console
$ docker pull bash@sha256:8d3ce7c647959d7f1a83ec86dbabed1064626d705521ad55bb9ff5e3a85ea986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6893485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbe79e440838814d962f6f1c59490424ac32ecb856c92b142adbbbc0bb16d58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:07:27 GMT
ENV _BASH_COMMIT=330223688c6be0a7590e33f1b764a64633de52d6
# Tue, 05 May 2026 23:07:27 GMT
ENV _BASH_VERSION=devel-20260428
# Tue, 05 May 2026 23:07:27 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 05 May 2026 23:08:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 May 2026 23:08:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:08:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 23:08:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c3049b8504043c9499e46ddd96fee2d93c48530dea101d8d73f8f8f0664c129`  
		Last Modified: Tue, 05 May 2026 23:08:09 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f498a51a8dae500b1ca86234402ece220ace666273787129fe4a16712eec1cf9`  
		Last Modified: Tue, 05 May 2026 23:08:09 GMT  
		Size: 3.0 MB (3028504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cb551b87b072220c0c60be2b1a9ab90f54d8509c012b62c78209fbd83d43bf`  
		Last Modified: Tue, 05 May 2026 23:08:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260428-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:2a4f7baaf79a1a501ff65276e257c72431d9a904201c887bc70c922b3fc8f988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 KB (135082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e125c66d04524aa26d41902ccdd87af42b170decf6b6d01ddf85fb4f36981`

```dockerfile
```

-	Layers:
	-	`sha256:07a428241bf07ed00d5c5aa2968596124f8d6767891c0a01a80fb40c51b1c8d0`  
		Last Modified: Tue, 05 May 2026 23:08:09 GMT  
		Size: 117.2 KB (117150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e7dbbd6792949a89574114e8e2a58c80bab7058ec771b52f14adcf3c789db3`  
		Last Modified: Tue, 05 May 2026 23:08:09 GMT  
		Size: 17.9 KB (17932 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260428-alpine3.23` - linux; arm variant v6

```console
$ docker pull bash@sha256:700236d6b62271ca1e3f907e0979748585eeb8dd9bad1fc9d51c3bf7cc145269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f78a1e6484e4fdf6c3671a3d75215115edc10605e1906e5aae9e0b192e7a7fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:10:00 GMT
ENV _BASH_COMMIT=330223688c6be0a7590e33f1b764a64633de52d6
# Tue, 05 May 2026 23:10:00 GMT
ENV _BASH_VERSION=devel-20260428
# Tue, 05 May 2026 23:10:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 05 May 2026 23:10:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 May 2026 23:10:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:10:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 23:10:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4ca491d6de85f74b68b7f9864c3444566df9aec179077226da6ea409de439b`  
		Last Modified: Tue, 05 May 2026 23:10:49 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1c60c6bb1fb486fc6d919ebd93210a741f295a154ecc0732c458ca68f59246`  
		Last Modified: Tue, 05 May 2026 23:10:49 GMT  
		Size: 3.0 MB (2987753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93c72d692b5530b9f8f6657aed323bc50c77257c7f58c730813ebe5d9aee31`  
		Last Modified: Tue, 05 May 2026 23:10:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260428-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:9f64c753a5c14c4f4dff90c1dca00205d3829a5f32c2e6aecd8cb149c188e551
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bdfb014fc11a10ba883075d002f826c9e05f98c6cc8a66634a278be483fd62`

```dockerfile
```

-	Layers:
	-	`sha256:adb9da8e1f19ce4d4785800a720638e358db864ddd253f4da8200f8e83a7a4ba`  
		Last Modified: Tue, 05 May 2026 23:10:49 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260428-alpine3.23` - linux; arm variant v7

```console
$ docker pull bash@sha256:bb7671a48eb7d3784133b41e335ba16f1f13f4c73cef0cb5bc1d5fafb9b25069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6221183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf258725734953766c9809f713766e2d659af95bc16b9f434f1a63f9a075a73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:13:18 GMT
ENV _BASH_COMMIT=330223688c6be0a7590e33f1b764a64633de52d6
# Tue, 05 May 2026 23:13:18 GMT
ENV _BASH_VERSION=devel-20260428
# Tue, 05 May 2026 23:13:18 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 05 May 2026 23:14:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 May 2026 23:14:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:14:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 23:14:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385ad7ce6918249b248244f7d2255d8868d7c8cf4da89faa74e2373f3cbcae18`  
		Last Modified: Tue, 05 May 2026 23:14:10 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7011caa58017b6aa0710f0c962b04b0d63d6a77f01cf46abd2a7285d7249e7e1`  
		Last Modified: Tue, 05 May 2026 23:14:10 GMT  
		Size: 2.9 MB (2937272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54afa4f6a41f94d69bc3e3a3f1f3ea2b9f758db66cb5b152747b207c891ea732`  
		Last Modified: Tue, 05 May 2026 23:14:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260428-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:810a871d6ee437854e4b6d2aad77e81997bd90fd4d7327b4f61ff2868b85ecc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cd6657a0475d3b9149d12b39af948044826b46b8a92c4b4f47ecda06ee2df7`

```dockerfile
```

-	Layers:
	-	`sha256:2c132d6e4f9411faaa47ca91c35e28d62e8961b58b10dd6f41be60e414f6ca2b`  
		Last Modified: Tue, 05 May 2026 23:14:10 GMT  
		Size: 116.5 KB (116536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58c0dcfca5e48f9fbc812f0c99894933ce277744a532b87c934d09adbcbb7fdf`  
		Last Modified: Tue, 05 May 2026 23:14:10 GMT  
		Size: 18.0 KB (18012 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260428-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:7cd47dcef1c0242bb61b808d3b790c3532bc741224945647b9183fd9609f4efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7298966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d240b304fc40c6fdb58a83991e7e105445057e7580eef3dcd6a4b106d13a91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:07:32 GMT
ENV _BASH_COMMIT=330223688c6be0a7590e33f1b764a64633de52d6
# Tue, 05 May 2026 23:07:32 GMT
ENV _BASH_VERSION=devel-20260428
# Tue, 05 May 2026 23:07:32 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 05 May 2026 23:08:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 May 2026 23:08:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:08:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 23:08:12 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e3064e9d3d85271880ead3810b1500e1f5f4418af3632830e32f6e8903d66c`  
		Last Modified: Tue, 05 May 2026 23:08:17 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38a79e8883945ac26dc784c2005aa763fa8ccf3096957916be30a8e94ab4242`  
		Last Modified: Tue, 05 May 2026 23:08:17 GMT  
		Size: 3.1 MB (3098302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8e89ff48a8bb3c5fe7104775f362c4929f7967314a69e68389b6d91cc478d2`  
		Last Modified: Tue, 05 May 2026 23:08:17 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260428-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:be83c244d4af93e7af817571d199692612f239dae588d7ada31cf9ee0b782d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceec08fd2a4f3849b618998ab19420f6a903da6b1f0104823bc8da715762836`

```dockerfile
```

-	Layers:
	-	`sha256:3dc80d53b406777a49b82643dc90b2fa1632521ba3f26fe2643c6a3dcd2b313d`  
		Last Modified: Tue, 05 May 2026 23:08:17 GMT  
		Size: 116.6 KB (116556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fa67bd6fcc89eb4474a9d98c48a24b0c0eec81a079726e14e8a07b6d8e9c598`  
		Last Modified: Tue, 05 May 2026 23:08:17 GMT  
		Size: 18.0 KB (18036 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260428-alpine3.23` - linux; 386

```console
$ docker pull bash@sha256:cac10d3788ea3945f1f05010dcd3b2b31158cb481e90c8afe0868b153b2e0b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6647501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9855b51ef03fa5ccff42bc49e715e9c86ceb4266b49c62f7f8149aac015ae77d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:07:02 GMT
ENV _BASH_COMMIT=330223688c6be0a7590e33f1b764a64633de52d6
# Tue, 05 May 2026 23:07:02 GMT
ENV _BASH_VERSION=devel-20260428
# Tue, 05 May 2026 23:07:02 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 05 May 2026 23:07:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 May 2026 23:07:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:07:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 23:07:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b92447c34f7d76a5221051778cd828bfc345bbc964c4113d23e9e116ea5449`  
		Last Modified: Tue, 05 May 2026 23:07:50 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec2e991de3ad954cfe2f3d6b37d7e340673f2dd783375769d9fd3af8c3b693b`  
		Last Modified: Tue, 05 May 2026 23:07:50 GMT  
		Size: 3.0 MB (2956265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc64f285e23a351ad9699353a9211c3dfcf26657ce0085d82b8336f1bb9fc7cb`  
		Last Modified: Tue, 05 May 2026 23:07:50 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260428-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:e46c95a610e17c5f516f8ba293088dafa06c4384f90cfb571a2c9772576b1250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 KB (135025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75cd95c9c8e08b9475f9470f5bd9cd1ad20926eb96dfd35e30377d973fc0446`

```dockerfile
```

-	Layers:
	-	`sha256:497a54c65e78191f1e4474fdc504bdf7b1d02017bd50924922f76c4aaddf7ad1`  
		Last Modified: Tue, 05 May 2026 23:07:50 GMT  
		Size: 117.1 KB (117125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2906e541a3a6df49ba9f2ad95d8c918c786c856e382bef757099c49f2f111a35`  
		Last Modified: Tue, 05 May 2026 23:07:50 GMT  
		Size: 17.9 KB (17900 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260428-alpine3.23` - linux; ppc64le

```console
$ docker pull bash@sha256:8987148ec582a4ce44c74db2569ebbd74fce641eecfb9f68d78aa8389b8ade32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7171121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf747bb86b4da630d79e4de41ef0d8576111d9450ebcd5f8ec4475db6e31a6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:47:02 GMT
ENV _BASH_COMMIT=330223688c6be0a7590e33f1b764a64633de52d6
# Tue, 05 May 2026 23:47:02 GMT
ENV _BASH_VERSION=devel-20260428
# Tue, 05 May 2026 23:47:02 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 05 May 2026 23:48:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 05 May 2026 23:48:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 05 May 2026 23:48:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 May 2026 23:48:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303bb2a1eaccec0904cec201ff93e743d0fa4d6c328e5fc15d78380971af968f`  
		Last Modified: Tue, 05 May 2026 23:48:31 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d646e599ac6ac15dfd1d32c0948f1d5179fc49c0a434b476c7ed793ecc1f435`  
		Last Modified: Tue, 05 May 2026 23:48:32 GMT  
		Size: 3.3 MB (3339397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6075e61a94296ede8508073161fe346971357120204d717b0401ade4dadb9c23`  
		Last Modified: Tue, 05 May 2026 23:48:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260428-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:e33c55a1708ee461b8cd6eae105154d756add0f31d3d4c7e68865ae0252b5833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924aaceb72b4f23110c0f6549f786f8c10e8180f9bb80b457b0c6f261694ea81`

```dockerfile
```

-	Layers:
	-	`sha256:aaac74b6efc2bce4face202dbdd2fdfa7c533c75a027305c9ee80e12ad8c8aaf`  
		Last Modified: Tue, 05 May 2026 23:48:31 GMT  
		Size: 116.5 KB (116533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa922072eda52e1d0d0c6f00702d3971f3d3ecb43720e3a98146be764d59dc53`  
		Last Modified: Tue, 05 May 2026 23:48:31 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260428-alpine3.23` - linux; s390x

```console
$ docker pull bash@sha256:c8d41255ffd51e436d45fb3278f42a57989f8326b825e136168c8cea017c6bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6848631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67efd74ace3c8dcf1275ce33f2daa103dbe77eb71727e34f6325360d0a0fb57a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 00:08:17 GMT
ENV _BASH_COMMIT=330223688c6be0a7590e33f1b764a64633de52d6
# Wed, 06 May 2026 00:08:17 GMT
ENV _BASH_VERSION=devel-20260428
# Wed, 06 May 2026 00:08:17 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 06 May 2026 00:09:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 06 May 2026 00:09:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 May 2026 00:09:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 May 2026 00:09:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7e52f98e6603924d008fa319b6a66740537a7cbf70862506a22cca8a22bae8`  
		Last Modified: Wed, 06 May 2026 00:09:26 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd18226c9f581849bc14f796f5460d7ca1fb8e88b28ce47c28903e8e4fdb653`  
		Last Modified: Wed, 06 May 2026 00:09:26 GMT  
		Size: 3.1 MB (3121308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cc44629195ee38991d8b24cab654ed5905a5a1ead5c7a19c090695bf08f113`  
		Last Modified: Wed, 06 May 2026 00:09:26 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260428-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:69098c961580565295d36f0e31b11dcfdace072f20408493982e87784371a04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 KB (134431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cea47813922fd9d791b4ed41412e7bc60d06e8543d06ee7ad9329140607617`

```dockerfile
```

-	Layers:
	-	`sha256:adc734a42eab1b5e214ba74ba4e99cd875075014975e240be0a308cc448ae97b`  
		Last Modified: Wed, 06 May 2026 00:09:26 GMT  
		Size: 116.5 KB (116499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:932fedd166bc70bafa3aea5f7bcc3ea0ae012a0884390e6cb9b7ee2cfd72a75c`  
		Last Modified: Wed, 06 May 2026 00:09:26 GMT  
		Size: 17.9 KB (17932 bytes)  
		MIME: application/vnd.in-toto+json
