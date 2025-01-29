## `bash:devel-alpine3.21`

```console
$ docker pull bash@sha256:cd7c58f70320c898bc44fd9155b8b04fca38ad0fc36482852a50f2b20de942a8
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

### `bash:devel-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:be671301b770f05a954c3cade9d7455a2cc5f323920bf527ec5c40e08e214e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6592577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ac3de0a2b52ceaa61025b0000eb0d44a1c0d39c16619607e30b69b8f41753d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_COMMIT=25e213a551dc808c7f29360075bad4806fb9fec5
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_VERSION=devel-20250124
# Tue, 28 Jan 2025 07:24:49 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d782fd46c5d157e903b9fef82d2484a7b72ea9577ead3341f0d5a7eb6df223e`  
		Last Modified: Tue, 28 Jan 2025 23:28:42 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed731daced2d54be1409c5acd77ca1e185bcda8b41f112421a21e293b3c008fb`  
		Last Modified: Tue, 28 Jan 2025 23:28:43 GMT  
		Size: 3.0 MB (2950071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ae88d42ca1fb4cbf0bb540214d7d6379818acb436ff7115b950fb93f06be37`  
		Last Modified: Tue, 28 Jan 2025 23:28:42 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:fcef8b86e7e73675b46257752000e22ac2bfc4990b4e2fe347b3d9b00fd9b357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98168aacede3f0d28dddf2822b57dad89586ab0b9b449b37ba39bf307a0488be`

```dockerfile
```

-	Layers:
	-	`sha256:c920257c5191efabdfe1e8d1e1e06f87ce388ef50d0631e37c080da028721bcf`  
		Last Modified: Tue, 28 Jan 2025 23:28:42 GMT  
		Size: 114.9 KB (114922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8912132543e1470b02a28e03e8aeaeae6f746d34b4d5b88166cca5f2790b38b7`  
		Last Modified: Tue, 28 Jan 2025 23:28:42 GMT  
		Size: 17.8 KB (17841 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:cc77610bb23643c79c06b25b68a19958fdd3b4384c35c809bb814a3d5dc9a933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410ac6da432a4180954efc6e1480220c33f0c744198fbc1319984d2f03de2cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_COMMIT=25e213a551dc808c7f29360075bad4806fb9fec5
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_VERSION=devel-20250124
# Tue, 28 Jan 2025 07:24:49 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30df67167d1632c1a6da7d7229864f0609dc42113df896a226fec5ace7d08e24`  
		Last Modified: Wed, 08 Jan 2025 18:07:26 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc927ecd1d909d48c6f0ee52926cca7bb7d9bba296c0b90c1a7cc8bad351c9b`  
		Last Modified: Tue, 28 Jan 2025 23:28:31 GMT  
		Size: 2.9 MB (2887046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3d5c6ab3d1fe87b8f4aaafdbf79b916f606393bf776b54291319baeee9c263`  
		Last Modified: Tue, 28 Jan 2025 23:28:30 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:093b948feeeb90808ba33828b921fc827b9a101a1bfe3a434e2aef4314f66f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 KB (17701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a24173b24860df9c07282d4038ca6ce883cd68c1bafffd05c2123e9c7099af`

```dockerfile
```

-	Layers:
	-	`sha256:acb16271dacef79876820afa76d086f1680f6d6250a4f4d796a3bf84343eee0f`  
		Last Modified: Tue, 28 Jan 2025 23:28:30 GMT  
		Size: 17.7 KB (17701 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:88b3f6e8d441e7843e539220ac817d3aec7278450a4337fb4e742e31e8d88ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5936945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27de583b51a124410ca2c4fe7064a97c86baac7ba5f2526c2fae8f2d15318c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_COMMIT=25e213a551dc808c7f29360075bad4806fb9fec5
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_VERSION=devel-20250124
# Tue, 28 Jan 2025 07:24:49 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3d2fdc30c5f6606f38c2be797bae397d151f4f1ee7e78e1ab4868fb463f4a0`  
		Last Modified: Wed, 08 Jan 2025 18:23:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c4bd71c0ebf8b5ca3a5b7f8139522bf39de09f52e529f70247e9b6378320d7`  
		Last Modified: Tue, 28 Jan 2025 23:28:21 GMT  
		Size: 2.8 MB (2839039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6487a4462dcfeff6862b0285c8a3b5ba69d486657129c93de90c0688688dfafb`  
		Last Modified: Tue, 28 Jan 2025 23:28:21 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:968afb73e956e4be375ab14746c8cac85d689ffd5820f67a9955a00ec6c150a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 KB (132875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f8d1ec33c88de95df4dafc118b70a1c42df262ba37ef09cbdce034091549df`

```dockerfile
```

-	Layers:
	-	`sha256:e313845cc3ef7e1250f35411e91ac0f2c3bd21870a9b416761161c0177a61866`  
		Last Modified: Tue, 28 Jan 2025 23:28:21 GMT  
		Size: 115.0 KB (114958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da9a010747cb7c8e95bb952c9e8d9e7a724cc6d23cbc6147c987ae59b84ac1e`  
		Last Modified: Tue, 28 Jan 2025 23:28:21 GMT  
		Size: 17.9 KB (17917 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:f2fe6e6da581509fa9fa12d397afd50a9e83a70897486f21e8328501edbf0bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7028589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d572d596be6793cd040ce1b82be692480ebd337fc1ae238b437cdf99d28fbf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_COMMIT=25e213a551dc808c7f29360075bad4806fb9fec5
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_VERSION=devel-20250124
# Tue, 28 Jan 2025 07:24:49 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c609346feefd24f529f25fd37883c8f54483d60d36f9cf7bc7e058e6699b4437`  
		Last Modified: Wed, 15 Jan 2025 01:24:58 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2297d5c0364e1892d6627c2fa1a7854b174617e500849c17c84d655752fa2d42`  
		Last Modified: Tue, 28 Jan 2025 23:28:29 GMT  
		Size: 3.0 MB (3035437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b4ff28e21cc1c930865f7063dfde9f3cd0958e5e0f8d8ec668b941bfa7251`  
		Last Modified: Tue, 28 Jan 2025 23:28:28 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:a24b66bfde21a8dbb1197bef2ccba024a4f5c68aa28c97fd1798730ce4721ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 KB (132923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1735acda04402ca14cafa9200ea61fa7f77dc5de41c1ba3d9fd7bf9f338c34af`

```dockerfile
```

-	Layers:
	-	`sha256:ddc4963a252ff36a320267ea8b258f095d8d7e8294cfceb714626ecf70bfaaa9`  
		Last Modified: Tue, 28 Jan 2025 23:28:28 GMT  
		Size: 115.0 KB (114978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd4977c135cceb3275e3f1db5eab382868d5f85e38ceda8a71083120e2d5456e`  
		Last Modified: Tue, 28 Jan 2025 23:28:28 GMT  
		Size: 17.9 KB (17945 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:c9d35412e6b4650727a667f5e2d495401ab38232cc07890ce8506cfe8d74b683
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6341582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2697e1a2f9e8233fe7774cdf0788aca796bc0dce899ecb76caaf71e9fc6b9cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_COMMIT=25e213a551dc808c7f29360075bad4806fb9fec5
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_VERSION=devel-20250124
# Tue, 28 Jan 2025 07:24:49 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d216b23d98250b1acf9c41015735b10591b64db988340ed0d2f2eac8994d3bd`  
		Last Modified: Tue, 28 Jan 2025 23:28:46 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780c2e831dfce406cb574c8a08d4a036c266bdb0b163ed9ca407214e4a6732fb`  
		Last Modified: Tue, 28 Jan 2025 23:28:46 GMT  
		Size: 2.9 MB (2877660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5645b509a8248f3df0eeb7a5fb86f0cb30796b054b4088ec1bf871c324bc10`  
		Last Modified: Tue, 28 Jan 2025 23:28:46 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:5c33cef894bf4de9cd6f06887fd0f5e87a7941d42d0def82974b8bfd1465f4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f863cf982d1a7ae9a3f47227502b4237b2ffb037c5f1e95cbff20a52ac2d54f1`

```dockerfile
```

-	Layers:
	-	`sha256:7dff48daf71d729f1a68845824e560c35a6e131f2dc974ea1f174098a2d77158`  
		Last Modified: Tue, 28 Jan 2025 23:28:46 GMT  
		Size: 114.9 KB (114897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:005f14d116678d4b4c836573e7222588310499d45cf6780b3e2caeb74adc432b`  
		Last Modified: Tue, 28 Jan 2025 23:28:46 GMT  
		Size: 17.8 KB (17809 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:cc6937a1db684fdeac30e71e2815e42995e5b637464874cc8cc621f5d2d64e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6793205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3efa42c66a73ea616e27fc81d08c7a287257be6b44e3ce992fe6f3beec846f64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_COMMIT=42c49d621d9341a530bca9422d7000087593e6bb
# Tue, 21 Jan 2025 23:18:21 GMT
ENV _BASH_VERSION=devel-20250117
# Tue, 21 Jan 2025 23:18:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 23:18:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 23:18:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2864eb05966c89ecc2f693f15dd35b154f22759821c1d4a8757dec136d82aa`  
		Last Modified: Wed, 08 Jan 2025 17:58:42 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9011025ba1c291dfcdca50359d35f53ec9c28235256e3362d026ea0bde3d872`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 3.2 MB (3218807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e975d10408974806fab354e47451575b438b7bfa7fb987dae80c001c1ea0960`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:09d09640dfc0712ed3c8269230802eb452b18531732795d07673249c0612705e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 KB (130870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5e495d0e94de40a35069faa58a40b7f9d33e1789b2a424f7ac661dda4fa77d`

```dockerfile
```

-	Layers:
	-	`sha256:c184ac50f630fe312f9c967aff554b5150b143995197a88b6b60c3097009a369`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 113.0 KB (113005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f1758b06bfbc770f925c9980e69245b84784b0f41a8ffa944b1f0374b9c0d1f`  
		Last Modified: Wed, 22 Jan 2025 03:08:49 GMT  
		Size: 17.9 KB (17865 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:c41a14659de4787338ac62ed7eed734a99deae07c6938577f4e22fa0ff01e43b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6252198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a3c0086d6b250c381d0169f9ead1199f11ef47a6b152cf4047d784a7f23f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_COMMIT=25e213a551dc808c7f29360075bad4806fb9fec5
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_VERSION=devel-20250124
# Tue, 28 Jan 2025 07:24:49 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee5ec45bdf477db840352ec8979a5377f81b57c5bd134c10ef0dd422448e2c3`  
		Last Modified: Wed, 08 Jan 2025 18:10:13 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822948256f1785035bf5bcf766a0d27ec120c65cdac257a9ef555251c9acdb10`  
		Last Modified: Tue, 28 Jan 2025 23:36:42 GMT  
		Size: 2.9 MB (2901147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b4952736b4fd86cf45b8df993563821148407abbfb5b13b936992f87b14962`  
		Last Modified: Tue, 28 Jan 2025 23:36:42 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:e3f9f67b3763bf52f6ae5179bc912c49d2e884e8125be5f3ef4a1cd6000ade01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 KB (130886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12b5b8055d93275e911a933dcdfcd5791ec47a84cc63e78ebf08beae36a530e8`

```dockerfile
```

-	Layers:
	-	`sha256:b4b2afb868bc07f98ab9bd114bb8d949e8cb887a3b9d44b0e9df3ecf89cdb864`  
		Last Modified: Tue, 28 Jan 2025 23:36:42 GMT  
		Size: 113.0 KB (113001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc4a3c850832abfa7f13c03561fc6ca0b54553778f0e18e11f1415715f3902a`  
		Last Modified: Tue, 28 Jan 2025 23:36:42 GMT  
		Size: 17.9 KB (17885 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:ba7bec021e7b23456053dc732b1b91c7baccccc0c3d4d7ab23a5436781adfb38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6513063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832a5011ddcbb039417e3d1f1b7b20e370556d37427540c785c59de458b509ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_COMMIT=25e213a551dc808c7f29360075bad4806fb9fec5
# Tue, 28 Jan 2025 07:24:49 GMT
ENV _BASH_VERSION=devel-20250124
# Tue, 28 Jan 2025 07:24:49 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 Jan 2025 07:24:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jan 2025 07:24:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a540196e840d845bf43b1d53eef177cb5b4cb8a0d8c3c3d0ed9a38955a9f84`  
		Last Modified: Wed, 08 Jan 2025 17:58:08 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ce934cc7fb2894cdb3b5e7adb8d1377eb027100b423aca065fdbbf803ddb40`  
		Last Modified: Tue, 28 Jan 2025 23:29:06 GMT  
		Size: 3.0 MB (3045404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf9907bf4656e3a2d41bb48c88809741c634968a1ea0a53ed790792d0b7d647`  
		Last Modified: Tue, 28 Jan 2025 23:29:06 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:6e497a6e760baf4aba8ed171e2331c7fc6c9d7d2187981e90404a7eb2e387186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f04730d3a36c6c42367facfb0a27513f3bb157f08c6b728f5ce645276a4e3df`

```dockerfile
```

-	Layers:
	-	`sha256:e9900d926f3b3a346278467ce5c410c30febd5d9e1ec6927f075e27304809c37`  
		Last Modified: Tue, 28 Jan 2025 23:29:06 GMT  
		Size: 113.0 KB (112971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25d47f972047ca22ebf78dc7070f8be1ba09bd9210f90f0b2577bb4d47d422c`  
		Last Modified: Tue, 28 Jan 2025 23:29:06 GMT  
		Size: 17.8 KB (17841 bytes)  
		MIME: application/vnd.in-toto+json
