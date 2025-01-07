## `bash:devel-alpine3.21`

```console
$ docker pull bash@sha256:9c2353cb8f5cb77ca169c24e364d282c03bd15e80918ab1fe318ee2b80d72dc0
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
$ docker pull bash@sha256:d1b30d0472c4a9dede3e1aa160f7ad89425263b5071fda0f40f1a391fcec7c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6593800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8962d1584be969e8614b301d9c39f20e445d6bad7ba10099e4946f4287d2cbd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933a33a76fe54f82b4a99df8053f071345a19d82bb182d5e9d5908687986f4af`  
		Last Modified: Thu, 02 Jan 2025 18:29:15 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db9bf5a7cdd63f55e2cc9ed9f5eee5ea7421eefabcc14aa45964fbdc51f791a`  
		Last Modified: Thu, 02 Jan 2025 18:29:15 GMT  
		Size: 2.9 MB (2948563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36464530a93b88df072a13c93698b6daa7d9ecd555ce5d5c68e6bd9f2109c75f`  
		Last Modified: Thu, 02 Jan 2025 18:29:15 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:4ccb88bb574aab95cd26af2b573daea0506a526a383a5534bf5fe0f4bcb4c3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b6a84a40edc481c89b5ca1d6f84837305a20fd3c1e97a4e492a33c6e2d9332`

```dockerfile
```

-	Layers:
	-	`sha256:b78eb7371747c539aa19f1ec1e3906b6aab603664e2338c05c20927c51558124`  
		Last Modified: Thu, 02 Jan 2025 18:29:15 GMT  
		Size: 114.9 KB (114922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be751fdb0b50ee0f3db293907c2048ff4df13602e0d16ee7182e66e7496632b`  
		Last Modified: Thu, 02 Jan 2025 18:29:15 GMT  
		Size: 17.8 KB (17804 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:964d635e6fc0b4ac71a47954583d11caf3bfccef2fd5ab5ec218de31e68abde2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6253820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa5dff28327aee4c74bf7fb1309ca2cba60dad3d4f3c3e200e2515b05a49a90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dad000104d8d6e4aac117d865936836caa8bf357d618a8bb7acf231795da1a2`  
		Last Modified: Fri, 13 Dec 2024 01:30:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eca77a41622c23669b6059f8b649183a553d0839c2a5627e303f4b3b24f718b`  
		Last Modified: Thu, 02 Jan 2025 18:28:45 GMT  
		Size: 2.9 MB (2885850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada21cdeb48b55f9668ea646fe35e4a7a06805a8d6731023068b388fa410700d`  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:c58c07d32fc0426c6b4322f5aa27ca062cf0279c82816dee43bd728b0c2d1971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 KB (17665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32eeda0bf86905c9dd38d3ad2203717b71d3ac752446ee91e49c37f8fabf9f52`

```dockerfile
```

-	Layers:
	-	`sha256:361f03c3a53005e40b355e23f12004f81fbe2af5784ba2b85abdc3912bc53a4b`  
		Last Modified: Thu, 02 Jan 2025 18:28:44 GMT  
		Size: 17.7 KB (17665 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:ce409bf09e58cca8375d7e378986ead32dd1aca83055958813eddbdc943464b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5938076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce3d5b7a717e7615fa45a88a7d20fe19c0d196c9e956c35d077dc25099a07a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092b47e0e9bd9310a551d1dc6827d9f6b0069c38ba1559b7a818161c42820f4a`  
		Last Modified: Fri, 13 Dec 2024 01:32:24 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114acb15a81bcd7926e0a2647b1c7b2773cea7e72f09347f75da2d3e02704ad9`  
		Last Modified: Thu, 02 Jan 2025 18:28:52 GMT  
		Size: 2.8 MB (2837250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55c5a15e2cedeacb113e9ed4260ce97857bf46bee20eac0f3fd0976d68297ac`  
		Last Modified: Thu, 02 Jan 2025 18:28:52 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:15ff9cbac079c3322a3fdf34b8ecb5b16309bae1aaaf15f9adcb29c36f7f419f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091561016dd5d178ebb27ba823a02dbd5356bc4c42e0f489445f930f9aed5406`

```dockerfile
```

-	Layers:
	-	`sha256:f766ba46921dfda61bd2ee43afbae8f38509e0179606e64f4f2f4f12aceff47b`  
		Last Modified: Thu, 02 Jan 2025 18:28:52 GMT  
		Size: 115.0 KB (114958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d06c39a9fc27a8ca52e9c2172cf3559ef0c3c809e504710f6034473ad69a7c6`  
		Last Modified: Thu, 02 Jan 2025 18:28:52 GMT  
		Size: 17.9 KB (17881 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:1a793cb79d95c2c953dfab3323876d3a1a47be62a28b813429cc657fc7365e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7027182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d971d19d657a23f96213a24cd61819427769ec68ec64cbf186903ecb3029ea9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bf7a7d9a0c61bb76ce352187a74e22a43dc03fc95614ed659a63b2a9f0b716`  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e698284d9796c81df644730d889bc3c1c0ce62052a24cbeff09604acf71dd321`  
		Last Modified: Thu, 02 Jan 2025 18:28:28 GMT  
		Size: 3.0 MB (3033208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fc511228c4db7d260919b8fa3d787770d9db6f267eda11a435aadfc5aa02f9`  
		Last Modified: Thu, 02 Jan 2025 18:28:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:e90be2a6cda67d2d9c654b5a2816f13f7aca9b07863cfd4aebed452060fa4f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 KB (132887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d308c99e9853659ccce093288477b30c31db1c76786f65b97dd0cba907ca5c`

```dockerfile
```

-	Layers:
	-	`sha256:8111c1779b13af89bc1ea8c0e049108d18b92f46946a585b550bc1776cfef87e`  
		Last Modified: Thu, 02 Jan 2025 18:28:28 GMT  
		Size: 115.0 KB (114978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84c3d679de0170b14c87cf7eae1d0458a3fdd3fd6cab5c9c3e89160eceea7e78`  
		Last Modified: Thu, 02 Jan 2025 18:28:28 GMT  
		Size: 17.9 KB (17909 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:4a8ddad0582f0558870d8f46d1f9f7655b4a291bf33676cdad97f5c2dab5ad2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6341912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816d90bcc83c9613b46be25fbd7e96ee1001e647acc281349dabfa1ac9ed8c97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88522e0eb8b468a959552a1174ea35467dd022cedb906daffdeb112e56ba267d`  
		Last Modified: Thu, 02 Jan 2025 18:28:41 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805ce5217f129c4ddc350b3d6447c6934fa1f5065c04315f9f7bac9dff1ac392`  
		Last Modified: Thu, 02 Jan 2025 18:28:41 GMT  
		Size: 2.9 MB (2875041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3f328857ef4da46927832006561567888edfba50b5685314e9f1bf15357e1a`  
		Last Modified: Thu, 02 Jan 2025 18:28:41 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:a4d8f756b542be1f62cf986eee8f35fd78bb99a617f17725ba3e5a7c8e6371b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267048749bf504a9030efead2ea0e3cebbedd938be121483b303a4c7446fadfc`

```dockerfile
```

-	Layers:
	-	`sha256:b2324835aa8ebd3bd7189ec7695879d06260595d5e9cfab80d16b73232901819`  
		Last Modified: Thu, 02 Jan 2025 18:28:41 GMT  
		Size: 114.9 KB (114897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892d25145da9659d419c8ed56e52e81ce76e2c22d8792b1532cb4a5c99501ff2`  
		Last Modified: Thu, 02 Jan 2025 18:28:41 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:30662f47e7d70f33ed2ca09062998f4197c8cf953528ed82b2b5e9b8bc982293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6795138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041b868683b40125fb8fda0cef861a9344f4ed793427f4b1ebbabdd7da7278f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b87b85a573e0641b22c0c1975b4daedc795bfc844d58d95354403cfa86fb1d5`  
		Last Modified: Fri, 13 Dec 2024 01:32:04 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edb3f4eaeb27f62b8dbc6407aa18972dc113756e1246fe0b113b201347ee74a`  
		Last Modified: Thu, 02 Jan 2025 18:29:04 GMT  
		Size: 3.2 MB (3217240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa6f44ab6a25a835a8bd91e8fc6e174cc4b31f8d0c753b981570eb8d70966f3`  
		Last Modified: Thu, 02 Jan 2025 18:29:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:34bbc946fbf5c2f1528b1c6d1b5b4699def1193f4f8a383a08e0736361e8632f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 KB (130853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324fc1f1b367984d90a27dd9d20b9b1de1b9a85fe7374714a179a5ecde79c3a2`

```dockerfile
```

-	Layers:
	-	`sha256:e929fceeabc42f9710f1928f3bda45d42ed2637bd7c8eca3c83d79b6b225df54`  
		Last Modified: Thu, 02 Jan 2025 18:29:03 GMT  
		Size: 113.0 KB (113005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75e01241d22b15eb8c122f0c2e2fac8a76a710ad298194ee8f1d73b63a25b0ac`  
		Last Modified: Thu, 02 Jan 2025 18:29:03 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:38f98f057c8b2f7a49a39e042461c622a5e8a74f12b2301e62970a532530f47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d41300c38f9a7651df3bc6859da7ac1dbd73a29d90367ce839e76684b9f95ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e78ecf1799363eb590970338b7d1c596a4b70bbabc18d7b41caa66e767f889`  
		Last Modified: Fri, 13 Dec 2024 17:51:42 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a7c68ffc9859807e5c8ad1c1f64d23a6f1104495ff7a9516b075366c1040dc`  
		Last Modified: Thu, 02 Jan 2025 18:36:30 GMT  
		Size: 2.9 MB (2899545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f0ee3281b5491b9892e13c077f2a31a3c31fad202480f9ac03a49891d11142`  
		Last Modified: Thu, 02 Jan 2025 18:36:29 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:1af5810888a83ed53e464c5d7379985e84f19946b9c236f3d68aa3ad100d71a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf784281b4a8b0fd382e2706bfd9a9faf9f18b52e0e251e0e4315082970b07a3`

```dockerfile
```

-	Layers:
	-	`sha256:26f01b247e838b6624c401eb5a78d183336438646f6cb738c4fd41f7d4b8a504`  
		Last Modified: Thu, 02 Jan 2025 18:36:29 GMT  
		Size: 113.0 KB (113001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f290b31f6a3533586dd3238ae30ab5e5361ceccfce7fd1fc9e7482a201f7cb8`  
		Size: 17.8 KB (17849 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:8a79e64a0d11871771b30ef0f4f9df9b600d3a7fbefb017dc42e0f58ab0c5026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6514009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8495511f2f08623f5a352217f0e858c715fc3ff3899e70da43f20c27f23eec1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_COMMIT=5114e17172276cf5a2f889f8037ae58c4cb05bb9
# Tue, 31 Dec 2024 11:18:05 GMT
ENV _BASH_VERSION=devel-20241230
# Tue, 31 Dec 2024 11:18:05 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 31 Dec 2024 11:18:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Dec 2024 11:18:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7b36c75dc9cb14230978822a9eeb1b65d331a45290bbeb33d7ac0fda7b1caa`  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a172e73832340a69792954a4d83c96cab7e402bd48c956fa7027f364b59cc5`  
		Last Modified: Thu, 02 Jan 2025 19:44:05 GMT  
		Size: 3.0 MB (3043703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9447bf203d24211dc0926d6d6599df92bcdd4e4841dea6b33972db62c08b7070`  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:981001a59655bc6e46c0f725fc773366c34fb9a1435ee835baf1e4d0d62edb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24aa49c4f149874ac4699b0ae0a5eca27c50afcadbd6303fba3369e244ef2a85`

```dockerfile
```

-	Layers:
	-	`sha256:20bee97be5303622d745f51a2bcbedeec53fb06fea30d04ba0acc5ba63560d82`  
		Size: 113.0 KB (112971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e859cece2758cb81e01dc96999074cf3ebab4b887bf8915c11699005fb6f414`  
		Last Modified: Thu, 02 Jan 2025 19:44:05 GMT  
		Size: 17.8 KB (17805 bytes)  
		MIME: application/vnd.in-toto+json
