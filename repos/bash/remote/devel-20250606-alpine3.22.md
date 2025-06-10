## `bash:devel-20250606-alpine3.22`

```console
$ docker pull bash@sha256:ca8a11e205fad5905c2d838c7726784180d9aebe69d170f3ae57b3eb64a6de83
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

### `bash:devel-20250606-alpine3.22` - linux; amd64

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

### `bash:devel-20250606-alpine3.22` - unknown; unknown

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

### `bash:devel-20250606-alpine3.22` - linux; arm variant v6

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

### `bash:devel-20250606-alpine3.22` - unknown; unknown

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

### `bash:devel-20250606-alpine3.22` - linux; arm variant v7

```console
$ docker pull bash@sha256:e563fe592aa48d47eeeea43dd75a2956b6c5a9e32b9ec459808676e697a96f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6104539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f483fa6152279c6d04e68708cf767c0c1f485dfc663d81675f6a2d8ce02ece30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345f6f1b0ad8403dd591b815dacd505a425ee595bc14fce2a619c5013c072b72`  
		Last Modified: Tue, 03 Jun 2025 22:53:10 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5563bf9189bc9c5d2a536040e9168ae0fe301bad556797561bb5b805788c704`  
		Last Modified: Tue, 10 Jun 2025 17:48:35 GMT  
		Size: 2.9 MB (2884566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1fbad02ee025ac90ba5eb8e7a223605382c90cd08ea469e89ab6d3ab1f6448`  
		Last Modified: Tue, 10 Jun 2025 17:48:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250606-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:16f99e7a62241a0146fa663a463b9ab3b6e707e1a57ea53c31fd2d8eddacabe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 KB (136278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb054864f8512bddfd49cb2ba803cae6f41db09bb71dc8e35bc96ecf8bc4d5dc`

```dockerfile
```

-	Layers:
	-	`sha256:a8c90b16579901397844b7d04b40d707ae598ad197540e8bcbe1dbc15fb3a57c`  
		Last Modified: Tue, 10 Jun 2025 21:02:52 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ce5c1dbfbf0e95a6481981f30eec3617ab1a1b4b0ae4674634cf339fd54faa`  
		Last Modified: Tue, 10 Jun 2025 21:02:53 GMT  
		Size: 17.8 KB (17813 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250606-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:5f634d52fc4f7874ae15ccbc51245da5b6601b1b5f369a346d90dc07b0c62931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7221334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a41f6d081ba835f08ae2c2598868acc81cf4b8bab89d64150b70c78c4575ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4acd4ca2748e61184f091eabee480069c09f2f7bd94917e9f2f79e4e8dd086`  
		Last Modified: Tue, 03 Jun 2025 22:50:57 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9825fe70a07521b6aea53c6639ce9f4bf7fe22161c5f34c2c9c02bfa1b607`  
		Last Modified: Tue, 10 Jun 2025 18:14:44 GMT  
		Size: 3.1 MB (3084600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2425a2e8a9ccfc85dff93a28daf7a29cf16ebdc7fc19879e6c7d611f86870c7d`  
		Last Modified: Tue, 10 Jun 2025 18:14:41 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250606-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:c0d23615ba28b4ad8b96d607d4bb4d0a40b4d5d987178def87fca96e4a75c1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 KB (136326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce928416e4220763edcdde9ad5327ff876e2338cb7bad07b0296b08f2edc759`

```dockerfile
```

-	Layers:
	-	`sha256:a208bc61ba338b7328bd4a56fc03721f1289aeb986f6c643af00672618bac3ab`  
		Last Modified: Tue, 10 Jun 2025 21:02:57 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3905db791e9b72cf37c4ffbc67441dae8d6dcf5117a6b15b25b90b5dd446167a`  
		Last Modified: Tue, 10 Jun 2025 21:02:58 GMT  
		Size: 17.8 KB (17841 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250606-alpine3.22` - linux; 386

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

### `bash:devel-20250606-alpine3.22` - unknown; unknown

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

### `bash:devel-20250606-alpine3.22` - linux; ppc64le

```console
$ docker pull bash@sha256:251202dd5cb5b21d16bcb24afc636c33dafb043c5a598c59f1a7bf1353e06f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7003822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d6402b66fd6590a876ed439f811877cb9ccf2eb6d95273a0e7fa8fa5c96f79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f9d5d7928a8f09e32bb78bd4075729362bf942ce757b9dd4229425488fc06a`  
		Last Modified: Tue, 03 Jun 2025 22:51:15 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed42930074c0449ee842f337c533106b1dc58d12cc72a55d20cb5c1a60522fa`  
		Last Modified: Tue, 10 Jun 2025 17:55:00 GMT  
		Size: 3.3 MB (3272848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2d1dc76e550d5625978afa1d196c92cf931610c9887cc4455eed4c2b5d99c8`  
		Last Modified: Tue, 10 Jun 2025 17:55:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250606-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:11a12aff0cf81a2feb5f994f2b663cf02678125ee60c5933383bb071d63537c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 KB (134292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044d33a325730ef6a337784cf600626fa0263e7d425e018bb88880b2a5c6a89f`

```dockerfile
```

-	Layers:
	-	`sha256:6d2cbc0f8a13ee62da45cce63b1558ade52a90889c85572e3bc3ccdd91eb53eb`  
		Last Modified: Tue, 10 Jun 2025 21:03:04 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbfe81e6e8ff53ca2bfd260c098a2da51ac4f4fadee186e600fab64249336655`  
		Last Modified: Tue, 10 Jun 2025 21:03:05 GMT  
		Size: 17.8 KB (17780 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250606-alpine3.22` - linux; riscv64

```console
$ docker pull bash@sha256:bce4f8505af19a3ef46fc561cdab37585db3f74cf01ea40c42c20b863858d210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6459707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce02eadb27b5d337981fda1bd585fd6571fb62cd6c7a5d931807ddd0b411158f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825d9c7d21cff81f34ab6ed79c306ac7f740386530ff46f996e5d394f46f4626`  
		Last Modified: Tue, 03 Jun 2025 22:51:48 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c37033143d1287a57296173be23af12b06a64a234c8818ceb39ec1fc4e0a43e`  
		Last Modified: Tue, 10 Jun 2025 18:12:48 GMT  
		Size: 2.9 MB (2945100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998a232dd7d52bd6a575284a3abbf360497e137d5184bfed69eb4ca070e82d02`  
		Last Modified: Tue, 10 Jun 2025 18:12:47 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250606-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:54f628e2ce03768666f2c9629c5aae713b865cf914a4457440c95d7b93856492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 KB (134289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24f0c0bf05635dde6138467348a1fc0e41151492acf4e88b5182390c54c5a4a`

```dockerfile
```

-	Layers:
	-	`sha256:7590e5206a5ec6aeb1a776d389fb5c9dd4e51997c5a9eaa31da3013543ed6645`  
		Last Modified: Tue, 10 Jun 2025 21:03:12 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5bd02d40edc26d365fa296a49ef0b03f89b6fa49fae818478df2c6fe31eb4f5`  
		Last Modified: Tue, 10 Jun 2025 21:03:12 GMT  
		Size: 17.8 KB (17781 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250606-alpine3.22` - linux; s390x

```console
$ docker pull bash@sha256:494bf9b381d7785e9d5033ab4bb9997c19be4d6ba4bbf7e2ae5d850edac2d7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6742625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160624b555654179993459315e1fc1f8c762a368dce72350d03c7a3316a51d34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f709b1b5c7aa325170bdef132d7c3b3e6711de73420cc6a2de43a76dfc7deee2`  
		Last Modified: Tue, 03 Jun 2025 22:43:49 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dee650da84e8288728f05ef68a1a4265d1db2422bd8df8dd59ff0e8ba5c8c8d`  
		Last Modified: Tue, 10 Jun 2025 17:48:27 GMT  
		Size: 3.1 MB (3094306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ebc7a2f8a5f894767d2ec197b7e1d602f1a5fe3d51175bbeb4bc79bdde8024`  
		Last Modified: Tue, 10 Jun 2025 17:48:27 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250606-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:16bf5b5567048c5e24008d58a6d2d1cff43d8732ba21f1130629575d9ae5e0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.2 KB (134215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48ef81bd50c60a8741972c27a60168a2f7d2e40b958aefbe53277cc11106858`

```dockerfile
```

-	Layers:
	-	`sha256:e51d95028875c562deae974ca269db4e9f07086d0180030f85b59df05883afbb`  
		Last Modified: Tue, 10 Jun 2025 21:03:16 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56965366cba3359117d2706f38fb37a3a830c097870a8fdd30072b8bbc58758c`  
		Last Modified: Tue, 10 Jun 2025 21:03:17 GMT  
		Size: 17.7 KB (17737 bytes)  
		MIME: application/vnd.in-toto+json
