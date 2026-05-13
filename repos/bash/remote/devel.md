## `bash:devel`

```console
$ docker pull bash@sha256:79fb7f0efc067273f3b8312c1e82956d15b16e43353c5fa39745a1bed02cc381
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
$ docker pull bash@sha256:0086ee28b35b5eb712b886d66b4516b8d50d97a8c0fdca1efec8842d0b7bc487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6893445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a17f7267be0a5376f435d9811035c39325e9e2bb47c4617dc99cf27b2df4ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 22:31:28 GMT
ENV _BASH_COMMIT=669b32f676a102193f65dcf88b98ba40bb361996
# Tue, 12 May 2026 22:31:28 GMT
ENV _BASH_VERSION=devel-20260508
# Tue, 12 May 2026 22:31:28 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 May 2026 22:32:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 May 2026 22:32:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 22:32:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 22:32:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1e24731c32542b7f05ceba9714a0cf48823726d7c6b3c398b553eafa66839d`  
		Last Modified: Tue, 12 May 2026 22:32:08 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0ebcf3e1c502bcf93ef07ea029ffa958f3594e7004d0f6199301694775d9a7`  
		Last Modified: Tue, 12 May 2026 22:32:09 GMT  
		Size: 3.0 MB (3028464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7280b220e47203f1d1e9433409a9333110627572c05e5cc68c73cd4573b21e81`  
		Last Modified: Tue, 12 May 2026 22:32:08 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2d7dcf002783c9d00090632e7d2b2eb48e92f4e8c636b1b916d0c403be00d34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 KB (135078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7960acc3b9a1b2f66dbc25f8ece76a9cef11a4a66d9dc63a14902df66ce13fa`

```dockerfile
```

-	Layers:
	-	`sha256:0414ded6e222b38d9b47b91b81d634e49e72bd558adb66cadb53f7a79a8a88dd`  
		Last Modified: Tue, 12 May 2026 22:32:08 GMT  
		Size: 117.2 KB (117150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45cd921c23ef08db1993f6f397dff953dda4657e742e9bec0fe849c98cc7b8d9`  
		Last Modified: Tue, 12 May 2026 22:32:08 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:7bea4041717d21b57aeecf20cbe5d2a7c6666c62e3a7acbcbd69dd3c34b3c231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a845ee4152952854bfebfbdba3b3225df9b489b68f885feee818b565a403542`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 22:31:19 GMT
ENV _BASH_COMMIT=669b32f676a102193f65dcf88b98ba40bb361996
# Tue, 12 May 2026 22:31:19 GMT
ENV _BASH_VERSION=devel-20260508
# Tue, 12 May 2026 22:31:19 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 May 2026 22:32:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 May 2026 22:32:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 22:32:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 22:32:02 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1dfcd8466afb809e81bb8bf6380b5f44cbc91b8c9a6e668d68d6e8be8c7f28`  
		Last Modified: Tue, 12 May 2026 22:32:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9cb455e35ce015f9ec93f2b8b7e1ba429cf417ac7196d3f0640a0648bb09f8`  
		Last Modified: Tue, 12 May 2026 22:32:06 GMT  
		Size: 3.0 MB (2987212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469edf809c9eb419e80382fc4d0ca854c2b5b730dda37860077f1d9935fd4360`  
		Last Modified: Tue, 12 May 2026 22:32:06 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:39a6c1c2c8f82f978861a6c0859c6e08721a947fe44ec36299f7c111a156f58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 KB (17793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3c331abe76bc065ef043ecb8212807c445895e8e43e28a0668bb597f1dde29`

```dockerfile
```

-	Layers:
	-	`sha256:67f7facc7c1c4b6864939517d853476816524ee16b2754ff2ffe9bcc3bd7881e`  
		Last Modified: Tue, 12 May 2026 22:32:06 GMT  
		Size: 17.8 KB (17793 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:48cc46d0d6dedfcef1849011ccd1a5cce9a3f5f3edcb7495b4f2aa538f8dabd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6220895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380f7eaa98df34e877e1cfd0231b62394b5f6e3a6234c545c2ec1c7bad8b4b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 22:31:22 GMT
ENV _BASH_COMMIT=669b32f676a102193f65dcf88b98ba40bb361996
# Tue, 12 May 2026 22:31:22 GMT
ENV _BASH_VERSION=devel-20260508
# Tue, 12 May 2026 22:31:22 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 May 2026 22:32:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 May 2026 22:32:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 22:32:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 22:32:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda981cf22562cb6ad72f226c4a0b326e5883331444a66f72da09d8f2ec3f03a`  
		Last Modified: Tue, 12 May 2026 22:32:12 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3adbad5ccff0083849ab60a850c5a59e3ed40a18f932f7a99855e7d41c0bfc`  
		Last Modified: Tue, 12 May 2026 22:32:12 GMT  
		Size: 2.9 MB (2936982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7ad8d4de9a8da8463a019aafeda69fbf9b7fdba4f8ba16d39741daf532aae5`  
		Last Modified: Tue, 12 May 2026 22:32:12 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:562e513e839e8f6987658a826420c8457b7865ee75b51b6ef6acf836de2996f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73895dc23f0ea9cecc16b073462c945c631357c7d33c82dccde88e368b45b7cf`

```dockerfile
```

-	Layers:
	-	`sha256:b18cb4f5d430f9da0e2812618b55935bbf88c61fb4e39248e067d6c60f5d6bdb`  
		Last Modified: Tue, 12 May 2026 22:32:12 GMT  
		Size: 116.5 KB (116536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:092e76c7f62d3ec6ac2af40d96c93f18723b21c63370dcedb247f71374bc0b5d`  
		Last Modified: Tue, 12 May 2026 22:32:12 GMT  
		Size: 18.0 KB (18008 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:d442c8a1990d2f515c0d3768795756af265c396d16b632efcfe088a414715dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7298615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a777cc96f9b2f284205239c93382319cb48aa2d0500b6ff65ad82561d6cf8ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 22:31:22 GMT
ENV _BASH_COMMIT=669b32f676a102193f65dcf88b98ba40bb361996
# Tue, 12 May 2026 22:31:22 GMT
ENV _BASH_VERSION=devel-20260508
# Tue, 12 May 2026 22:31:22 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 May 2026 22:32:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 May 2026 22:32:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 22:32:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 22:32:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816bcb1d1ccd50c55e60fab04dd62b8855cac8c9de5bfaa4de043953c7d8ad38`  
		Last Modified: Tue, 12 May 2026 22:32:09 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16165860bf73c4ca223c9036ef41bc53d6eb50fdba95e93737b8aecb825c8af2`  
		Last Modified: Tue, 12 May 2026 22:32:09 GMT  
		Size: 3.1 MB (3097955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4932cb60fdc24f977901f46d2a2d3a4269a927efd2a51fca49b54467b238fb74`  
		Last Modified: Tue, 12 May 2026 22:32:09 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d5ffdf9290180abb9de4552d0a0a9d188e18d8b570509be6313d86ccd585dffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268f8512d539f66cf894899d312a4ca4524784dca497efe47b5bfe525de87ad4`

```dockerfile
```

-	Layers:
	-	`sha256:04667c47cd028c48a651cfd4e98e22446c468d1d46e6b840fba2bd7d1717fe84`  
		Last Modified: Tue, 12 May 2026 22:32:09 GMT  
		Size: 116.6 KB (116556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdcfbcea503890c916a76efdf2df99094ae665233b861f1b3ad87ce50ee7aa54`  
		Last Modified: Tue, 12 May 2026 22:32:09 GMT  
		Size: 18.0 KB (18032 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:935c1d08fd4c97a2f040619d85cdbe49eff64263acbc0e67417d31c54c61f7ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6646667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a34906229f84e8c1abe2866253adc7d649b7e7d9f5ded39f59dcf7d16bdb8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 22:31:49 GMT
ENV _BASH_COMMIT=669b32f676a102193f65dcf88b98ba40bb361996
# Tue, 12 May 2026 22:31:49 GMT
ENV _BASH_VERSION=devel-20260508
# Tue, 12 May 2026 22:31:49 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 May 2026 22:32:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 May 2026 22:32:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 22:32:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 22:32:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c56188af701100733b81dccb3953bccccd1e608546d4913a7f1fcadc0dba5c5`  
		Last Modified: Tue, 12 May 2026 22:32:32 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0bd5f98dcb4c332c96c593a8981fa6157b60b39369e0a5ea39450db06a276d`  
		Last Modified: Tue, 12 May 2026 22:32:33 GMT  
		Size: 3.0 MB (2955427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08fbc412e76b806464cbcb4f31debd23667516c3f65bb1d97a6a43407d2b2df`  
		Last Modified: Tue, 12 May 2026 22:32:32 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f7b10ce661440fb1d6e2c26986e468c0fda3c005f1cfb7358e67565616af6381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 KB (135021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03f19b9eafe20215564c7a84488a2b3a6a9de681f2dd1972218965bdc188fb5`

```dockerfile
```

-	Layers:
	-	`sha256:bc1b25d6e13a239180c0b5ee19a354dd235e03110c1a8a4957d1b198734be6d3`  
		Last Modified: Tue, 12 May 2026 22:32:32 GMT  
		Size: 117.1 KB (117125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dee5a32b02dd83b53f6168259954794a421c37f274c875c03a3066888165557d`  
		Last Modified: Tue, 12 May 2026 22:32:32 GMT  
		Size: 17.9 KB (17896 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:28abbc1a10f092580f5f5439dfc76ca57cdf4bb409220e911a5bf34ad3eca4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7170320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ed7f380cb286e86cb9678ef669f9aad088ec388c35ce7c2e94fec59246e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 22:30:46 GMT
ENV _BASH_COMMIT=669b32f676a102193f65dcf88b98ba40bb361996
# Tue, 12 May 2026 22:30:46 GMT
ENV _BASH_VERSION=devel-20260508
# Tue, 12 May 2026 22:30:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 May 2026 22:31:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 May 2026 22:31:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 22:31:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 22:31:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bcc61c5f0e18ee418d14a81d01dc231bc1c4f28c83fc865c9117901c1c21d54`  
		Last Modified: Tue, 12 May 2026 22:31:58 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2eabc27ea3265696f2dcd0e873f4b6d1c103028a9b8b9ddd3627a2a32e154f`  
		Last Modified: Tue, 12 May 2026 22:31:58 GMT  
		Size: 3.3 MB (3338600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b69f4bf00d5fe95a390e140b2f0e4b464d93d52059ee459c92781732ba86629`  
		Last Modified: Tue, 12 May 2026 22:31:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:cf8f776b583956fc06fab23e347898c528ff9479d9c82ef8d81247b03c6f8735
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a8214f3e489e642546b55e19e20587ca20f6ea44c1f466df59403b598271b8`

```dockerfile
```

-	Layers:
	-	`sha256:0d83775d9a82b872d13c51279917e2946cea6145a37c91478032fdf25e6181f4`  
		Last Modified: Tue, 12 May 2026 22:31:58 GMT  
		Size: 116.5 KB (116533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9c741fc1092568d4ff53d3c36b15911bb3affc256be1941d5a636761a2fc01a`  
		Last Modified: Tue, 12 May 2026 22:31:58 GMT  
		Size: 18.0 KB (17972 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:63ad5e1a565f7eb5b40d4a0700520f3c470ab56194bfa8fc4a6021737f1a39fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6808024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c54ea644ab96dd2035850e3d08ad32141e852ff6e2337aa40f5db54cc7d1bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 06 May 2026 08:06:10 GMT
ENV _BASH_COMMIT=330223688c6be0a7590e33f1b764a64633de52d6
# Wed, 06 May 2026 08:06:10 GMT
ENV _BASH_VERSION=devel-20260428
# Wed, 06 May 2026 08:06:10 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 06 May 2026 08:15:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 06 May 2026 08:15:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 May 2026 08:15:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 May 2026 08:15:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccad08d611662a4c6a0234a79ddd0c463405201ab3c73d4d1ddeeea1d68d2895`  
		Last Modified: Wed, 06 May 2026 08:15:30 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4034968107d1dab51408d85d6ffbfaf8d70534edb0543cc3e0ef286def13cc`  
		Last Modified: Wed, 06 May 2026 08:15:31 GMT  
		Size: 3.2 MB (3219566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62445306eaaf91170457b74740c431294d5e166b3a209a1745d18a16ac8de08`  
		Last Modified: Wed, 06 May 2026 08:15:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f01c3510ab24375f0d20b3afc47cdea6309d3e4534bd332775cc1794540c1bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b290b04d681600620fefd169c4e23ac8fa09d89897316593d2b8358460af705c`

```dockerfile
```

-	Layers:
	-	`sha256:7802a0d095198c866b35febe84f561f2d29a50e7a22cf56b242f7fe7cf871bcf`  
		Last Modified: Wed, 06 May 2026 08:15:30 GMT  
		Size: 116.5 KB (116529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75201dc48132fb708a2848c278f65396e142d13cfcc9aaca8bfe657349fed91c`  
		Last Modified: Wed, 06 May 2026 08:15:30 GMT  
		Size: 18.0 KB (17976 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:3cc00fc981d7e4afefee06261e8a7a9c59719f999b8b8bd74cf1741abaa7d152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6848235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77d72604c9c74dd6228c4e756222512161190a461929469c28104cf8d76dd1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 22:30:45 GMT
ENV _BASH_COMMIT=669b32f676a102193f65dcf88b98ba40bb361996
# Tue, 12 May 2026 22:30:45 GMT
ENV _BASH_VERSION=devel-20260508
# Tue, 12 May 2026 22:30:45 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 12 May 2026 22:31:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 12 May 2026 22:31:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 May 2026 22:31:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 May 2026 22:31:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9962303ab3016d33ad022058ffd4740aa3ede70a93b5117853ac03a7098647a`  
		Last Modified: Tue, 12 May 2026 22:31:31 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c87dc7cbba7209f747bff7426d970cb58ce3fc48549e17cc29cb4b064ecd66`  
		Last Modified: Tue, 12 May 2026 22:31:32 GMT  
		Size: 3.1 MB (3120913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac44196ffd7cc6e2c1799f5a281685559cec661c7970292af8a5f69269af7dd`  
		Last Modified: Tue, 12 May 2026 22:31:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:562d4fefb53e8119f55926db72a4c52ce9894a52ffea848a058fba002febf3ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 KB (134427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f418a3b2a41c5a41b36595de78c01e60821c214923ac4e721a112e34e8a5c032`

```dockerfile
```

-	Layers:
	-	`sha256:2e081bb242ad1c183df1939b67c63c2ce43631c35960b75c7246ee7cd041bf3b`  
		Last Modified: Tue, 12 May 2026 22:31:32 GMT  
		Size: 116.5 KB (116499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfcda4bc227c84f8a6b519820fe7b3f41024f8a931563a4a8be695e71585be5a`  
		Last Modified: Tue, 12 May 2026 22:31:32 GMT  
		Size: 17.9 KB (17928 bytes)  
		MIME: application/vnd.in-toto+json
