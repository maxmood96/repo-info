## `bash:devel-alpine3.21`

```console
$ docker pull bash@sha256:6092b8eb26ab7ee3f8049e82cf99f539d016b849c38d059f76df055fd24de899
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
$ docker pull bash@sha256:58bcdfc681afe048f66e0190a8db65e57af130b09f6373c044c0b3a7906abc54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6635524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5dc819bd6ac2c5cba82daf3e3dea4eb29b1e6f9db479b63f4af7f411345709`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_COMMIT=42c6cbd459a121e98d9ac43c477a5daf6c3d4f0c
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250409
# Tue, 15 Apr 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743fec78b88ece6a12d2278bb1e081e7ce244764cadc9e33d0f0d2ec8f01a836`  
		Last Modified: Tue, 15 Apr 2025 22:47:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0130f28c7949a1a3415536350b82207f3f42b0c5c352f606c24152aada79b63a`  
		Last Modified: Tue, 15 Apr 2025 22:47:06 GMT  
		Size: 3.0 MB (2992485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd72065d55cb0f2bc6268f173176eddf1266e4a8055a8ec468575c4274640b4`  
		Last Modified: Tue, 15 Apr 2025 22:47:06 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:0b3fe9d66999aafda46b3121c6b001d48fc369a4ac933a53c5f053d1f379ce19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 KB (132597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2957b6b4b74b118c8bbffd7a4fc02d6ab02e417a2953dc45cba801fd141f838`

```dockerfile
```

-	Layers:
	-	`sha256:2a7ea3d56f638197735a5c52b8319d568b6ff1971b6d20636abfe7ac4e29e156`  
		Last Modified: Tue, 15 Apr 2025 22:47:06 GMT  
		Size: 114.9 KB (114928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96fdd015f6d4f6959d65c74cc5bb7b4208020590394c5dffdb19d9887caafae4`  
		Last Modified: Tue, 15 Apr 2025 22:47:06 GMT  
		Size: 17.7 KB (17669 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm variant v6

```console
$ docker pull bash@sha256:5bb9353671a8e4c95b980fc41278967d4444c7e9621f17827a6bd47b570ff97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6293971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03eaf9968ea87a00228f9de38d308c7c9cf35c30a31e4ff6c0f7f735a47a293d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_COMMIT=42c6cbd459a121e98d9ac43c477a5daf6c3d4f0c
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250409
# Tue, 15 Apr 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
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
	-	`sha256:04f4178a6e4f36920137769c2f168315b3ed4734ad732f5e3a4da387106a7af3`  
		Last Modified: Tue, 15 Apr 2025 22:29:06 GMT  
		Size: 2.9 MB (2928444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5d328e8182ea147b47cc92e8d19065b8a4ca15ab64cfe845b0a93852fb4591`  
		Last Modified: Tue, 15 Apr 2025 22:29:05 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:d20436e9f215ef319719d5ce98fe922d3296f1f85b737226ed3efcdbc3ca8b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 KB (17530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c81df1b275ded7f5dfb7e4a9f14aa2b08d0c2a510945b75214e17b2ef93d3a37`

```dockerfile
```

-	Layers:
	-	`sha256:6972d58d20853650f8cbb8287d14d74b754a27886292a8f27c971825bc90c3bd`  
		Last Modified: Tue, 15 Apr 2025 22:29:05 GMT  
		Size: 17.5 KB (17530 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm variant v7

```console
$ docker pull bash@sha256:f42e8bdf5775db8136069a86e5903efe0f6d674c9c946941055f8c3823b4f2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5978541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d98396d94303d81c6657a1c23c4091bea4c2e0346c77dcf297d110bdad09fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_COMMIT=42c6cbd459a121e98d9ac43c477a5daf6c3d4f0c
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250409
# Tue, 15 Apr 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b71f74feee41903055522dcbbe45229fc23ca960d7e80c99f2747b60a0a3b1`  
		Last Modified: Tue, 25 Mar 2025 20:46:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7265c2ad14c83a730598373bef1968a953275cbcec3d01a7c269a10dda649fcb`  
		Last Modified: Tue, 15 Apr 2025 22:34:12 GMT  
		Size: 2.9 MB (2879624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393196504c0a2d128f4be7068fd438770c9186b5c705725434aec0d4fab520bc`  
		Last Modified: Tue, 15 Apr 2025 22:34:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:75e6a1874002f0b13ffce2862487d21544081be700473490c0a9ef383433d2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 KB (132709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:649b5dd805a2c482cfd17704d8c46556ce6468c5725e309d61f5bbae581bf9e0`

```dockerfile
```

-	Layers:
	-	`sha256:9f68df9b13e22a12b335c3b2ff7a180211b647e9c973e64d2b86dc1d46ee299b`  
		Last Modified: Tue, 15 Apr 2025 22:34:12 GMT  
		Size: 115.0 KB (114964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:934d87bf2496c2b3c21e81ab1f12b6aee6a76f8487b251e39cc1f002d6c07662`  
		Last Modified: Tue, 15 Apr 2025 22:34:12 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:52a5a03acd0c80217057389d6034e33524b0306085305c24dd76dd8705d60dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7073664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434a87bc524e0b60af154657380ebf681f6bd76af0b9b2c052fd0497d77fd2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_COMMIT=42c6cbd459a121e98d9ac43c477a5daf6c3d4f0c
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250409
# Tue, 15 Apr 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af32faa015356c0b2cd3b227fa97838bd58739b580d1b55a7c84292ea848464`  
		Last Modified: Tue, 08 Apr 2025 21:41:10 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1bf82ded47bc2dc1c815fa0e98f89fef9030c3502e5599fb289ffd71b95085`  
		Last Modified: Tue, 15 Apr 2025 22:33:56 GMT  
		Size: 3.1 MB (3079838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad073249e6843fceeb6516bd8ee9ba9409a1400ee2036b70da0a8ca47aa14062`  
		Last Modified: Tue, 15 Apr 2025 22:33:56 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:d130b10868d8850e52fe0dca53b28988c3a73e77b5050ec4b0436471c81c2676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 KB (132756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb7a57efc006cfe392902b1fb0a6099ea712db3f001103248685e38e762b717`

```dockerfile
```

-	Layers:
	-	`sha256:958ff35162b1eccf025938d4f8b66b902ed7906ee308d294080943be97f92ff9`  
		Last Modified: Tue, 15 Apr 2025 22:33:56 GMT  
		Size: 115.0 KB (114984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8bd56274330b6d78e3989d4e91bc61e92798161c35b56efb1deb7041f71fbc4`  
		Last Modified: Tue, 15 Apr 2025 22:33:56 GMT  
		Size: 17.8 KB (17772 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; 386

```console
$ docker pull bash@sha256:b724120db53659f9b8d1e3e8989bf12441cf5ae1964a8814dbb2d1319c0590c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6383948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f784a133292164aa26d07afb691df477d290d06ea84a38004e64f0053446bdce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_COMMIT=42c6cbd459a121e98d9ac43c477a5daf6c3d4f0c
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250409
# Tue, 15 Apr 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2289e867c3786714b54842297c9fcff5b10fb5baa760188770f97a979fa33a4`  
		Last Modified: Tue, 15 Apr 2025 22:28:45 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde72cdcb83d7ae1f0008e6997cc399b0acd135a38125f2232bc464e68cd92f4`  
		Last Modified: Tue, 15 Apr 2025 22:28:45 GMT  
		Size: 2.9 MB (2919532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac55452cd48ad95fcb2c78df2e7150650937fa6d8493bb47cfb0789cdda7ab3`  
		Last Modified: Tue, 15 Apr 2025 22:28:45 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:49f220a2f08ec9f9bb9b67c052213d5813bc76836d148df720e8781c934f7eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 KB (132540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c849cb005f5d969749f558ed3fea4985f6b83af39780ff1fcdd817a4b92a9259`

```dockerfile
```

-	Layers:
	-	`sha256:ba74e0c0ba0931fb43fc984ed1fd64dbbb696daa778a71f697ca20564f9bfa63`  
		Last Modified: Tue, 15 Apr 2025 22:28:45 GMT  
		Size: 114.9 KB (114903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d97578a0b439b32ae5c96a017a4b881c0e7ec6a62127ac656d0a8294fb961ff`  
		Last Modified: Tue, 15 Apr 2025 22:28:45 GMT  
		Size: 17.6 KB (17637 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; ppc64le

```console
$ docker pull bash@sha256:a76f2c45fe113221c2ea587d4418fd4a2896a6abab9946f7bea33cee013fa91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6843110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80ec341120d9903b23bca5860a242bcaba32b339dc09441bc4f7cb5e62d169a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_COMMIT=42c6cbd459a121e98d9ac43c477a5daf6c3d4f0c
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250409
# Tue, 15 Apr 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36049ca8d20b61234d6959e293fa53a0267e9cfd98d7f17f6c24ae271b006d4`  
		Last Modified: Tue, 08 Apr 2025 19:29:49 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2803d1bac0e6860593b8f09e51413ae1be3c16a85f788597a80f830ef10c2da`  
		Last Modified: Tue, 15 Apr 2025 22:41:35 GMT  
		Size: 3.3 MB (3267969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2f2fd79efc1caee92e1625f448c8ff0f184066d3f1e3e94596d19043a37577`  
		Last Modified: Tue, 15 Apr 2025 22:41:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:efb76fb1ed893e87dce6f092972ba1f457edd6ab316a9f360a37303514f15f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48451d7dc0fd1f5ed61176920b69ff585339f3558185480ff4060ae475def823`

```dockerfile
```

-	Layers:
	-	`sha256:4e62f0ad1682087812bfeb95b2e87c05a144637288d8e0b060ba3f82647652c2`  
		Last Modified: Tue, 15 Apr 2025 22:41:35 GMT  
		Size: 113.0 KB (113011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11170f32bf2801f7455cba4c07fabbd84ac1253c5f37341aa3758e066507f781`  
		Last Modified: Tue, 15 Apr 2025 22:41:35 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; riscv64

```console
$ docker pull bash@sha256:4d39c488b7a13fd745b441ca4a5674dc6127ac42c2b5077f48ad3ccc59e09573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6294375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5308dd14f565320b274ae9b8b9de45c2bf49654ac2692cb264675a10dd8727ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_COMMIT=42c6cbd459a121e98d9ac43c477a5daf6c3d4f0c
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250409
# Tue, 15 Apr 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
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
	-	`sha256:6c39de21d9c4e20a888a22aff2ace5f89ed51a6f61b6b2f1932615aa882a28b7`  
		Last Modified: Tue, 15 Apr 2025 22:51:17 GMT  
		Size: 2.9 MB (2942138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa65c9b142e44aec8e9251ce2b0b881b1198d718e07b804b205b62ed2a495350`  
		Last Modified: Tue, 15 Apr 2025 22:51:17 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:6a927024d293f56145f7697bc8349e6674997dc701f48eb6aa0849ef9f8b0b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 KB (130720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61fd439b2fff98abe13adc038e662c00132b6d3d40718eee74272ee8f3dd5ad`

```dockerfile
```

-	Layers:
	-	`sha256:a14b376aba1357f59565bbdc3bda9b98b130ac5dbab455a3d502e97b1ec6846e`  
		Last Modified: Tue, 15 Apr 2025 22:51:17 GMT  
		Size: 113.0 KB (113007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8429ccde663824edd268d518a1c15f95f293be5545955d046af715e2ad832390`  
		Last Modified: Tue, 15 Apr 2025 22:51:17 GMT  
		Size: 17.7 KB (17713 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-alpine3.21` - linux; s390x

```console
$ docker pull bash@sha256:8c823056d15c9506321b77ce9c4f115d881e5ca0b6ff3890dd638aa295fb633e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6557815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262b37a71d400bbe7daff77f4ad98b78456888752b24f4d4f1ee334ddd402be9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_COMMIT=42c6cbd459a121e98d9ac43c477a5daf6c3d4f0c
# Tue, 15 Apr 2025 04:18:04 GMT
ENV _BASH_VERSION=devel-20250409
# Tue, 15 Apr 2025 04:18:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 15 Apr 2025 04:18:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Apr 2025 04:18:04 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20ebcc118aee9f69754c83c44c7e1446bc00d1974545eb0c3248776bc32cd0d`  
		Last Modified: Tue, 15 Apr 2025 22:40:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce3dcb415f0d97fd16c1136c7a29f0e5e2222e2e62a32757554a0a61a71a9fc`  
		Last Modified: Tue, 15 Apr 2025 22:40:50 GMT  
		Size: 3.1 MB (3089454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1a7e5892a9208eb8786cd74540a46ff979e2ee48d8e388260fe92c08f130fb`  
		Last Modified: Tue, 15 Apr 2025 22:40:50 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-alpine3.21` - unknown; unknown

```console
$ docker pull bash@sha256:8f96d7488806aec43f507e515d6c057226f9f628b4e9f59a9d911d518be624ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 KB (130645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526dfee38c7c73b932b2e2d71d689d977e942c8d35bc1c83521592dead9d061b`

```dockerfile
```

-	Layers:
	-	`sha256:b5ee7cf15ad0cff1f45bbf00e546f9594fcdb4c731cba8b81e169a91405e1a69`  
		Last Modified: Tue, 15 Apr 2025 22:40:49 GMT  
		Size: 113.0 KB (112977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53ac7024b70d2e5e42a7d32b8a2698529adae4a4bdfa2da165c2f0a816b0d3ac`  
		Last Modified: Tue, 15 Apr 2025 22:40:49 GMT  
		Size: 17.7 KB (17668 bytes)  
		MIME: application/vnd.in-toto+json
