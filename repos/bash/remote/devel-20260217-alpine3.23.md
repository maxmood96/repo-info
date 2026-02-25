## `bash:devel-20260217-alpine3.23`

```console
$ docker pull bash@sha256:f002a0c0e2d974f4dc87c2b1aba8e8c70bd4f4999beb7cb2088a6234f7a9a6c7
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

### `bash:devel-20260217-alpine3.23` - linux; amd64

```console
$ docker pull bash@sha256:9b0c623b173e953899000087ea6e004662d125fb8a1bbd8cdb060ae5e6b064d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6889548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3432091e98f14f07e22bb65c5814bf0e909b1b6f39170263882d4fd4244a1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 19:58:55 GMT
ENV _BASH_COMMIT=044c1acc91df168c9e9f1379b9a1ecc75d395bd3
# Tue, 24 Feb 2026 19:58:55 GMT
ENV _BASH_VERSION=devel-20260217
# Tue, 24 Feb 2026 19:58:55 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 24 Feb 2026 19:59:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Feb 2026 19:59:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:59:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:59:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31888ab5389d71ee75af8be4968004e7c384a5f7f02685756b5a5dbec407e38`  
		Last Modified: Tue, 24 Feb 2026 19:59:39 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdb9b0f35911c3f6555fbe9a04ca0c89cd5252052f73ce62278e1bfe59e6229`  
		Last Modified: Tue, 24 Feb 2026 19:59:39 GMT  
		Size: 3.0 MB (3026935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fdbebb85a04fdd0d7860d1dafbdb7ab5f92df3e0df7739572d14d0358d237b`  
		Last Modified: Tue, 24 Feb 2026 19:59:39 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:9ac71c208dc9d7bf829ab2bfb47b319347cd6d35d2168a24cdd809139b3ef670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73613dca5e7fbb326e9e8890be98fde5f80b2bb0c2429b470262a1ff3fb9dbc`

```dockerfile
```

-	Layers:
	-	`sha256:d20b345e81bafb57e8ca06fa2f288a813d509f9131f4f000b75d59ddbda47100`  
		Last Modified: Tue, 24 Feb 2026 19:59:39 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dcf49f04947baae7507ef0c4ddc3d75428bab53147697eb1493a50f61c5d457`  
		Last Modified: Tue, 24 Feb 2026 19:59:39 GMT  
		Size: 18.2 KB (18184 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260217-alpine3.23` - linux; arm variant v6

```console
$ docker pull bash@sha256:c57218b1f1f5b81a8e05f6d5246868b669d939e7c12e381838e6c31af5026369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6556774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d3eaf05154c37e9d8c7deb2df813b5375d969d3c643691b13978c1b62ec3fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 21:27:32 GMT
ENV _BASH_COMMIT=044c1acc91df168c9e9f1379b9a1ecc75d395bd3
# Tue, 24 Feb 2026 21:27:32 GMT
ENV _BASH_VERSION=devel-20260217
# Tue, 24 Feb 2026 21:27:32 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 24 Feb 2026 21:28:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Feb 2026 21:28:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:28:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00ce10d8d9dd1370d656f155a8540f43830b1e5e7ec66670ccb4b8cafd3e7d8`  
		Last Modified: Tue, 24 Feb 2026 21:28:20 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb2f49c0f646f2c75c0f7a9fe5274d9ae9899cba22fe77a1f88181fece0b823`  
		Last Modified: Tue, 24 Feb 2026 21:28:20 GMT  
		Size: 3.0 MB (2986161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f401096504bfda49850e4c5488c45c9b0c4bca83f90c8b338cbb9385d34615bc`  
		Last Modified: Tue, 24 Feb 2026 21:28:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:bb87e018d4d9beff84731b0aad7218a9d12dd5defb962a58257ac589e0a130dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (18049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd66d5ebfab3e071dc914c56d94f3cc828ee5c1f876961e1e30bc6177289bbe7`

```dockerfile
```

-	Layers:
	-	`sha256:2c42d25fd9b15905b065f2a554e77e0678183a845e26ec7a279751a6040f42de`  
		Last Modified: Tue, 24 Feb 2026 21:28:20 GMT  
		Size: 18.0 KB (18049 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260217-alpine3.23` - linux; arm variant v7

```console
$ docker pull bash@sha256:a4506df246a712e960d0c490bab36ed591f44572577a905f94fe551f5b7180ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6218602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c307ee5a4f2c8daff57b8fd9320cf806fb4e8d8cd14f780d0487851ed7d955b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 21:27:39 GMT
ENV _BASH_COMMIT=044c1acc91df168c9e9f1379b9a1ecc75d395bd3
# Tue, 24 Feb 2026 21:27:39 GMT
ENV _BASH_VERSION=devel-20260217
# Tue, 24 Feb 2026 21:27:39 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 24 Feb 2026 21:28:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Feb 2026 21:28:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 21:28:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 21:28:22 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17716e15ae196a1c49ba8eb118f8a07c10aecbaea9654f591cfaab8256f7fdf5`  
		Last Modified: Tue, 24 Feb 2026 21:28:27 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff509299d36ac4ddce4c345959201daae56c82afb656a90e9db913a47cb04a69`  
		Last Modified: Tue, 24 Feb 2026 21:28:27 GMT  
		Size: 2.9 MB (2936088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a336d37864688c63caadea8f3912d204a5f3f32a164681a0c9a336c6f1ca1603`  
		Last Modified: Tue, 24 Feb 2026 21:28:27 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:cf83a04a7ae995c7aba32bf4748e9720494b6eec1dd673714cec2445e48d11a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf01bf2665e434eff3b6027458ef7af354698cfb2f0e59587a9bd119540fbc1`

```dockerfile
```

-	Layers:
	-	`sha256:be0f9b0be843798ec2850758ac7bdb1a3eb7041f8d80ca445252779af3fd9ba0`  
		Last Modified: Tue, 24 Feb 2026 21:28:27 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ccc7c5778b6b6f800b434978eb274436d84f5526a7279dcf48749883c56f74`  
		Last Modified: Tue, 24 Feb 2026 21:28:27 GMT  
		Size: 18.3 KB (18264 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260217-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:2fc4516f677454927c09590039b64592b0c27a48f22fb60a51e748926bb9dade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7295237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6768604c7b7654a26f87eb01dee91536922a3436a9bc1459bf933b15b4f001`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 20:09:18 GMT
ENV _BASH_COMMIT=044c1acc91df168c9e9f1379b9a1ecc75d395bd3
# Tue, 24 Feb 2026 20:09:18 GMT
ENV _BASH_VERSION=devel-20260217
# Tue, 24 Feb 2026 20:09:18 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 24 Feb 2026 20:10:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Feb 2026 20:10:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:10:01 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9609a073dda2fdfda22af936b12c78d05b65808197c9451253a6d9b2d4c40ea7`  
		Last Modified: Tue, 24 Feb 2026 20:10:07 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0279098cf46b3125c79c264f4e2a1fbb4e1a9e34c4577412b4c7dcbbf2730576`  
		Last Modified: Tue, 24 Feb 2026 20:10:07 GMT  
		Size: 3.1 MB (3097353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79253dbdd8addb72c4b0e504794a36a21b7440fecd115385967c88c71fcb488e`  
		Last Modified: Tue, 24 Feb 2026 20:10:07 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:14a917446f5b0c9ec85cd765c36ae3a28eb14c16b6c6f082fa3b22e5c31ad18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddaf6a5c5c3f3cabdbd89218e3b4c06dc21149463546f9e68d4c1b0e40df52d4`

```dockerfile
```

-	Layers:
	-	`sha256:123843bd9a818a188e6158e53275ac266167735b8195aeafa1559f9a0ba73d2f`  
		Last Modified: Tue, 24 Feb 2026 20:10:07 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4df39ce5d5e2e220372b022e0bc322f0009eec695f7fb17031aa3b1d58e83e`  
		Last Modified: Tue, 24 Feb 2026 20:10:07 GMT  
		Size: 18.3 KB (18288 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260217-alpine3.23` - linux; 386

```console
$ docker pull bash@sha256:67f6bf9b2815ec8748c1f2efe8cee7f2c9f81b6aeeec4cd97c2a8d38998b89c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416aa424a912242ccb5a7d7393842828cb7d4b44c00219b50964484c1f5d6c8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 19:52:41 GMT
ENV _BASH_COMMIT=044c1acc91df168c9e9f1379b9a1ecc75d395bd3
# Tue, 24 Feb 2026 19:52:41 GMT
ENV _BASH_VERSION=devel-20260217
# Tue, 24 Feb 2026 19:52:41 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 24 Feb 2026 19:53:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Feb 2026 19:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:53:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfd90c62440ae151bea66cb9bc7d52e9b62bb083cb7dfc0147dee0cd6ee0bb3f`  
		Last Modified: Tue, 24 Feb 2026 19:53:28 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28fd3142d5912949af14be3747a8d5be87e67618e287abd410e40a2273039b4f`  
		Last Modified: Tue, 24 Feb 2026 19:53:28 GMT  
		Size: 3.0 MB (2953891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc02dc3142a5c529f355f6a60d49c9e93c174933ff9ebc9e63617833020c469`  
		Last Modified: Tue, 24 Feb 2026 19:53:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:f896d6222f1b8b484b774d64c894e5bc79ed5037bba96d5cee3dc3f924841500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7497c5a72cb384675a0edfd4a5192d9d801f549971e651fcea9ea46895b2b807`

```dockerfile
```

-	Layers:
	-	`sha256:55ab3fd511410e62a4a182e34749ef8daf90be619e4d99fec5462b7bfebf2383`  
		Last Modified: Tue, 24 Feb 2026 19:53:28 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c093a85c0bcba74f9ab4ff18f2477432b9f9068b46678c11630de57cbd14b73`  
		Last Modified: Tue, 24 Feb 2026 19:53:28 GMT  
		Size: 18.2 KB (18152 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260217-alpine3.23` - linux; ppc64le

```console
$ docker pull bash@sha256:1c203935220a8b1fe32d29a4acd5951fd0518288b2f7e970567e2c63d8ed68a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7167711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cdfe7967ef558725f8c8c837705796577f15dfec69f4b23e15477de3209ffb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Tue, 10 Feb 2026 19:57:01 GMT
ENV _BASH_COMMIT=044c1acc91df168c9e9f1379b9a1ecc75d395bd3
# Tue, 10 Feb 2026 19:57:01 GMT
ENV _BASH_VERSION=devel-20260217
# Tue, 10 Feb 2026 19:57:01 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 25 Feb 2026 02:22:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 25 Feb 2026 02:22:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 02:22:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Feb 2026 02:22:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d04bdf162acd8f02fd8e01f1f63735d877db356d8a3302e73f979a447498a21`  
		Last Modified: Tue, 10 Feb 2026 19:58:17 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f77619453a142a89dd5c7b993e7041be00995c3e229e8688d68797bf09150d`  
		Last Modified: Wed, 25 Feb 2026 02:22:50 GMT  
		Size: 3.3 MB (3337272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87ce155e5a938307f05bf5c74f40343afae90e5290c90cb4a5eb0950d20dd80`  
		Last Modified: Wed, 25 Feb 2026 02:22:50 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:abb6ebbed355670fadb2f91ce6d5c433224af896e817f241d556a9780d30c850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82e50a8029550c3fd9fea50ecd61736e3e3aa8043a5e8d0ab81ae661b323608c`

```dockerfile
```

-	Layers:
	-	`sha256:7d80540869125fbe84ccba44167f17ebf2b3a284a493ec1f481dab7f9262bf76`  
		Last Modified: Wed, 25 Feb 2026 02:22:50 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed80a7b85f67db913870f80c0237949714622958541e84443ab46ca31c45b400`  
		Last Modified: Wed, 25 Feb 2026 02:22:50 GMT  
		Size: 18.2 KB (18228 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260217-alpine3.23` - linux; riscv64

```console
$ docker pull bash@sha256:056420e9a697a4fd9551ecc61e96ae6f0b919c4a47d33dc9774b1e64dabfc476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a758aa51a9b458ec8e1754df38fd28fde8fd53a5fe777cabcb046898706b573a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 20:36:08 GMT
ENV _BASH_COMMIT=044c1acc91df168c9e9f1379b9a1ecc75d395bd3
# Tue, 24 Feb 2026 20:36:08 GMT
ENV _BASH_VERSION=devel-20260217
# Tue, 24 Feb 2026 20:36:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 24 Feb 2026 20:45:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Feb 2026 20:45:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:45:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 20:45:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f417a7be3c146d2c42c666ab79c82849f3b8de40d74e1a66ce079a295ea58858`  
		Last Modified: Tue, 24 Feb 2026 20:45:28 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f5ea7f8cd79d7cb81dcb38161255558d4599a68b2d23b9bd873a5cb02bfbc3`  
		Last Modified: Tue, 24 Feb 2026 20:45:28 GMT  
		Size: 3.2 MB (3217625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be71355d5852ea8aa4857ba654c52b7f608ab2b2aad158bce6002c925335434`  
		Last Modified: Tue, 24 Feb 2026 20:45:28 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:a92756daf2f384ea6c1132bdefcc6eaf5cabc3fe49a9e31da41a1b3251290a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0824162ff98ee7ce36eddb2b1956b914155df602ba78e40ab9125fad7d15867`

```dockerfile
```

-	Layers:
	-	`sha256:4983363b36050df200b1f3ee6a888d6a64b3e8fcfff88b5ac2ee55057ac38cc0`  
		Last Modified: Tue, 24 Feb 2026 20:45:28 GMT  
		Size: 116.5 KB (116501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0365a393e9c5fdbdcc5baac74699337dbca17746205846d361374ffb454bc95d`  
		Last Modified: Tue, 24 Feb 2026 20:45:28 GMT  
		Size: 18.2 KB (18228 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260217-alpine3.23` - linux; s390x

```console
$ docker pull bash@sha256:14bafebaf91ae77ca2d254da5e5dbb22854d0caa8b5a1f6fc84f0a493e1c7913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6845994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072dd34368ddb5c146e467d1bf42747233d92dd7e4f18dc5e598d11b8e717257`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 24 Feb 2026 23:30:48 GMT
ENV _BASH_COMMIT=044c1acc91df168c9e9f1379b9a1ecc75d395bd3
# Tue, 24 Feb 2026 23:30:48 GMT
ENV _BASH_VERSION=devel-20260217
# Tue, 24 Feb 2026 23:30:48 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 24 Feb 2026 23:31:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 24 Feb 2026 23:31:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 23:31:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Feb 2026 23:31:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1269f15567fcc26ce0143976bed809183d965c4bd335bfa1fa1ed50594af222`  
		Last Modified: Tue, 24 Feb 2026 23:32:10 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648feb37ca702845fc9f4f3a938b6e4d1efc186c74d049d3e69263dc6837b6cc`  
		Last Modified: Tue, 24 Feb 2026 23:32:10 GMT  
		Size: 3.1 MB (3119868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2a7f63fcbbb76574dc59cc0a7bcb9160b1bd4a5128db718611ecfb784f5819`  
		Last Modified: Tue, 24 Feb 2026 23:32:10 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260217-alpine3.23` - unknown; unknown

```console
$ docker pull bash@sha256:fa0b2498e78ca786cff60562db547b99c03198a6c6bfef4e744d870d411f8dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec7ce3cbca46c5832459a04e83f7f8b5ee4e3ac69d7c990d4f26d6d79158c92`

```dockerfile
```

-	Layers:
	-	`sha256:5cb7ef344b84e370365b9a50997754b854ed5ca9a8262fe9df9957a4fdb7ecf3`  
		Last Modified: Tue, 24 Feb 2026 23:32:10 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5724de04560b9fccd95a87464d5c74984574a9584c24d0672af9a065c5a09fa2`  
		Last Modified: Tue, 24 Feb 2026 23:32:10 GMT  
		Size: 18.2 KB (18183 bytes)  
		MIME: application/vnd.in-toto+json
