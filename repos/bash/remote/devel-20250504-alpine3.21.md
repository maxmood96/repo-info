## `bash:devel-20250504-alpine3.21`

```console
$ docker pull bash@sha256:a180bc25ef8f187d8cb569a87f4a185e4cc1a3646e98c074c6aa7164b4f83e45
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

### `bash:devel-20250504-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:d2378455f5b06ee3e6ee05966c61c3051926748511e4c6599501a5219abbf898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6639435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd303c46f22118d561ca37b51972c61d3bd85c5ba4c089ceedbad95fc07557a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_COMMIT=535a8150b65ee6888f54f602274dbbdcd77c788e
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_VERSION=devel-20250504
# Tue, 06 May 2025 10:18:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 May 2025 10:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 May 2025 10:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25816c60fc4b52ff713022c417471906ace69314fd8cc0c4c09ad04879166e78`  
		Last Modified: Thu, 08 May 2025 17:32:40 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d1b562c46ed6e69f4048fec5d41ea63ae806983a6824131ec94ad1f637178d`  
		Last Modified: Thu, 08 May 2025 17:32:41 GMT  
		Size: 3.0 MB (2996397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e5e2163b6bbd375187486e5aaf2a2df1883066832747760425d27cd34403cb`  
		Last Modified: Thu, 08 May 2025 17:32:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250504-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:840ead084d2967238f31c8db9b4b199fa29410d822b7c65f4877966778881928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32116b9dec5ff91d0dc3a87a7c022c986d146041d0679a488a8974da6285aecd`

```dockerfile
```

-	Layers:
	-	`sha256:464e256a71415eba5d974261a25b7866f14a7b51f8a3ebe00cc27312eff5d018`  
		Last Modified: Tue, 06 May 2025 18:35:41 GMT  
		Size: 114.9 KB (114928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68ef7783600de2ac2573dcc7b6eb089dba0122f7e953a3ccc26d46a570a02f6f`  
		Last Modified: Tue, 06 May 2025 18:35:40 GMT  
		Size: 17.8 KB (17756 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250504-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:847669bc06acb2f66ea357768426a09081a8d37bbe1d43bc17a408d92ffd0068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6297642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbefb065c484e4fc3cce4318e86bec3319c7aba2bb4705ba0d4acf771b4e8f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_COMMIT=535a8150b65ee6888f54f602274dbbdcd77c788e
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_VERSION=devel-20250504
# Tue, 06 May 2025 10:18:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 May 2025 10:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 May 2025 10:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f71d03b79647836cd876f54899ad58fcddbbb6e8b09ec300fc132bd64af9c6`  
		Last Modified: Fri, 14 Feb 2025 22:06:48 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0469302601ea0e406593b1441c64f8acbe9950297e3fcdda78cdfd6e680471d3`  
		Last Modified: Sat, 17 May 2025 07:43:09 GMT  
		Size: 2.9 MB (2932115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7877c66e5c34bc63c5e51614ef73830e911d5e0fa4755286b3f23f66017d51a0`  
		Last Modified: Fri, 09 May 2025 01:44:15 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250504-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:ca7e4756a24eb721c475f1b8c330f8ca49361723ccde1a99782b0386296ea2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86b7d47d2ac418b8a8289deaeaaa418a61cbd45d3e5aa7c3242058ff68e77b9`

```dockerfile
```

-	Layers:
	-	`sha256:35eb7b7bfc28cd61775a75664cf9b5634002fe6cfd89a1d4502022cd21bec751`  
		Last Modified: Tue, 06 May 2025 18:38:39 GMT  
		Size: 17.6 KB (17618 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250504-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:d2d6935704b6fd129f63d81f086b11f357dc37f1eeb6d1056cca6ec2e426d1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4f021ff739d7b8bde6845539830c1612df89efea06b0aa99de6f3c4b6fa6d59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_COMMIT=535a8150b65ee6888f54f602274dbbdcd77c788e
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_VERSION=devel-20250504
# Tue, 06 May 2025 10:18:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 May 2025 10:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 May 2025 10:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b71f74feee41903055522dcbbe45229fc23ca960d7e80c99f2747b60a0a3b1`  
		Last Modified: Fri, 09 May 2025 01:44:14 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ad751850ea39b98db6cb8e8e41ecf6cb632c62c37b84aa94975666378729e1`  
		Last Modified: Sat, 17 May 2025 07:43:34 GMT  
		Size: 2.9 MB (2882140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6bdf02f56190fc98f0d223afb5448010fd07ee25686b700b163436178d0c45`  
		Last Modified: Fri, 09 May 2025 01:44:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250504-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:3deefa56b1e0bb875deea2e010adb435e2c25607af4897fe3c04acf9eb51f37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5694f25850f5e85523ee1fca3709d7bb7ce40132a2b5f0d12926ae87dee75bb`

```dockerfile
```

-	Layers:
	-	`sha256:1ffd13826774440f7873e225fe0b37b500df15db0b0bb34b30167e0677014d56`  
		Last Modified: Tue, 06 May 2025 18:40:59 GMT  
		Size: 115.0 KB (114964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a86b6e2d1904b324b62444e0adb0f053b5cff84efdb1e671363797416755da0`  
		Last Modified: Tue, 06 May 2025 18:40:59 GMT  
		Size: 17.8 KB (17833 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250504-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:a6c6008bf09ff45ec46aa9c1931b4283024848a63b3985681faa3324ad3ce69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7076232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20730c95b60a86472959b676b7e07645c54360aa0c9d51a5df513599d47b75b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_COMMIT=535a8150b65ee6888f54f602274dbbdcd77c788e
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_VERSION=devel-20250504
# Tue, 06 May 2025 10:18:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 May 2025 10:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 May 2025 10:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f46bb25264bf2d21e412840d898d439bd2e303048a8d131f049fd47e15c1eeb`  
		Last Modified: Fri, 09 May 2025 01:44:15 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7714a0c9650329cdd46d1ae02c64e8b6878f85dccc0f9e4a9334c0b05c1173`  
		Last Modified: Fri, 09 May 2025 12:51:38 GMT  
		Size: 3.1 MB (3082411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236915756d50746bcfdddf73d1ecb56652cd1bb9894c6e99a7d4b517c2902e97`  
		Last Modified: Fri, 09 May 2025 01:44:15 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250504-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:70d0b3925985bf825f6c70481c5685f0473a28ac4adf0e1abf89178e422e8174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a145fec8018b7baa81a8e17cbf2143d5f75dd7f4e24035fc4f5a4c0fc934af`

```dockerfile
```

-	Layers:
	-	`sha256:afc2e6959cc33b4e81ac03a7af58b66cdf1ffd02e1a66b3917b8c6d5db546ee9`  
		Last Modified: Tue, 06 May 2025 18:35:37 GMT  
		Size: 115.0 KB (114984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a501fc0c7c6c498004e03cb588a21bbe213f390049a29df8803fb18a6e26eda`  
		Last Modified: Tue, 06 May 2025 18:35:37 GMT  
		Size: 17.9 KB (17860 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250504-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:b070f29f803c9d4f98fbc3f0dca1d9a3b16d8c0ceaefa3d1a283e7a98e15d14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6387313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95783bb7c3d0b658dd4cb9d427f30661cb7b6fdbe0d474b91edc613def1e906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_COMMIT=535a8150b65ee6888f54f602274dbbdcd77c788e
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_VERSION=devel-20250504
# Tue, 06 May 2025 10:18:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 May 2025 10:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 May 2025 10:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d262ba37aeaaa077dffa9bebc937538128287c6b6037ec6b1bbe08b4789e40e9`  
		Last Modified: Fri, 09 May 2025 01:44:15 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd0f5a7e6dda73a2e22083969bf48ac4f092246d42b1d5c3e92d383c5ea3c4b`  
		Last Modified: Sat, 17 May 2025 07:44:15 GMT  
		Size: 2.9 MB (2922895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92857d6e68c8bd2f2d75efad9e32e06f2ba4943dd53d40b22a5750cb414cc070`  
		Last Modified: Fri, 09 May 2025 01:44:15 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250504-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:136f39396a2caa3f080215b2d352399ad2891e770a978311acaa69bab1ec3c6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c82968e16c42014cdc590ceb068426ed507ccb680249b7d5b871a79bf53f1e`

```dockerfile
```

-	Layers:
	-	`sha256:0064f3dae406b2bccd7408f47f9b87749a2256fc1e131f2a99ed6a7ee261263c`  
		Last Modified: Tue, 06 May 2025 18:35:53 GMT  
		Size: 114.9 KB (114903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a83eec1900159422313e3a7bcf6f3a4c325838e2b8d09b2141184a838a90c4f`  
		Last Modified: Tue, 06 May 2025 18:35:53 GMT  
		Size: 17.7 KB (17725 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250504-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:a8ee07e3e1c4d07190e2a9be57106cb41a7ca4115ee8bc0bc6869a79f6e6e4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6846368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9289163798bb9fb9e8d0e2511bc9991b9fb0c11ce796ce87ec00aafb5d7a8d6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_COMMIT=535a8150b65ee6888f54f602274dbbdcd77c788e
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_VERSION=devel-20250504
# Tue, 06 May 2025 10:18:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 May 2025 10:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 May 2025 10:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d400c01bd14c64fd11d69a0922ddce95535ebc6421198af720e8fe591b191f7`  
		Last Modified: Fri, 09 May 2025 01:44:15 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df88ffba767f22267d38100e67f6c690e40f9150cb3de18bec8aa77762a3365f`  
		Last Modified: Sat, 17 May 2025 07:44:33 GMT  
		Size: 3.3 MB (3271226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6c62bc5bddd3db9ea63c84d890ee9819a443e052c95ac7dae81bc58a8f2bf9`  
		Last Modified: Fri, 09 May 2025 01:44:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250504-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:e4ef68d48e9e92729d839368715232b13ed97c9d877d5bb3326d1cf91b22fd3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34baa7dcbf9d384e56dbe496f2cdd55bcbeae2295d224efe46981692ccd8d316`

```dockerfile
```

-	Layers:
	-	`sha256:5f8364d1066e1afdfbb8adc65a2a69afd259fc3e9e064e678556b164014ff6c0`  
		Last Modified: Tue, 06 May 2025 18:42:13 GMT  
		Size: 113.0 KB (113011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08c899acc4d04f710206824eefeb6700b9a7e04b55a4f0c8eebef3350704ad1f`  
		Last Modified: Tue, 06 May 2025 18:42:13 GMT  
		Size: 17.8 KB (17801 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250504-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:fe702b4d65bb19d35b86ac54d8bd5d5202dcbb791f1ca276d0664ded8c478945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6296851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b3f691b7609d48e40a04ef7a91020043453cffbf1591f601c6c88349b8443e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_COMMIT=535a8150b65ee6888f54f602274dbbdcd77c788e
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_VERSION=devel-20250504
# Tue, 06 May 2025 10:18:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 May 2025 10:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 May 2025 10:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03589e78b235e506dafea1c4a2d73b5326f0580bc335cad463e8b5863a7e527d`  
		Last Modified: Sat, 15 Feb 2025 02:22:31 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f335e48f6114854a849195e2be8cb416191a2de34d8708bf826deb1ae226ec`  
		Last Modified: Sat, 17 May 2025 07:44:48 GMT  
		Size: 2.9 MB (2944617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8ed488e004a3130f9309bd3615895f02be0c1db8171cbc1f5481a92628c9c9`  
		Last Modified: Fri, 09 May 2025 01:44:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250504-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:08e7ef82d26486bc264386a7c7c743eb4bc6e662bfbde2f9d595de57e6389069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c54e5033fb4b0aa7c582b8a22206923aa4577f93217154aa909e0cce1d1052ec`

```dockerfile
```

-	Layers:
	-	`sha256:02b7ab5aae680cfd6d9143e4f36f382e8c0887a5b2e77a00f79cfab8e69ae23d`  
		Last Modified: Tue, 06 May 2025 18:43:48 GMT  
		Size: 113.0 KB (113007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe8c39dcd1d8fb6c3343eec0c6945092ed1c0cb4b45db98edc2ad7e58e55c40`  
		Last Modified: Tue, 06 May 2025 18:43:48 GMT  
		Size: 17.8 KB (17801 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250504-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:6db3219dfa8d07f39cfc43d5856283e1a7d967a8b65fb93235a76e73a0166301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6560423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4efd4b07135056f2d07d3d1ed99971cb2ccfdfb335655caa72d3c29d631ac4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_COMMIT=535a8150b65ee6888f54f602274dbbdcd77c788e
# Tue, 06 May 2025 10:18:00 GMT
ENV _BASH_VERSION=devel-20250504
# Tue, 06 May 2025 10:18:00 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 May 2025 10:18:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 May 2025 10:18:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 May 2025 10:18:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f46b3744fb8a924c16ec91cd49f225382e9dc9803fbf9234c27869110fede6`  
		Last Modified: Fri, 09 May 2025 01:44:15 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e4c32e98936de4d3e41056197134b324986c20845d594db193c007b1ae5d93`  
		Last Modified: Sat, 17 May 2025 07:45:12 GMT  
		Size: 3.1 MB (3092064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c88c6b87c499c74cb8c9e051cae1a76b347b7b52a7aeffc140b954b1dfdd97`  
		Last Modified: Fri, 09 May 2025 01:44:16 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250504-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:0a95b6bdf126ef8089d2fc0a70a57a3dea864790f4afeddc25cde1a0cf6de22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c955584391993727b3f3700da2b8e5ce6b5615e93db94071072b701d625794`

```dockerfile
```

-	Layers:
	-	`sha256:1e4232a3ecc77953a57a5e3d9c407de8feee98d8e41c1396b7950a7341528388`  
		Last Modified: Tue, 06 May 2025 18:36:55 GMT  
		Size: 113.0 KB (112977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99fded6592274372008526cb6e311a7c6e325304dbc4e792c6833d510f526546`  
		Last Modified: Tue, 06 May 2025 18:36:55 GMT  
		Size: 17.8 KB (17757 bytes)  
		MIME: application/vnd.in-toto+json
