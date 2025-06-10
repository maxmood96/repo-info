## `bash:devel`

```console
$ docker pull bash@sha256:e8ecf0f146704002239ae54351bd04b5a27d19ecdc15cba5d90b6a533c8941a3
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
$ docker pull bash@sha256:7edddc5a786c7ff816ff241bf6aeeb85025bbe7838638f35226093bd18f52c20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6795984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7376c077c19b6a4cbcb2b6a7c5944c92a670e9032b2e8fdff3f27de89c446684`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 10 Jun 2025 04:18:05 GMT
ENV _BASH_COMMIT=727b8d366390fea446f7a566c4be1be6c0e2a765
# Tue, 10 Jun 2025 04:18:05 GMT
ENV _BASH_VERSION=devel-20250606
# Tue, 10 Jun 2025 04:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 10 Jun 2025 04:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Jun 2025 04:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 04:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 04:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c801d5eb90d1dae10868e79fc22c817b80e8b68eadcd1b29720e49cc66de1780`  
		Last Modified: Tue, 10 Jun 2025 17:39:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f91ce17585064fc609bbf49109ea339605ece5a8d003898edc19aea5c063f3`  
		Last Modified: Tue, 10 Jun 2025 17:39:09 GMT  
		Size: 3.0 MB (2998351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe52d5f12c0d0c4f0d8cf4207fce3f7cfdb215a303406c8c0a60366683b17fb3`  
		Last Modified: Tue, 10 Jun 2025 17:39:07 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d124b74d7976ca0ebc98d638873a26e1a72e820f4dbd542c75d11c0a4811ecb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 KB (136166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2c78f4c0741291a7cc657a535417811d0abcea2f3f2ba9a078b5e2d93cab37`

```dockerfile
```

-	Layers:
	-	`sha256:33eee87b4d40859d08d07ef9ee8175295d14c3420ba206b90252af56beeb8c76`  
		Last Modified: Tue, 10 Jun 2025 18:02:46 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4375b7b8e7fd8ea3221725e7c27e6cdfe6fccfd66a64fc771e4bb83806095681`  
		Last Modified: Tue, 10 Jun 2025 18:02:46 GMT  
		Size: 17.7 KB (17737 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:42f2a3afc7a6cd9c957dcf26ab0c342de555cfa324d32ea1493e98132be21b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6436022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1f19135cfd32e604d5b9d548f67fe528d80b633aca037be264712900a07018`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 10 Jun 2025 04:18:05 GMT
ENV _BASH_COMMIT=727b8d366390fea446f7a566c4be1be6c0e2a765
# Tue, 10 Jun 2025 04:18:05 GMT
ENV _BASH_VERSION=devel-20250606
# Tue, 10 Jun 2025 04:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 10 Jun 2025 04:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Jun 2025 04:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 04:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 04:18:05 GMT
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
	-	`sha256:73c805cf49766f76b3e7ad0ef20b7284b387d8dda7add75b584629287998bfb3`  
		Last Modified: Tue, 10 Jun 2025 17:38:14 GMT  
		Size: 2.9 MB (2934305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9752268b30aefb2cee6d1e55552d8de4ab0ee12bc85bc42441e374cc08d0199d`  
		Last Modified: Tue, 10 Jun 2025 17:38:13 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d34364f3adae76da790728afd782273a244f54293545ac9ec693459ceae1a686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:309ee3a3a010a532afd99b26b4282c43ce4a1356c7bcc4dee2ffe0be7d3c0507`

```dockerfile
```

-	Layers:
	-	`sha256:f5da117bf0ff751858507f794a5a24bd600c762ed8868aea57933a9f821b297a`  
		Last Modified: Tue, 10 Jun 2025 18:02:51 GMT  
		Size: 17.6 KB (17598 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; arm64 variant v8

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:8063f11f020d609939f7dc4dc8dac9c20e2c4849c5ab3f4050a27b7a75cf4e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de58bac55898ee6bc029b6dadb476987c33d2d3d21d8ca5c077e5b2b8ea0741`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 10 Jun 2025 04:18:05 GMT
ENV _BASH_COMMIT=727b8d366390fea446f7a566c4be1be6c0e2a765
# Tue, 10 Jun 2025 04:18:05 GMT
ENV _BASH_VERSION=devel-20250606
# Tue, 10 Jun 2025 04:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 10 Jun 2025 04:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 10 Jun 2025 04:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 10 Jun 2025 04:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Jun 2025 04:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a590dbd7c0291fd4d53b7ea86873a4bbc4855069026cadefea9b991c20d8faf`  
		Last Modified: Tue, 10 Jun 2025 17:39:10 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef142fab9d5715b5142255aaebbf0656dad5be5ffbec0bf87b1a56e8925f594`  
		Last Modified: Tue, 10 Jun 2025 17:39:10 GMT  
		Size: 2.9 MB (2925034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba042d94e05141363066b11c4e6d1e940998e386064f16e05bdbe515322aa949`  
		Last Modified: Tue, 10 Jun 2025 17:39:10 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:00da7f2ea7faeaec770b8ad1a4f5523492a08e2921409e18dfc66558e10887d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 KB (136109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec1a16242df6e46d8425ea57fff2ab5133ab324f8f5cdd6a5b2c9b36507ad3c`

```dockerfile
```

-	Layers:
	-	`sha256:3a7e3b4e81d2220304013717b23c8ddfbb2bbc4dcbe6f9ee221cbe7e9fbb971d`  
		Last Modified: Tue, 10 Jun 2025 18:02:55 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834a04abff67e0c5ec8f18162b8549310cc317fcb1a5021a5f043b895d7f8c13`  
		Last Modified: Tue, 10 Jun 2025 18:02:56 GMT  
		Size: 17.7 KB (17705 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; riscv64

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

### `bash:devel` - unknown; unknown

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

### `bash:devel` - linux; s390x

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

### `bash:devel` - unknown; unknown

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
