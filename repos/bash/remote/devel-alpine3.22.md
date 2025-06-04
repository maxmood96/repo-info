## `bash:devel-alpine3.22`

```console
$ docker pull bash@sha256:959840dbb856625c1ccef797d62c9569b56bd561f577bb323281e134f645629d
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
$ docker pull bash@sha256:1b7c98ef01afc1707c56d502e86062dab38e2d21b60855c3f011318466d4a783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6795488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1a1ac91b13cc3fa1719fd026fc6d23a7e4736dfca82843081816cd7379b253`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_COMMIT=dbe4256d5ea02fec1817fe7e275b0e534dc33a40
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_VERSION=devel-20250530
# Tue, 03 Jun 2025 04:18:01 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4374c4730d2ebe5b6bc18f29b58b24b0ada2b048ee550cf66696f2d314790d`  
		Last Modified: Tue, 03 Jun 2025 22:39:00 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52571f00920644bab648d8e54923d7086504b1d08a4daec930387fa1bf10a2d3`  
		Last Modified: Tue, 03 Jun 2025 22:39:01 GMT  
		Size: 3.0 MB (2997853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f03b04992235f160cb273dd41494e175cf73d3e257c37ed3df26f308f64861`  
		Last Modified: Tue, 03 Jun 2025 22:39:00 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:413ece88ad3a6d5f9a8ba2df1b47cdb2dc43aa2fb525f6600b3190f24aef8fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 KB (136078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4ba2a97c7878fafe19f9dbc38ac7e23618f7dc7f908dc702fb4bbf50e0d688`

```dockerfile
```

-	Layers:
	-	`sha256:5ba363e5a2af5a7dfe2c39c131d24c2f8af63165d9eb73b6a9b6c4c4f42649c6`  
		Last Modified: Wed, 04 Jun 2025 00:02:54 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e755223f891814d972536253227a4378ec813b28726bba1bdccd1d494c6ba7`  
		Last Modified: Wed, 04 Jun 2025 00:02:55 GMT  
		Size: 17.6 KB (17649 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm variant v6

```console
$ docker pull bash@sha256:c878f4a7c5e3fcb0fbd5e206f740b10a80dbe247409ea5b6c6c7407ee854368c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6435624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e5250d9ac9ce79da7e1f9fc7ed1e1ef7badf05ec52c964e4e72867bdad77da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_COMMIT=dbe4256d5ea02fec1817fe7e275b0e534dc33a40
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_VERSION=devel-20250530
# Tue, 03 Jun 2025 04:18:01 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa72c6a9e21dc757e636874754288c8a9e0c46684f2567c68530f8619b60f607`  
		Last Modified: Tue, 03 Jun 2025 22:50:33 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b1e2c9e706f6afbfd31727bcd2cfd7eb82a2e30b94eb5e5007af0164b11df3`  
		Last Modified: Tue, 03 Jun 2025 22:38:23 GMT  
		Size: 2.9 MB (2933903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c93f045cc135d10362d3dda6726beb73678ed9d721420beca62184502a5e5b2`  
		Last Modified: Tue, 03 Jun 2025 22:38:23 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:988358ab414b62efb7aa52107d46fa5b374b94c3a0a9c460e04d50eeefe03702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a9998cc5045fb592eb3dadd7b268da5b935dbfd99a46c3cf50f8b436079453`

```dockerfile
```

-	Layers:
	-	`sha256:799fc0bd24bd6126fcb9bb47cc0b3ed86493aa5bd717d3827764d1ec4d9e6a82`  
		Last Modified: Wed, 04 Jun 2025 00:02:58 GMT  
		Size: 17.5 KB (17510 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm variant v7

```console
$ docker pull bash@sha256:fc93087ff536e9603a3fac7cfe341a780c1a75ed91929fad898dd0a89d7e2a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6103966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f578939ae25f7e5ff80eab7e8848137522a658d2c52e485044545e51cc114108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_COMMIT=dbe4256d5ea02fec1817fe7e275b0e534dc33a40
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_VERSION=devel-20250530
# Tue, 03 Jun 2025 04:18:01 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345f6f1b0ad8403dd591b815dacd505a425ee595bc14fce2a619c5013c072b72`  
		Last Modified: Tue, 03 Jun 2025 22:53:10 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d302d8f536e3c90e3d0df650fb9422f8870f4ad686fada9529d90f430b185664`  
		Last Modified: Tue, 03 Jun 2025 22:38:22 GMT  
		Size: 2.9 MB (2883998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6f31d174e26f25b829fe6c8861bf14e0e0a84b5ac07730dd9935907abebc71`  
		Last Modified: Tue, 03 Jun 2025 22:38:22 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:e5e6207166579c5c008b018ca030f0d5b0bf0292f88fbb3a657872ca39b15976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 KB (136190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37dd88b13acfea0c3cfd43243c1acd4e33a32f26aae9f237ff94eb932fa4f4a6`

```dockerfile
```

-	Layers:
	-	`sha256:5d8aaf9225f9d9a597794ed42c5a62df713882a123582dc3b9573074fac1b5cb`  
		Last Modified: Wed, 04 Jun 2025 00:03:02 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a412314ac1e0262c02966709972b1421b82a7c1abe0478897b57c51b44e80756`  
		Last Modified: Wed, 04 Jun 2025 00:03:03 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:f283f826d63f85ba8c9622163acaa8a5685e43d87da38a9ee3d8f3ec529ecc7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7220647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54647c62fd8d6b8eda91e0600574695030670a232b38d16486280d5a7253b101`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_COMMIT=dbe4256d5ea02fec1817fe7e275b0e534dc33a40
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_VERSION=devel-20250530
# Tue, 03 Jun 2025 04:18:01 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4acd4ca2748e61184f091eabee480069c09f2f7bd94917e9f2f79e4e8dd086`  
		Last Modified: Tue, 03 Jun 2025 22:50:57 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797300df53eeb871544545865a367b608b0bdeafd2fe8e486762e50539e6844c`  
		Last Modified: Tue, 03 Jun 2025 22:51:00 GMT  
		Size: 3.1 MB (3083915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc76fd40aafd8e9dfa8f5e651062fc4942b2ef2eb4b010645c96bd1713b355b2`  
		Last Modified: Tue, 03 Jun 2025 22:51:08 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:f1021b1943d4acf960c9fc766fea73fb15fb04ba6eeff95a9ecea23952bc1af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 KB (136238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a84dfda9c51f00d0d9e3e5b7ee7370fb515822e637368d0341d3688ba9d117a`

```dockerfile
```

-	Layers:
	-	`sha256:49d6f128ea51d0286c08a0c2d20798eaad4fedfb8065bacbd4312a61e5a9ffc1`  
		Last Modified: Wed, 04 Jun 2025 00:03:07 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:608cd4de182a8df41f17d7fc692beeee9bcf5711ccfc8e4489ff5367aa958fdd`  
		Last Modified: Wed, 04 Jun 2025 00:03:07 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; 386

```console
$ docker pull bash@sha256:74d6693c2b2fef7d102a90e7affd86ff8c21b0c034e7a7856eaaa80ab2f084ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b038d1fa74b60eda86872b9e15e6346f8294241f0ab404115d22bb3e8bc16eec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_COMMIT=dbe4256d5ea02fec1817fe7e275b0e534dc33a40
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_VERSION=devel-20250530
# Tue, 03 Jun 2025 04:18:01 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5173ae93c02ea3ad92601e4233cb978bd84070486ded1bdcab5ef72f51f25dad`  
		Last Modified: Tue, 03 Jun 2025 22:39:07 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e7dd04f6df7c594e4deee162eef0d23960d8e852e085fb08962c9e6d3cadaf`  
		Last Modified: Tue, 03 Jun 2025 22:39:09 GMT  
		Size: 2.9 MB (2924582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23773273a669285234f96ae923e700cca6b85887eff7239e4b9ec057e0bd57`  
		Last Modified: Tue, 03 Jun 2025 22:39:09 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:cb418878b0fbdb6933768c3e9e21dae33e7c2c4145dc46e15b92084307ac8682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 KB (136020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa73327de78972e96b632d9e0ba4f3ebe5553863358448c9cfd7a9436158a04`

```dockerfile
```

-	Layers:
	-	`sha256:81d925e8ba8aa9966ad9ca56072d6edb80fc8a55f33435f3b0c178a7ca832cb5`  
		Last Modified: Wed, 04 Jun 2025 00:03:11 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ec1714b99c82a5e05162701fed7fb67f6d0d8a77dbe0771ed879724f3468bc`  
		Last Modified: Wed, 04 Jun 2025 00:03:12 GMT  
		Size: 17.6 KB (17616 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; ppc64le

```console
$ docker pull bash@sha256:7652d0643a3ae683946b21c8a9f48edaaece064aef3b87cddca025f85e143d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2a53561751c7e228ee1941a67e678188a2fa8b92f25f4d0e70a39dab4d3f9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_COMMIT=dbe4256d5ea02fec1817fe7e275b0e534dc33a40
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_VERSION=devel-20250530
# Tue, 03 Jun 2025 04:18:01 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f9d5d7928a8f09e32bb78bd4075729362bf942ce757b9dd4229425488fc06a`  
		Last Modified: Tue, 03 Jun 2025 22:51:15 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e789496201e87a147bdbe8d783f61cc1af077bfe24d267d3a31ee84f0df01e1`  
		Last Modified: Tue, 03 Jun 2025 22:39:01 GMT  
		Size: 3.3 MB (3272633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0aa7dbcfa57f9ac759a4aa8f081555863d6fe902ff040635b9008d897460dca`  
		Last Modified: Tue, 03 Jun 2025 22:39:02 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:23e1e686b8b966bd46af881522fe5e09c474d5f967bbc84ca344aaa077596d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 KB (134204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ba6337cb5a18d72b7f6433a7c5ded6fc18cb253c2fc367a9337f94ab94d53e`

```dockerfile
```

-	Layers:
	-	`sha256:d36fbb25ca33b2d179ec99cfd01f5baf5aa8a4d4d444bd21872b4986b7da2306`  
		Last Modified: Wed, 04 Jun 2025 00:03:16 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06bc1e1b61ba16d3a0600d80a685d37fc3e36463a2239e7e56b62378422d94fa`  
		Last Modified: Wed, 04 Jun 2025 00:03:16 GMT  
		Size: 17.7 KB (17692 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; riscv64

```console
$ docker pull bash@sha256:08b66d048a41005a3e93ff19fc55fe30bafc2f72925c36804281b1afee46d6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63b7414bb02cac6d7c9b07766d01d2b721eda501041de8c3f49a5ec171750cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_COMMIT=dbe4256d5ea02fec1817fe7e275b0e534dc33a40
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_VERSION=devel-20250530
# Tue, 03 Jun 2025 04:18:01 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d9c7d21cff81f34ab6ed79c306ac7f740386530ff46f996e5d394f46f4626`  
		Last Modified: Tue, 03 Jun 2025 22:51:48 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23722ca5b155c4e6ed123a1f0e0e1acd0300f7bf052627d2bf287bf8c77fe1fe`  
		Last Modified: Tue, 03 Jun 2025 22:47:22 GMT  
		Size: 2.9 MB (2944661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f992e4e4c6cbd088174c0b88590e9d5f7e583842de1e027f8742a1f1e177ee`  
		Last Modified: Tue, 03 Jun 2025 22:47:21 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:3a4b9b1e234b736cd81f2f94dfb133a9ac7e159f22e2d385aa0c5e5c5da5504b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 KB (134201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f0ef858d91a744e69cf2e69d4fd068b04baf3b5cbfd8efa80f3e0058647e29`

```dockerfile
```

-	Layers:
	-	`sha256:acedb71b76393434fa2cd650a6926d028d73eacccb697d00a79db5831a0e16ea`  
		Last Modified: Wed, 04 Jun 2025 00:03:21 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b040a9576dff1c64e64b3c2c83087de786038925f6618fc1cbc5cd50ae3f50`  
		Last Modified: Wed, 04 Jun 2025 00:03:22 GMT  
		Size: 17.7 KB (17693 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.22` - linux; s390x

```console
$ docker pull bash@sha256:7cbfb9e2b31ad7d1e9a54cbbf90b1fe3fc1b55ae98370b64251606ac5de2f891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6741995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e450cccf9e9bb07c2959c557c450b65f00026651861f3334dcaed80f99c610f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_COMMIT=dbe4256d5ea02fec1817fe7e275b0e534dc33a40
# Tue, 03 Jun 2025 04:18:01 GMT
ENV _BASH_VERSION=devel-20250530
# Tue, 03 Jun 2025 04:18:01 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Jun 2025 04:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Jun 2025 04:18:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f709b1b5c7aa325170bdef132d7c3b3e6711de73420cc6a2de43a76dfc7deee2`  
		Last Modified: Tue, 03 Jun 2025 22:43:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c197a020ba10ad328f997dbd89c7f999b5d85ad45d38c22504989253e44d8cbb`  
		Last Modified: Tue, 03 Jun 2025 22:39:30 GMT  
		Size: 3.1 MB (3093678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade106694378bfbdee8a85dc7d8951b1b56b371ab02a0d9dc91ee2c8783bdeec`  
		Last Modified: Tue, 03 Jun 2025 22:39:30 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:6d0ea548bf1b3e3ae6662eaa639ea3053877cf4b533f75ca8e650d948b0c45ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.1 KB (134127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32be9500d3b1a8c8feaae9350d8accd22adf953338881501412de5032ffa17c`

```dockerfile
```

-	Layers:
	-	`sha256:a36adcbe6767d51b92cafec532418685faffa87a965aca036b099a15fe62b979`  
		Last Modified: Wed, 04 Jun 2025 00:03:25 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99c789cd12d6be8c37dfe0867920a146094f5bc4613b50119ed754d2cafe7aa1`  
		Last Modified: Wed, 04 Jun 2025 00:03:26 GMT  
		Size: 17.6 KB (17649 bytes)  
		MIME: application/vnd.in-toto+json
