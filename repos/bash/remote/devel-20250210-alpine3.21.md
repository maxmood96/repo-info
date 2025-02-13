## `bash:devel-20250210-alpine3.21`

```console
$ docker pull bash@sha256:8a8896e39449037a68acaf040ee79fe651e7a1e76051ab97c6d7d02a0b1ef355
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

### `bash:devel-20250210-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:2741064802dd4ab528e3a45c31613c0eff3dab5f044fbcf5e047126b00e8827d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6593272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279bd1bc7fbb59b766df9454b84ab35db4712738a0a9d69bb913056ecee8ff44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_COMMIT=3cfc255efe9a05fe8b28cc03a1b6a3fac59741c0
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_VERSION=devel-20250210
# Tue, 11 Feb 2025 05:18:02 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981aec3dda15dbb9454c323609a17993a1e21d751b5126cc4de24a76fb31a52a`  
		Last Modified: Wed, 12 Feb 2025 09:02:05 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2164f12afe15b580ded8918e9b96737a68c736a7c4590cad595133767d58c1d4`  
		Last Modified: Wed, 12 Feb 2025 00:00:30 GMT  
		Size: 3.0 MB (2950760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86290bbdb88fc73adb7b1aa6ff0c6e08b184d2242eca6d2aa731be5027fd7146`  
		Last Modified: Wed, 12 Feb 2025 00:00:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250210-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:bcfa9b8e0bf39cf64325bf2175012180735e74c9bd2a26267595d4e1502e4c44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03905aaeaf52b851d6a5ce9c01393eb432d64b7c30f135468473aa30f2c45f6a`

```dockerfile
```

-	Layers:
	-	`sha256:cc2e0e66c5b0d8b46563a39184efa9a5ccebfc8265ae8471ecd549bb45e3cb5e`  
		Last Modified: Wed, 12 Feb 2025 09:02:03 GMT  
		Size: 114.9 KB (114922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f4bd77abd0d9fa7edee1eb7e466742d52118cbe73d2114e86f7ec165f9d9f92`  
		Last Modified: Wed, 12 Feb 2025 09:02:03 GMT  
		Size: 17.6 KB (17613 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250210-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:1a930b02b5a80a358ba566ec3534945d642fac63045a8a3f4dcb0094f9925c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18afacf2b533ce1ab6bc6351bd88c8fc681b40a9e8f738c2345cf1cdd479bd5f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_COMMIT=3cfc255efe9a05fe8b28cc03a1b6a3fac59741c0
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_VERSION=devel-20250210
# Tue, 11 Feb 2025 05:18:02 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30df67167d1632c1a6da7d7229864f0609dc42113df896a226fec5ace7d08e24`  
		Last Modified: Wed, 15 Jan 2025 07:36:20 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1604efd7c17f6abd0028db6fd17cae32c772a418fa033f1d91b887603370a3c`  
		Last Modified: Wed, 12 Feb 2025 10:05:54 GMT  
		Size: 2.9 MB (2887220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ec4ad37144349e64279dc4e3202d99801928bc2e98c662756b15c78e7b599e`  
		Last Modified: Wed, 12 Feb 2025 09:02:09 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250210-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:c539d98ed63a41c2fe41779dc39245b4e0205fd242cf7f2d0540b9b8a68909da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7c202fc28d253bbb9b2d7fdaf7b51c53b7c7dcd6552d13907f4b7664947821`

```dockerfile
```

-	Layers:
	-	`sha256:7c3282ed57a74aa02cfced4eb9097681c0f159b81ff404c816c07d537738ee5c`  
		Last Modified: Tue, 11 Feb 2025 19:29:44 GMT  
		Size: 17.5 KB (17474 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250210-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:b48d6428ec778653382f49c17ebcb9068f985fc175f534f6ff2b82e030bb818c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5937591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a747d280aec6dae97168760c7e5e07406db857a48640e94c6b356e6d2003d930`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_COMMIT=3cfc255efe9a05fe8b28cc03a1b6a3fac59741c0
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_VERSION=devel-20250210
# Tue, 11 Feb 2025 05:18:02 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3d2fdc30c5f6606f38c2be797bae397d151f4f1ee7e78e1ab4868fb463f4a0`  
		Last Modified: Wed, 15 Jan 2025 07:36:50 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f45c119918b5a3c6174a47a1e88a2802625c5a0e3d4082081bd6fa4a6cc41b0`  
		Last Modified: Wed, 12 Feb 2025 09:02:04 GMT  
		Size: 2.8 MB (2839690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08110bdd00e0eadd6895d624c110c3f5ade3a45c568c971d2b8b3c6842e2977`  
		Last Modified: Wed, 12 Feb 2025 09:02:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250210-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:dc5317960396ecad24eb1bc06d65a5bd921b601c7ae8c4b0d44206e60f343680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bc932344ed55f081add12b400caabf275e75706f0e8bfecd4fdc9fa20b915e`

```dockerfile
```

-	Layers:
	-	`sha256:aabae1b94d12cf6c75056824193be7fbfe81b359475e2514996cc0d33c6cef02`  
		Last Modified: Tue, 11 Feb 2025 19:44:52 GMT  
		Size: 115.0 KB (114958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f5062562865486c5a97b4dd2c93aeee85eebed0a88542b1451b579d6f0fa87`  
		Last Modified: Tue, 11 Feb 2025 19:44:52 GMT  
		Size: 17.7 KB (17689 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250210-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:4b8d1a37547b46752a5d639412cdec82890e4287e8d16458292fbb3112258f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7029367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8755fb5a27bdebc760781160a8ef99aee3c3c6e50f77141d61c0f9e40fe56495`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_COMMIT=3cfc255efe9a05fe8b28cc03a1b6a3fac59741c0
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_VERSION=devel-20250210
# Tue, 11 Feb 2025 05:18:02 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa48446e68d46a51c43513cd51c946dadb78e43915902fa802a2599d86ee148`  
		Last Modified: Wed, 05 Feb 2025 03:39:52 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a63878c2fe43e99c7d6d5438c70e11a1cd865b6d77ccd184d8ed5fd6ec3e6ac`  
		Last Modified: Wed, 12 Feb 2025 09:02:05 GMT  
		Size: 3.0 MB (3036218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e004366656ad683b743112aa189836e55f4d34486fffb716c1038287e795a48`  
		Last Modified: Tue, 11 Feb 2025 22:32:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250210-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:d663db2429fa5fb0a45dda341fce454615548d877acb4aa484814d0c80c5a531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f511112b933b03eca54fc234936e7f9dedd4879dd66428deead62d7507e4de23`

```dockerfile
```

-	Layers:
	-	`sha256:0482323da79a82fc5b2cbaad3df8a6186c2b88aeae7304b41f99f4e177c81d86`  
		Last Modified: Tue, 11 Feb 2025 19:29:33 GMT  
		Size: 115.0 KB (114978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6af658ea60ba2cbbd966ab451c7882da714ad4bda40e95d52ca0128593816336`  
		Last Modified: Tue, 11 Feb 2025 19:29:33 GMT  
		Size: 17.7 KB (17717 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250210-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:dc993306390a159697fa7f70a6e3f8dfe69aa11db3ce6ac8d05f9514a6332f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6342328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b36e8a38864ca3f32c3bb461a768a6aac567a6ceb80c2b50935f9b50912ee2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_COMMIT=3cfc255efe9a05fe8b28cc03a1b6a3fac59741c0
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_VERSION=devel-20250210
# Tue, 11 Feb 2025 05:18:02 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0bf9a1b247219fafa83b2812485b9a48d63a9873c3f217bba902b868dfe189`  
		Last Modified: Tue, 11 Feb 2025 19:30:04 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c55bd1308da84884e71de56003718fa304084912216279684fc9c1e515e15f`  
		Last Modified: Tue, 11 Feb 2025 22:32:50 GMT  
		Size: 2.9 MB (2878410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1d06e30216fe9dc17ef59c556e50889b3dba5ef88d19e97b7d0a4ee2fdd405`  
		Last Modified: Tue, 11 Feb 2025 22:32:49 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250210-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:644db867dd9a4cdb321b4cfb7ea0ea821b347ef715152673fa3adc4ca5f76c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e48f1013e51d37f7c9aeec5c8d00ce740aff231c955e09a6a1bd064723a5b4`

```dockerfile
```

-	Layers:
	-	`sha256:cfb7557cbb7f84b35ba5a7eab4785a712b8707f0acf474130a59efc80f0dc8c9`  
		Last Modified: Tue, 11 Feb 2025 19:30:04 GMT  
		Size: 114.9 KB (114897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02e1ab80e6de3aeb1acfe6aacfb7bdbf2df4457aa2e3a6d872375c77834a07a2`  
		Last Modified: Tue, 11 Feb 2025 19:30:04 GMT  
		Size: 17.6 KB (17581 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250210-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:4ed33cc259bdb05c3ffc93183fe861eceaa75d984011e4464d0b538f4e4b8c3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6795293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:363802adf1f8883f31a2c08020ef2d99e0d8034a428ca8ae8abc1069595a5ede`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_COMMIT=3cfc255efe9a05fe8b28cc03a1b6a3fac59741c0
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_VERSION=devel-20250210
# Tue, 11 Feb 2025 05:18:02 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dfc46915d71ccb9f5cc24acd8a414354e3b2924934682b77fd72a0764b864e`  
		Last Modified: Wed, 12 Feb 2025 09:02:09 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b916dafa874021256b94a74a2c7565909b13abff77d2d0f258494e3bbd541e`  
		Last Modified: Wed, 12 Feb 2025 10:06:02 GMT  
		Size: 3.2 MB (3220899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a34dc18840cd20e03b7105871515954d2b50561b05d06ec0a7dff63636bd7c`  
		Last Modified: Wed, 12 Feb 2025 10:05:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250210-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:2e07b848ad74e6c6a59f0b39e24f90f625589ba692832aa07d5d7ac73c3dd2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1240393a4eaff00f1c864c803978557b7070c59baf1caf81f503582aa291ff08`

```dockerfile
```

-	Layers:
	-	`sha256:ac775baedb125f54b1e262cad133b688d7815807faf694390296fc5169f6c7c4`  
		Last Modified: Wed, 12 Feb 2025 09:02:04 GMT  
		Size: 113.0 KB (113005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d5ed46056e8e03125c64d90e7ff7bc72a829ba472126b636e49d5858145c2e5`  
		Last Modified: Tue, 11 Feb 2025 19:29:41 GMT  
		Size: 17.7 KB (17657 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250210-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:6e50d15fb7985fdc6e54d4a0c2b99829c279b7bc0012e86eca3c02309056bd6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6252709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31193e868054de6211d3419c3eea6a3daf6c5bfb3cc0a70f466aed728075882a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_COMMIT=3cfc255efe9a05fe8b28cc03a1b6a3fac59741c0
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_VERSION=devel-20250210
# Tue, 11 Feb 2025 05:18:02 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee5ec45bdf477db840352ec8979a5377f81b57c5bd134c10ef0dd422448e2c3`  
		Last Modified: Wed, 15 Jan 2025 07:39:56 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b015c15645b940e4db22335f14308dbcc03e5ebe16ed9584581a6d1c152205`  
		Last Modified: Wed, 12 Feb 2025 09:02:05 GMT  
		Size: 2.9 MB (2901654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772e2efc8c11e85d49ff6f2cbda77346dc7b6350d449c84a9a0ae0e82629d6e0`  
		Last Modified: Wed, 12 Feb 2025 09:02:05 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250210-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:ac62c8aa9e850d38175f770618009d8d13a6da5ecb7e9f0e7dfe9d6b0482cf14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3de56fdcad58bec27799c3ff1b6d4b2abd67c2a3e67edb2b911ad699fb47c07`

```dockerfile
```

-	Layers:
	-	`sha256:1414fa505d0a7ec3a414c7b69d4a3753eccf9927fb1ea9ebddf49a052433b7c0`  
		Last Modified: Wed, 12 Feb 2025 09:02:05 GMT  
		Size: 113.0 KB (113001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0d6c247d890a7964435eb406e6f5b5657fe9c495db31e603d5c5fcde329bb6`  
		Last Modified: Tue, 11 Feb 2025 19:38:06 GMT  
		Size: 17.7 KB (17657 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250210-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:4d0238cb2186ad876995d31292ed687328b18ed0c7f99d01595db3e9dc179317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6514294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2a0e99caccd570cafc94cff7e4b1421c89fe57341db80cf96c9f57f35b4bc1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_COMMIT=3cfc255efe9a05fe8b28cc03a1b6a3fac59741c0
# Tue, 11 Feb 2025 05:18:02 GMT
ENV _BASH_VERSION=devel-20250210
# Tue, 11 Feb 2025 05:18:02 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 05:18:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 05:18:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af395138899cbb5ed17e042be43e4dc4170d1061fd99f18f88ae0030c6e620e1`  
		Last Modified: Wed, 12 Feb 2025 10:05:55 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4491a0e1c3a4e6f842846e29f79537371c78ef1e79559305cf77b2ee739d757`  
		Last Modified: Wed, 12 Feb 2025 09:02:06 GMT  
		Size: 3.0 MB (3046634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25595cd83e20a84640e6ac5f1817dac49c2690667834685dfd64864761349174`  
		Last Modified: Wed, 12 Feb 2025 10:05:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250210-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:e618b17315bc5f1fddd62d658e03409816bdae94410027c6949d204657564665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 KB (130584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5309b628d99229fbd200954c177bcb9323694e7cdc9b530e15bdf243a930a5d9`

```dockerfile
```

-	Layers:
	-	`sha256:8dc04c395090ea997f425a44a3e559a77783174667f38e9b0b48204081abb957`  
		Last Modified: Wed, 12 Feb 2025 09:02:05 GMT  
		Size: 113.0 KB (112971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f442ce8b7469cacee33b13b6de4a56452d810450c68e806251e7c14cf76aa5c`  
		Last Modified: Wed, 12 Feb 2025 09:02:06 GMT  
		Size: 17.6 KB (17613 bytes)  
		MIME: application/vnd.in-toto+json
