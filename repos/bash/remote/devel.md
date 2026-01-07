## `bash:devel`

```console
$ docker pull bash@sha256:49ca42cbab51d790b81f1343cd0e659931bfcc41d38e04828a85f51af5c8acd7
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
$ docker pull bash@sha256:3011712eb399787c8bc63ca9e826fbd6e594ce0995e4f31dfeb3009e85a2df4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6872119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12553a77ae467179fdb5147fee996998a8dd16e81e59071c29389f4e16af504e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Tue, 06 Jan 2026 18:51:33 GMT
ENV _BASH_COMMIT=a43e08df2deefa6b63dce66d57adad2c9a704eb7
# Tue, 06 Jan 2026 18:51:33 GMT
ENV _BASH_VERSION=devel-20260105
# Tue, 06 Jan 2026 18:51:33 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 Jan 2026 18:52:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Jan 2026 18:52:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:52:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:52:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f19fedc1845d1af562f2a498f815f640d247011f9f76212979767f0fffdd457`  
		Last Modified: Tue, 06 Jan 2026 18:52:21 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f1c7f64c2aa67a7cba438d83698381fdf9c3b3e334236674696b4dc3489540`  
		Last Modified: Tue, 06 Jan 2026 18:52:22 GMT  
		Size: 3.0 MB (3011222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7169bbf60d009bf75ba1d16dfac02500f4318bb258c37e80af17db8a9dd013`  
		Last Modified: Tue, 06 Jan 2026 18:52:22 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:92d75973f572ed731b6828e3f24fd01bf82b162ff9e81a70e62efb3ab0907f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 KB (135358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ecd4726ae3f9f68abb27d69c6bfa2cd1064a046e168737bef55a5cd13f69b5`

```dockerfile
```

-	Layers:
	-	`sha256:32df88cbe535a61efc38bdf910a9772c369e3556211714e0be6a6314306a2367`  
		Last Modified: Tue, 06 Jan 2026 19:02:56 GMT  
		Size: 117.1 KB (117122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8812fc3ddda9023c5cde509e7b91ed9b74b7773b1d87dc3fc136b5deb45458`  
		Last Modified: Tue, 06 Jan 2026 19:02:57 GMT  
		Size: 18.2 KB (18236 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:85ec2944a048a96dc0193e659dd68155e3e80300b82cb2584697daa29e3c966d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3559cae90cf599036f101c56762fddd048900a653a43555621aaafa094b933eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Tue, 06 Jan 2026 18:52:20 GMT
ENV _BASH_COMMIT=a43e08df2deefa6b63dce66d57adad2c9a704eb7
# Tue, 06 Jan 2026 18:52:20 GMT
ENV _BASH_VERSION=devel-20260105
# Tue, 06 Jan 2026 18:52:20 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 Jan 2026 18:53:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Jan 2026 18:53:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:53:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:53:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98efd09cf56449a836dcf6ef09eeed5e8701cce1a90b85e5af492e4dd3e9e4f0`  
		Last Modified: Tue, 06 Jan 2026 18:53:14 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c70725b50edefb4f6e26612277f9ee0ba96276905913c5050be88d73f8cd1a8`  
		Last Modified: Tue, 06 Jan 2026 18:53:16 GMT  
		Size: 3.0 MB (2972046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ebd97749084a3628758322a1d4d9022738bdaae11b1856456d26c561243160`  
		Last Modified: Tue, 06 Jan 2026 18:53:14 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f46e480eb1da1087a165413088a6584a9e965f94c0a1e00f289278949fdade29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 KB (18101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89de925e6b6ca425c34e186dee0911279182fceb89ac081b48d3d68b8f85a9d3`

```dockerfile
```

-	Layers:
	-	`sha256:024331f70854af8ee2ecfed9d6888a2917343e8ee6eb2127e9abc47ac09a1074`  
		Last Modified: Tue, 06 Jan 2026 19:03:03 GMT  
		Size: 18.1 KB (18101 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:d5f4038cf7ab2cb0f2a779fe64a41ef9ecd85fb652d65c4961c68ac6ace964b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6201624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2796f2bcbfda9ce59c6dd37619c4272cea80061188e02de98e5414a1bda3c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Tue, 06 Jan 2026 18:52:36 GMT
ENV _BASH_COMMIT=a43e08df2deefa6b63dce66d57adad2c9a704eb7
# Tue, 06 Jan 2026 18:52:36 GMT
ENV _BASH_VERSION=devel-20260105
# Tue, 06 Jan 2026 18:52:36 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 Jan 2026 18:53:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Jan 2026 18:53:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:53:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:53:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95541745099d2f71ecda351c477dc1928cd863fbb37a42ca846305ae7a14aece`  
		Last Modified: Tue, 06 Jan 2026 18:53:35 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7cbf3ba05087e17098ef6238e85504f29fd4ca4a846386db4412299d0de3b4`  
		Last Modified: Tue, 06 Jan 2026 18:53:36 GMT  
		Size: 2.9 MB (2921444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fedf808464b0fae5205b6803e0df5056f1e17f90cff97aed7178b0f8a56691`  
		Last Modified: Tue, 06 Jan 2026 18:53:36 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:35824ed3681bac9c0c0baca3e3183ced83831a43d04f052a4f4b7c638936914d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e3b9b2375989b6c3406eebd831c8b3f759874eb27178b4df27faac8af00a8a`

```dockerfile
```

-	Layers:
	-	`sha256:3b5600b554d391d7f98f3359584096ca3ba45f435caca7e5c4fe98d5c3929e8f`  
		Last Modified: Tue, 06 Jan 2026 19:03:08 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3e3f70de5e45c0cf1b034c5577b3f5c5bf3b8e06bc3cc54c4c0f8f4c4dac37`  
		Last Modified: Tue, 06 Jan 2026 19:03:09 GMT  
		Size: 18.3 KB (18316 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:33bb3ee7545a4afa044553369ecc739c3b1f8866e7394806264750df8c374f08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7275922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7d82b0329b372d1e274f9406b021d16120097b549259b44598259abaed241c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Tue, 06 Jan 2026 18:53:54 GMT
ENV _BASH_COMMIT=a43e08df2deefa6b63dce66d57adad2c9a704eb7
# Tue, 06 Jan 2026 18:53:54 GMT
ENV _BASH_VERSION=devel-20260105
# Tue, 06 Jan 2026 18:53:54 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 Jan 2026 18:54:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Jan 2026 18:54:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:54:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:54:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420354ec10bc3b67ee8fd09691c92a6a747489a743f516b06ee7331f278c1db3`  
		Last Modified: Tue, 06 Jan 2026 18:54:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30cb6e7380d0772e02414c914952eef2b9120ae0d85b148dae729c31d523db4`  
		Last Modified: Tue, 06 Jan 2026 18:54:52 GMT  
		Size: 3.1 MB (3079395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605acb92cd22e08e5831413dea8f4c6a573ca3d77398f26a7be0fc3e5da96a55`  
		Last Modified: Tue, 06 Jan 2026 19:06:00 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:5701adde0c55c68642a858859015e78f6ee2b866c8c8e52b25b800cf3603c63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 KB (134868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76e528d530bb6763b798c3be7d4d81bcb82c1479f583bfaec61da3383c102b84`

```dockerfile
```

-	Layers:
	-	`sha256:b72304437755e05b42a8f757b99f4416ec30de62d31755cab5e0f724ccc0dfaf`  
		Last Modified: Tue, 06 Jan 2026 19:03:13 GMT  
		Size: 116.5 KB (116528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656639e4255f2d902938fb67aa149f997e36b6f05236c2c8c27e7ad7f1e06f7b`  
		Last Modified: Tue, 06 Jan 2026 19:03:14 GMT  
		Size: 18.3 KB (18340 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:ad1a5c11205d71863da6ba212d262b5ee975c5ad2025036dcf2a2d1aba39e8a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7884dd27fadc2bea0d26fbd90009e564a00f3651355a006e8f54854200ebf9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Tue, 06 Jan 2026 18:53:21 GMT
ENV _BASH_COMMIT=a43e08df2deefa6b63dce66d57adad2c9a704eb7
# Tue, 06 Jan 2026 18:53:21 GMT
ENV _BASH_VERSION=devel-20260105
# Tue, 06 Jan 2026 18:53:21 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 Jan 2026 18:54:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Jan 2026 18:54:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:54:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e432c99602ca3db7d63f565fb1cc6898172aab75c6dbf6e618e26607960752b0`  
		Last Modified: Tue, 06 Jan 2026 18:54:15 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1cea5f54275ccd7b491eb4e40c192e2cc0f302d50af4ee65acd13bb3fb14bf`  
		Last Modified: Tue, 06 Jan 2026 18:54:15 GMT  
		Size: 2.9 MB (2940385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c217f38bab65e5756dd6b52b38dda2f7c2637fca490cd8efc72cb28a958a543f`  
		Last Modified: Tue, 06 Jan 2026 18:54:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a3d161bf72f651648cc0dde5a6b300118cabf4314d973b0eeac481111263bf78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b08b3ddbc1223e73acb7a3605c450a7d2ae52bfab56bccd55e651b4ddf89164`

```dockerfile
```

-	Layers:
	-	`sha256:a8b43622a3b87b8b204f46c40d40b104d539615668df13b74873b8716fcedfe1`  
		Last Modified: Tue, 06 Jan 2026 19:03:17 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ad8abd8f96a86358b1d5f7184cba1444be28fbe1ef4b483f47bf4108f2d32a5`  
		Last Modified: Tue, 06 Jan 2026 19:03:18 GMT  
		Size: 18.2 KB (18204 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:691c4c1af6bdae0110bb2abb55950e88ab48871e7f26ba0eec888508174d60e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7145023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d6e8d2f3f2da7f74fa02a5608e0f9502ee698d2763a17a51857fc3afc98ff1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Tue, 06 Jan 2026 18:58:47 GMT
ENV _BASH_COMMIT=a43e08df2deefa6b63dce66d57adad2c9a704eb7
# Tue, 06 Jan 2026 18:58:47 GMT
ENV _BASH_VERSION=devel-20260105
# Tue, 06 Jan 2026 18:58:47 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 Jan 2026 18:59:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Jan 2026 18:59:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:59:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:59:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:57 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66370ff64caff24f7cb3a649867d909a0786e73592e15d3a2290667f7d87ecee`  
		Last Modified: Tue, 06 Jan 2026 19:00:25 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929124e8547d00cc02c09fc8a58c8ba4eca29f68e5d68edc870231dca1f1f1c7`  
		Last Modified: Tue, 06 Jan 2026 19:00:25 GMT  
		Size: 3.3 MB (3316473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc476707ca563ecebfe4fa2ec34aa2bdba9137809b5a1d15c86c10d17ae3f80`  
		Last Modified: Tue, 06 Jan 2026 19:00:25 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1850d1a07972ef675748145add5f9e235d1d6c5c8b11c7e7d3c25127358eba21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f158af703175d9c1b349d9ab1ad1edd0eb980cc97bc1d88b6b1890879643278`

```dockerfile
```

-	Layers:
	-	`sha256:e9cf869c40030fda7e5821d8b1382073f3c2a97b9ab8680554da4172a2ed8996`  
		Last Modified: Tue, 06 Jan 2026 22:02:43 GMT  
		Size: 116.5 KB (116505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6667e065c1b7f203df03e0cb2e09fae78cb1e00e82b11d0e030bec86aaa92039`  
		Last Modified: Tue, 06 Jan 2026 22:02:44 GMT  
		Size: 18.3 KB (18279 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:123a1f9ccefc7eed6b6f7a6d6c2239104fe76318fb524684897988bcc5bfe229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6784348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd60c7b6480d1eb07e9abf4eade76eb5d8f78538b9a07e8146ee0d7256d402f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Wed, 24 Dec 2025 05:12:39 GMT
ENV _BASH_COMMIT=2cdb2f9b314525a118eff5237839ccc272c2e32b
# Wed, 24 Dec 2025 05:12:39 GMT
ENV _BASH_VERSION=devel-20251217
# Wed, 24 Dec 2025 05:12:39 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 24 Dec 2025 05:21:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 24 Dec 2025 05:21:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Dec 2025 05:21:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Dec 2025 05:21:33 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4513d4113afefc12d5002e33ef2b29b54dd17341532e87f1b9aba2c3f330253d`  
		Last Modified: Wed, 24 Dec 2025 05:22:05 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae171dce9b160bd5279a6952dc648c2472e7b2c31b54e65e82999a4a149f148`  
		Last Modified: Wed, 24 Dec 2025 05:22:05 GMT  
		Size: 3.2 MB (3199614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b75468e889e284723c6b215903b57bc4b1a67ddc97f2c39c44eefb9b308355a`  
		Last Modified: Wed, 24 Dec 2025 05:22:05 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:33cf92395a71be328f2805d02e09007f3d6eef48857f8261a7c0dc7e82dc0185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 KB (134900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e87687f59b81ec17fd75d118ee59e872b3eba1d5ecacf7c0e6d65bbcacb3009`

```dockerfile
```

-	Layers:
	-	`sha256:21620b5e1bdba187d1d04c7e8264c8a8332c86e0b0fca85571f9f3e87cd16f17`  
		Last Modified: Wed, 24 Dec 2025 07:03:14 GMT  
		Size: 116.5 KB (116501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e7cd3acb270bf18180eef5762e8c7aabde33e3c0c1ba4c263ed2cd76e082c4`  
		Last Modified: Wed, 24 Dec 2025 07:03:15 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:1928341de01f93fd864d7130553be4b69b533e504916bd410ea4e4481554b091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6827116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518dc36120a0bc3d2ce467267e34251b08a4820ca6ad22537398872e1357cab5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Tue, 06 Jan 2026 18:52:33 GMT
ENV _BASH_COMMIT=a43e08df2deefa6b63dce66d57adad2c9a704eb7
# Tue, 06 Jan 2026 18:52:33 GMT
ENV _BASH_VERSION=devel-20260105
# Tue, 06 Jan 2026 18:52:33 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 06 Jan 2026 18:53:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 06 Jan 2026 18:53:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 06 Jan 2026 18:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Jan 2026 18:53:10 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44787419c87ce7babdf5a9529a53f8c0397ae4d9d35fa8a814789863073a5d73`  
		Last Modified: Tue, 06 Jan 2026 18:53:24 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eecd3f0be4fb53eb2bd7c00d4d36e0b412f79a43a66ee11d6cbd1a1dfdf8495`  
		Last Modified: Tue, 06 Jan 2026 18:53:25 GMT  
		Size: 3.1 MB (3102011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7eb84de0f4af377a0cb6d993eb547daf71d88cb2d4331cbda42b92ddcb94874`  
		Last Modified: Tue, 06 Jan 2026 18:53:25 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:ab707795e028d31ea162e08291eae3ccb8ea648224cb92209d54062787f44760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25a8a8a796885dae455b761bcbcb2a9786488910fae10dd52925dd3c3947868`

```dockerfile
```

-	Layers:
	-	`sha256:30debe73290d0d3cda648a1181a1c626e3c84eab3d81385fe256286a24f10796`  
		Last Modified: Tue, 06 Jan 2026 19:03:22 GMT  
		Size: 116.5 KB (116471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31286324f832deef0a0c751642f65bf8d87ff66c7010e3644d7c140d8892ba6a`  
		Last Modified: Tue, 06 Jan 2026 19:03:22 GMT  
		Size: 18.2 KB (18236 bytes)  
		MIME: application/vnd.in-toto+json
