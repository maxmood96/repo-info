## `bash:devel-20250224-alpine3.21`

```console
$ docker pull bash@sha256:243c40f2cdbc9b157149c59d9458530b65dc125a355d0644efedd7169a63b53c
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

### `bash:devel-20250224-alpine3.21` - linux; amd64

```console
$ docker pull bash@sha256:6f3eda06d7818524e4db0aea2de2ffa202f0ca41e5435e0bfc17b1c838609dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6599728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158170e58f98a8879c3acc80d0c7acfe0c699cded1ed16def4c4bfa0ce364322`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_COMMIT=e608233770b0ba5fe20cb46842992b64f7252383
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250224
# Tue, 25 Feb 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22039adc0f58af333a10bf767c61429a7f62538e22bde060bb906d62766d382a`  
		Last Modified: Tue, 25 Feb 2025 23:28:09 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ead60e9b0a66370f4375c3d852092044182519dbde685f6aef1dc9f22f2146`  
		Last Modified: Tue, 25 Feb 2025 23:28:09 GMT  
		Size: 3.0 MB (2956688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb97610848fab30afad8a1faaebfa167819de304526ff7fb6b8260c3e21db30`  
		Last Modified: Tue, 25 Feb 2025 23:28:09 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250224-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:9a5fa6e23b4c9e2d46deef9c22608f388c45a2ee870c1f2c7f1d56826d80c374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64b35b8740677dea55e9d2937ff95563c2d5fc01366905b8c76bdaefb007f92`

```dockerfile
```

-	Layers:
	-	`sha256:0287a54ddb20b244c1ab14ea1cd0266d8dfa17d8cb4149f76edfe4be0009cd44`  
		Last Modified: Tue, 25 Feb 2025 23:28:09 GMT  
		Size: 114.9 KB (114928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a12af3ada29a40184e3502ff1134062bdc60af623d78f35f4953e822881b066`  
		Last Modified: Tue, 25 Feb 2025 23:28:09 GMT  
		Size: 17.7 KB (17701 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250224-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:d70bc86754a5411963adaa5ac0ff84e4080f8d5d0a85b7b5e1b05fb04cbf77da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6257759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22edf3cc358ac6642ded58125fffedf7860e05c81e76cd891799e2cacbe86699`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_COMMIT=e608233770b0ba5fe20cb46842992b64f7252383
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250224
# Tue, 25 Feb 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f71d03b79647836cd876f54899ad58fcddbbb6e8b09ec300fc132bd64af9c6`  
		Last Modified: Fri, 14 Feb 2025 19:17:59 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31c382361648d52cf18ee7a8bad5bb7d3d144abcf762e71f70792c77e5ff0a5`  
		Last Modified: Tue, 25 Feb 2025 23:27:55 GMT  
		Size: 2.9 MB (2892236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9960e177511132de7f26b96d5f0f7343ba37ed3f95833bb876f55134ebe6533c`  
		Last Modified: Tue, 25 Feb 2025 23:27:55 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250224-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:2cc972439af1f0db980d31d00d3db577b5822f293b442c25fc07eefc9defbaae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 KB (17562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4185ddddb71c4e0403c755f466d07eaef866b9499106528ed534a84c92676129`

```dockerfile
```

-	Layers:
	-	`sha256:db7e13c5164d755b155f50e3a524990184b516af7fefb408603fc0906e13b6f2`  
		Last Modified: Tue, 25 Feb 2025 23:27:55 GMT  
		Size: 17.6 KB (17562 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250224-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:48e062a2a0d3937fcd36f8efb5a48d40441c78851d2b6777ac34cc667016844e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5944224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c09b803809839f93451c13f35ada5eb28958022767664fb8a688e6e979c682`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_COMMIT=e608233770b0ba5fe20cb46842992b64f7252383
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250224
# Tue, 25 Feb 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd3e75f2624dd38c4e78a673875c24e5c4ddb5c41b2a1d512a5bef4426fe483`  
		Last Modified: Wed, 26 Feb 2025 02:51:03 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a31746f93987e27bddfd150b39c337171bbdb95c547de3be43d84f7362882e`  
		Last Modified: Wed, 26 Feb 2025 02:51:04 GMT  
		Size: 2.8 MB (2845311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535a55ab065604e2ba62133580eccf60654f5e4387fc22879d983de4b156f737`  
		Last Modified: Wed, 26 Feb 2025 02:51:03 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250224-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:85ef905a897dec759e1656c9fda26bac25b0a503ba3fe2e3e3ae7b98a7c999ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f73d40f3600bef20c381a5c65b2cdf5ccb5dd436e8c86724ea4746c5b0a013f`

```dockerfile
```

-	Layers:
	-	`sha256:10e6cef4baa11a08207ba10df890791d9b2f226c21e85156ef6516e0c9a04439`  
		Last Modified: Wed, 26 Feb 2025 02:51:03 GMT  
		Size: 115.0 KB (114964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129edd3638940fa13381e25e011af5f197171d84faa9a3b6e595bd998be32957`  
		Last Modified: Wed, 26 Feb 2025 02:51:03 GMT  
		Size: 17.8 KB (17777 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250224-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:341ea4a53d4a8dad1cb20364349787f2bf77d3b9ff0bceac2624eeaba4aeccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7037567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3315dacb59c4cc7658015edcd6137c193da65a206ba1ad112bbe419079041f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_COMMIT=e608233770b0ba5fe20cb46842992b64f7252383
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250224
# Tue, 25 Feb 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3d502bb651671c19c8b3efd13b26616ab4951c4f20dafbe31bdd3e48035f5d`  
		Last Modified: Fri, 14 Feb 2025 19:17:30 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217adf572143dca266406ba35996f2a56b82f1d628d74c7c111a08c607c674e0`  
		Last Modified: Tue, 25 Feb 2025 23:33:36 GMT  
		Size: 3.0 MB (3043747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c079d3d5dbd2ebd7a57a7169cc833bde0b71f771c0ce90a2b3046ca4ae9f46fa`  
		Last Modified: Tue, 25 Feb 2025 23:33:35 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250224-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:08c873cc8188ad8cc3003445e62be93a2e26a71396b82a094c0090b29de1571c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2e0e2a45aa4291eb90e5842a4b5ba6d585d8a540b129ad6c73c49e66483b3c`

```dockerfile
```

-	Layers:
	-	`sha256:c81d65dc571e8585242587b6872924a947447c4e0bbfece5bed3db13e130bcd3`  
		Last Modified: Tue, 25 Feb 2025 23:33:36 GMT  
		Size: 115.0 KB (114984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f2ad388dbd77fc68cf93ac02d7e8f6734fe365799dedf121789e7f5e3d9a8a`  
		Last Modified: Tue, 25 Feb 2025 23:33:35 GMT  
		Size: 17.8 KB (17804 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250224-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:408daeeaddf7008d694235fcbd90f762309f836236537a6268c741280465bc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6348649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2054ec6bb12d6f47362a91437194acc51ab887296571a63f022ae4e5d280b3f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_COMMIT=e608233770b0ba5fe20cb46842992b64f7252383
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250224
# Tue, 25 Feb 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2135f97a18496b5c0fa4066f9ea4244b7f92226e5406144eadc5542f1a65d0`  
		Last Modified: Tue, 25 Feb 2025 23:28:22 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99db244f5ebc3ca4fce3a43a7e514b54b851cb41225d13496bdc34959b307172`  
		Last Modified: Tue, 25 Feb 2025 23:28:22 GMT  
		Size: 2.9 MB (2884235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a016764df387b5c6ef3e4c4babda1e59d6bc95b68c15ec37b462b3ea378f927`  
		Last Modified: Tue, 25 Feb 2025 23:28:22 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250224-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:41b6e36165131a377b373562f026dd8bdad90eab2ff4d93b5f576dde6be4656b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7b3ba75dcd20c8e76e628c6fa6c84a910b409a9c8edffc00b64aa5cc9ede7c`

```dockerfile
```

-	Layers:
	-	`sha256:0459fdb0c7cc6bea0dfbe58847a7fa6e43c0d3a5392fcaad793ab28c01b5252e`  
		Last Modified: Tue, 25 Feb 2025 23:28:22 GMT  
		Size: 114.9 KB (114903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96730a5dcc91090d09cf8c2af07ffcd6c59eba35c894dd7edd3d7adc93d82a1`  
		Last Modified: Tue, 25 Feb 2025 23:28:22 GMT  
		Size: 17.7 KB (17669 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250224-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:cccf33d4b4696cf1f9034cfccc509bc2eaaf9aaf7541dc80958776ce75f2e642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05ccd05a26d155d3202d1c412439e455a8d4b89318a9f045028196279b1447`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_COMMIT=e608233770b0ba5fe20cb46842992b64f7252383
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250224
# Tue, 25 Feb 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0386798110616d77db41de4a2d80786fdc3f26815e48c70d0cea5c4dee3b7b4e`  
		Last Modified: Fri, 14 Feb 2025 19:16:02 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c412fa2e416fa6b2799354b6ba2e0a9290c73c9f3fb80ccfa360319d80b2ab80`  
		Last Modified: Tue, 25 Feb 2025 23:28:13 GMT  
		Size: 3.2 MB (3228819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee4f85f2236a0e001321891b634afe7151ec4ec3165beb8451fd4a8c76b8d82`  
		Last Modified: Tue, 25 Feb 2025 23:28:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250224-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:d6b21519f6413ac7c8d2bef47336e45f03225396293472f8d3d87114f2795233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a5fc8f41c0030fa813849bace5cc0bd3262a6e7b89447ab301ae4130b9aab8`

```dockerfile
```

-	Layers:
	-	`sha256:2f56f21ed4c3890c5516446d391c629a462e3ac507481a51fd75c42e5726bcc4`  
		Last Modified: Tue, 25 Feb 2025 23:28:12 GMT  
		Size: 113.0 KB (113011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f092b0d262b1a285ea907bab4dd369007fd17d8d2e65c6ae71e734dda04382d5`  
		Last Modified: Tue, 25 Feb 2025 23:28:12 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250224-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:3fab530a872492fc7635adc619f4a652c4fd9d6a05989c113e758f2e7e4d9dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6259467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8286d6b1abd85214e4628ba9f59688015bcb91da8245aa5843c97672977476a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_COMMIT=e608233770b0ba5fe20cb46842992b64f7252383
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250224
# Tue, 25 Feb 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03589e78b235e506dafea1c4a2d73b5326f0580bc335cad463e8b5863a7e527d`  
		Last Modified: Fri, 14 Feb 2025 19:22:45 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30c67cb712d4f24fa2dd000a46d7f89abb4b7ea5b66a265eee8b395d1e9f545`  
		Last Modified: Tue, 25 Feb 2025 23:37:34 GMT  
		Size: 2.9 MB (2907232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de5cef920d99201d9187ada380b3713ade565aef588da31e0129acdab4b7c4`  
		Last Modified: Tue, 25 Feb 2025 23:37:34 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250224-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:d8c4e8b761f8913a8227760e0f91e15b14f8e20f7a61bc09ad30228efc580cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.8 KB (130752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8913af52b19dc9fe387d5cc65b548dc85681c3d6adab6994fa3ca7658a9b3149`

```dockerfile
```

-	Layers:
	-	`sha256:5e28281b3dd00e49cc7d2bbbe9cd1b0187ef5c0e016508befad9223a401a327e`  
		Last Modified: Tue, 25 Feb 2025 23:37:34 GMT  
		Size: 113.0 KB (113007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a260b1c3f199c2331c85f00de58647689d9e9f8040653270fabf743981a279`  
		Last Modified: Tue, 25 Feb 2025 23:37:34 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250224-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:d82401e227bc8220168e8d146969b278a8d9e77bb71eb98cd52f625108b0d6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6522230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e840a287c6c8e2a6e614ba2d17b5277ca8afc61d2ddfbd1f84ff617cca7c900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_COMMIT=e608233770b0ba5fe20cb46842992b64f7252383
# Tue, 25 Feb 2025 05:18:08 GMT
ENV _BASH_VERSION=devel-20250224
# Tue, 25 Feb 2025 05:18:08 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Feb 2025 05:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Feb 2025 05:18:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df36b3281700d2604998143a2e08360f4a5b865d77d9cf513bacb1e08fd48d24`  
		Last Modified: Fri, 14 Feb 2025 19:12:07 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0ced6239b3356feae2eaf0d4fc717208e6152c602c798a450dfad9e4268815`  
		Last Modified: Tue, 25 Feb 2025 23:27:39 GMT  
		Size: 3.1 MB (3053873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba0b9cb27e7b6689fd7d80ba97c29cd487b9419c287ffd17bedf268fae2b64d`  
		Last Modified: Tue, 25 Feb 2025 23:27:39 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250224-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:b6ca8ce43ca8557d031c68d528e2563fdb61a449cae6e2ca65c94055d6c7f13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29e9deb3fa7d4780c02bad60264984b1dd680df168519589f3cd63e3d05d577`

```dockerfile
```

-	Layers:
	-	`sha256:d0cf9036562fee8f73e68da9426314cd7d660f5ee08996c2bfc918d641ff8494`  
		Last Modified: Tue, 25 Feb 2025 23:27:39 GMT  
		Size: 113.0 KB (112977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74a5f77d28e1a0873a175b1fe0fd186ffd8146f8612dc9d4b229c846d687e7c`  
		Last Modified: Tue, 25 Feb 2025 23:27:39 GMT  
		Size: 17.7 KB (17700 bytes)  
		MIME: application/vnd.in-toto+json
