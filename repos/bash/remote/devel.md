## `bash:devel`

```console
$ docker pull bash@sha256:7ddb078aa77fad1cdf8bddd0211ec7519b53915e5c9ca220b0a82b168f3b1edf
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
$ docker pull bash@sha256:3ed69a58428cf1120aa35aea6dd7380a2d6a90fcf54fa880323d8cc11547c090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6795971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad3a2e2b1e65831cacf642f9a6b8a6a131b684bd2d6f81545008d1545bd37e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_COMMIT=b35866a2891a9b069e37ca5684d4309c0391e261
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=devel-20250627
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2cfc17b65ac62faa6d53138bdf9d0e9a9b3307c6ca76823fc8d1ac1050e29d`  
		Last Modified: Mon, 07 Jul 2025 22:56:47 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b58bbbb3b26b1965fd5fcf8decb76ae9337e26c6d93de75406d2504a3b0672`  
		Last Modified: Mon, 07 Jul 2025 22:56:48 GMT  
		Size: 3.0 MB (2998334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74270d511227ae798071e909190a43e406fe310b125df08f378711eb1fde721b`  
		Last Modified: Mon, 07 Jul 2025 22:56:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:99837adbc2a96536f156a3a5873adca09dad2d9686dac1739b0ca165e458adf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 KB (136364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e32c92b03fc857929d8da8190c22039f2813813789e35db7315c7b0b9a4c5d`

```dockerfile
```

-	Layers:
	-	`sha256:9a848395ded2a94ff6b16930cb8c301d3e259f6afc4b4c479d956326b4aff34a`  
		Last Modified: Tue, 08 Jul 2025 00:04:04 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6d2153e36b6caf042e5fe247b25b5dc895aa4982db2c64d3da9f6d85b84990`  
		Last Modified: Tue, 08 Jul 2025 00:04:04 GMT  
		Size: 17.9 KB (17935 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:e24d4afed57694317879ab91a6d5fe1ebb180c75b2e9b65560dfff8f1c3a03de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6436000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46cb90f09f8757b21e1e9fc7cfd3afd01ffab348f0d04eb4acb08ac735d07890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_COMMIT=0f0cea342e32f1f82aa9cc9026038bfc3bb03e92
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250616
# Tue, 17 Jun 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
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
	-	`sha256:a3ee8c3f762b1058320a4d913f2f919b00c37090e69cd88964dffbe906233ad9`  
		Last Modified: Tue, 17 Jun 2025 17:14:18 GMT  
		Size: 2.9 MB (2934278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650ee08308e529bc8050b57ca5a479d9e75d5f4a83c54a76b495b8e7743c8a8b`  
		Last Modified: Tue, 17 Jun 2025 17:14:17 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0f17246ac8422baa0d9dfab753de3880a623a9917b38b36d7df3501d9f539ca4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff69bcfa762cacdbb010bd04f47dad4e1a9f761db8d90e808be0193116bd5f8`

```dockerfile
```

-	Layers:
	-	`sha256:9bbd0d8451401d3b5540686aff32eed3d14f1507b3e87d1ea04ae5b5f8aeef29`  
		Last Modified: Tue, 17 Jun 2025 18:02:47 GMT  
		Size: 17.6 KB (17568 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:4c0b05fc5effd9eab7d5a238eba65985679ba25a6e0d26d8612b7125fd57f428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345b85fec3e54999e40003b6d471123856322b91daf7f52cd46803fe188296a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_COMMIT=0f0cea342e32f1f82aa9cc9026038bfc3bb03e92
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250616
# Tue, 17 Jun 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93f032839dd1cab190e0e490d5966b24e6101f992f8d57c4e4a1223eb8de131`  
		Last Modified: Tue, 17 Jun 2025 17:46:17 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84491fd51030b3305c190ed6e2c84e0ab4b9875155b86e8c5950034ad7dd96cb`  
		Last Modified: Tue, 17 Jun 2025 17:46:19 GMT  
		Size: 2.9 MB (2884982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94826e7a88adf354f2f7f2b66cb72e86516dfe3dfb82182bee2267e117d8354f`  
		Last Modified: Tue, 17 Jun 2025 17:46:18 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1187be2247a69b2141311e12cf6b9ed42b50de4ebeef2026f9b22f2cd58f053e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 KB (136250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c670e222274b7c2b842ba85c939e3670c265f4e504c74775af3ffcda308412`

```dockerfile
```

-	Layers:
	-	`sha256:f2249d4d1c20692ed084b17b56f010e72cde4b77729d9d251bfe57933088e25b`  
		Last Modified: Tue, 17 Jun 2025 21:02:51 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3070fc798977eff7618defb7ecfbfd37c752af7f327676b77a85f84baacc7567`  
		Last Modified: Tue, 17 Jun 2025 21:02:51 GMT  
		Size: 17.8 KB (17785 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:1dfc7c190772db74fadd8dc1fd9e25256a9970f1aac3a7ec8c84fa25ac8d2e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7221457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cd91812f9947874325c1ee35b94ffb0cb5182c2295ae45152bb708a47330da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_COMMIT=0f0cea342e32f1f82aa9cc9026038bfc3bb03e92
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250616
# Tue, 17 Jun 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773f027333465f385710e2ba91cc2ff66b9e92c5240dfc3943c0fe1d4b34aee9`  
		Last Modified: Tue, 17 Jun 2025 17:44:57 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ace8b711eb27af2d5aa941b1fa1d0853d919592ce7298d6c197369fd890478f`  
		Last Modified: Tue, 17 Jun 2025 17:45:02 GMT  
		Size: 3.1 MB (3084722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02539cf2356914c6a1ebb2932b88498bc7e43ba1f616f14a695b34d630aaaa20`  
		Last Modified: Tue, 17 Jun 2025 17:45:22 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:54477a132d0508123201ebf60ff62443f9bbec1063c076615c2e82b557c353a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 KB (136298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c97fd7754f2838d08e02424582c854332c2c6fd2b30ffb418757fac11967d7`

```dockerfile
```

-	Layers:
	-	`sha256:bbb52baba821b051a474f80dbc7e16b1d6ac1ff715e4566ef0477731836ac2ac`  
		Last Modified: Tue, 17 Jun 2025 21:02:56 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a4cdabfb6af7a6f3d450cad91ac2bbae72e12c31393ef169afc28ceaed2b01`  
		Last Modified: Tue, 17 Jun 2025 21:02:56 GMT  
		Size: 17.8 KB (17813 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:7c0e373af842bdf066f964b090697c81478267faa9fd7f7c814e79221dc88e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6542006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e4b211fd5d356c22d8d272b179f5cbde04d33c3ee3d5482e3af2ecfe06e2c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_COMMIT=b35866a2891a9b069e37ca5684d4309c0391e261
# Mon, 07 Jul 2025 22:42:46 GMT
ENV _BASH_VERSION=devel-20250627
# Mon, 07 Jul 2025 22:42:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 07 Jul 2025 22:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Jul 2025 22:42:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f2887a5f1de5c228333b35d13959fbd8ed530628077003652c2f133a9b73a2`  
		Last Modified: Mon, 07 Jul 2025 22:56:58 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c93d80b9efde93ec8bfaa5d3131119de75c764cd6c7e87fb3e34ff54108ad1`  
		Last Modified: Mon, 07 Jul 2025 22:56:59 GMT  
		Size: 2.9 MB (2925190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2de3697ec3064a39cbe3b1260e755e7988fdb11fc1ce59e556cacdef6abff4`  
		Last Modified: Mon, 07 Jul 2025 22:56:58 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:cd3a0373b04661b2e7e1d2fcd023dd771e75ce277673fe5503de86843bb1828a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 KB (136306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4d4185d5d0a1a56b2ac613a8d3140e0dbdabee3cbe0c2e327c5c12d4441239`

```dockerfile
```

-	Layers:
	-	`sha256:d2cfff15d2812192f77ec016572d44e42aaea1e4aee1d3cd4e1308357ed5a87d`  
		Last Modified: Tue, 08 Jul 2025 00:04:10 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a40220c4fce701e570e5dd6879433c27fb7e899346c3a58c38ce16fc174eaaef`  
		Last Modified: Tue, 08 Jul 2025 00:04:11 GMT  
		Size: 17.9 KB (17902 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:a896159cfc09027f2ac4908b6e5367d14165eb002b9758f6b0a78f88f8aefb23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b1da20f2e2124ee68feb7a1de36fe5931f568de8fe731ddd5ab1b4c66b84f63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_COMMIT=0f0cea342e32f1f82aa9cc9026038bfc3bb03e92
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250616
# Tue, 17 Jun 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b0218cb5d78b12fb4148537202674363c44265fc17b5542e22b2c87de2e89d`  
		Last Modified: Tue, 17 Jun 2025 18:16:38 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:624bf7dd622b12ba6e5d5e117353fe5c8a7c1441eef73258fa9ac0e6dc072119`  
		Last Modified: Tue, 17 Jun 2025 18:16:50 GMT  
		Size: 3.3 MB (3272584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca81a716cc21adf4a70e726de157be2b64067556ffe9dd9947281567477f26a5`  
		Last Modified: Tue, 17 Jun 2025 18:17:02 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:e2c83f7906b15f5a9d434de093be3c348d259f790269cbd909f95d6780c84254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 KB (134265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f131915252590b7a38d4c55c8c6e3b5c6c1a4b601f81fad50c0e6cd3c4875d`

```dockerfile
```

-	Layers:
	-	`sha256:5567c22f3319a317f955aefaa0aaab69cb5b9090bb70e275026a908b3ccdde85`  
		Last Modified: Tue, 17 Jun 2025 21:03:02 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed3ce35602dfc68e7170af69d9994cae74520637c8cb561ea0f33d13e683398b`  
		Last Modified: Tue, 17 Jun 2025 21:03:03 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:661849726eb46908390aa5c1b78c9ef3974a5db7604468322eb2437157138196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32426da7457e2ced39611e948853c693093072e9e02b96cdadd1aa6ccaab8c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_COMMIT=0f0cea342e32f1f82aa9cc9026038bfc3bb03e92
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250616
# Tue, 17 Jun 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
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
	-	`sha256:61e1e2b0cec28aa5f6f161d1e3f084d48d98fdc580d0460502916462b584811e`  
		Last Modified: Tue, 17 Jun 2025 17:22:41 GMT  
		Size: 2.9 MB (2945186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03052eb88ad517a9fd0844fe1feb71130054aff0fde160c0527dbb82a8b063f1`  
		Last Modified: Tue, 17 Jun 2025 17:22:41 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5e3f4bc3674d794e7a1dfc9d7eb21041746b6753c6cb0827248f42272ab5569f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 KB (134261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5946a443ef965a7eef2a5008f300317637243f3ca41c7a2daacf4affb3faef90`

```dockerfile
```

-	Layers:
	-	`sha256:cafea00f92023b5fc099e4908bb684f14402db8d43ae59fb746746945ded69f3`  
		Last Modified: Tue, 17 Jun 2025 21:03:07 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfcf998f7093021c8976b28d77c0278be8f181ce0fd8ffedf0a2afba6cb4cf5a`  
		Last Modified: Tue, 17 Jun 2025 21:03:08 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:439efc96fa1913934c51d171c951ad55fbcd5a3cb4d5458c31f4988c6bd25652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6742246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f484b52e89de4d889a1bcd927249f74cdd39d8d9c82eb284c11189b493fb88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_COMMIT=0f0cea342e32f1f82aa9cc9026038bfc3bb03e92
# Tue, 17 Jun 2025 04:18:07 GMT
ENV _BASH_VERSION=devel-20250616
# Tue, 17 Jun 2025 04:18:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Jun 2025 04:18:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jun 2025 04:18:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b054caaf46699fbe28b4b5895a55b6811050de700a34f3c7b291d1233c355a6f`  
		Last Modified: Tue, 17 Jun 2025 17:50:46 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffa4615c8181df95cae5f3d24da0b7a9495e2d1dc557cf4aaf55ecb433fff90`  
		Last Modified: Tue, 17 Jun 2025 17:50:47 GMT  
		Size: 3.1 MB (3093924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bd040278bd0986d31eceb84079240b5bfd0f47b7a16e7b92b478120c1e5d69`  
		Last Modified: Tue, 17 Jun 2025 17:50:46 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:9d61d4eb71eccfb3d6d98889a92511fb2563b3cbc9376e934081ac9618daf0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 KB (134187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d9bcb3f3b65551efcaa45319b0f6070e05e67be0b21bf6e4a01df652593c78`

```dockerfile
```

-	Layers:
	-	`sha256:8af3a8c45e70376c6b2b801674fc292e22aed3199c40399a527d15beabcd37b4`  
		Last Modified: Tue, 17 Jun 2025 21:03:11 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d439f85fe5cf0cfae8edaf0dbdf2ada4a892db7a3013ff9dd22f64fd3de7e64`  
		Last Modified: Tue, 17 Jun 2025 21:03:12 GMT  
		Size: 17.7 KB (17709 bytes)  
		MIME: application/vnd.in-toto+json
