## `bash:devel`

```console
$ docker pull bash@sha256:982529bf8633f19db9c733f1ca994b212d8a0d00c33f14f4adaed50b74a83d21
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
$ docker pull bash@sha256:76dfba93eb9f0683594c108f54d8d20434386e2286b9c4cc1f7925dbb46e0ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6904327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0504c6677077810b62aa1dd014a49d176e648e4b630a3255ae5cef9046643c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:09:29 GMT
ENV _BASH_COMMIT=2d4ba0c618584d3554165b9484d921ec8c4e4523
# Wed, 27 May 2026 00:09:29 GMT
ENV _BASH_VERSION=devel-20260520
# Wed, 27 May 2026 00:09:29 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 27 May 2026 00:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 27 May 2026 00:10:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 May 2026 00:10:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 May 2026 00:10:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a0f7b01c13ec194a6347038643879df938ef99a4f99b29213245393123bc83`  
		Last Modified: Wed, 27 May 2026 00:10:13 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e688137ee5dd8077e084562fede0cf38dc0fed86f7ba214475b57932d816b15`  
		Last Modified: Wed, 27 May 2026 00:10:13 GMT  
		Size: 3.0 MB (3039344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e16c9c13f125590dc03c8c45e307c2d7d3e6f00a41254d7a4856e4eaff05b5`  
		Last Modified: Wed, 27 May 2026 00:10:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:0fc0e9ed2013fd9dd4911415221b194db2ddf6e29bf342dc12b289382938d04b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 KB (135454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0071584860d0b6f86c84fc29cc9d534dba926edaba34216cae00999f33d1d7`

```dockerfile
```

-	Layers:
	-	`sha256:65a9e7b8fabd4e32580be88af0a32be8f1646979fce529c93b673f390e487ce5`  
		Last Modified: Wed, 27 May 2026 00:10:13 GMT  
		Size: 117.2 KB (117150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a0d1e17545370b7c2cc31e3b5dce6ae06116e100d5f0cf3e7c2ea626c9f3c8`  
		Last Modified: Wed, 27 May 2026 00:10:13 GMT  
		Size: 18.3 KB (18304 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:40dc9590cb8dd64f8ca5ec6d5dec6b8f61c92724fe6766092d9e788a0f7e1690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6572360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f67868e642554a74749aaa8c1e0298732be406c1d08a37e7d7cb822f047c45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:09:26 GMT
ENV _BASH_COMMIT=2d4ba0c618584d3554165b9484d921ec8c4e4523
# Wed, 27 May 2026 00:09:26 GMT
ENV _BASH_VERSION=devel-20260520
# Wed, 27 May 2026 00:09:26 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 27 May 2026 00:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 27 May 2026 00:10:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 May 2026 00:10:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 May 2026 00:10:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff220f2f2e719e2f5ea5cb303bbc52318c154c40ee4194772dc3b303319d181d`  
		Last Modified: Wed, 27 May 2026 00:10:12 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531c1019d8cf56ee1722021ba285e3474949f8a94975dce16ee7252f06dd4e03`  
		Last Modified: Wed, 27 May 2026 00:10:12 GMT  
		Size: 3.0 MB (2999710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e4b5ef3f4538f86b3b75f5b39e364318f714c685bba86ee9b2302052617e64`  
		Last Modified: Wed, 27 May 2026 00:10:12 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:b0e56c0ed74c80820568fcc9d5a402ac6e258a76cb3807dbebe13d81c30012ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 KB (18169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20005bb1603cb9dbaf5051d2f0e4680de9a84d5d12ef709520ebebd6b3589ee`

```dockerfile
```

-	Layers:
	-	`sha256:b28343322d5e7edce1456dfbeebb0e04c2522ea128b8f09594faa1567066ea9b`  
		Last Modified: Wed, 27 May 2026 00:10:12 GMT  
		Size: 18.2 KB (18169 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:e197967f5c96b32f6077083f96b7c67e8546043bbd710802337058ca95675422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6232375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487b163fb8658f18444ff96fb938add3ec564c69cdeb19cd990c30024e8d02f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:09:07 GMT
ENV _BASH_COMMIT=2d4ba0c618584d3554165b9484d921ec8c4e4523
# Wed, 27 May 2026 00:09:07 GMT
ENV _BASH_VERSION=devel-20260520
# Wed, 27 May 2026 00:09:07 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 27 May 2026 00:09:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 27 May 2026 00:09:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 May 2026 00:09:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 May 2026 00:09:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ee2521163f53dfa02b7c7cb1521012ce334eba32e56ac8b95e6954ad3dd9a8`  
		Last Modified: Wed, 27 May 2026 00:09:55 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52459b177e2104f13fe35a2f54745c5ad9f058fe7f74af32148cfb38d3829eb4`  
		Last Modified: Wed, 27 May 2026 00:09:55 GMT  
		Size: 2.9 MB (2948464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a696c5d39f0f8becc2fa2654a37e38511d1b79c129871357ed32ffef9e944447`  
		Last Modified: Wed, 27 May 2026 00:09:55 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:54d417b147ed580eec0263e8cdf507b32000d2d23d7433fba1c16fbe76a740bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 KB (134920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0014377a70eed524337ec566635db2e3aedcad281d5fac387f2ec89a6a7c3a9e`

```dockerfile
```

-	Layers:
	-	`sha256:634539aa0c054e01591440a51700f59d50f2b5abb75da80570c552bc4a945369`  
		Last Modified: Wed, 27 May 2026 00:09:55 GMT  
		Size: 116.5 KB (116536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67ade837e925d6751bc318d8eb3b0d4683c0efd8801bcd74d8eb5d9270634fe`  
		Last Modified: Wed, 27 May 2026 00:09:56 GMT  
		Size: 18.4 KB (18384 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:44744b4f97d5798a87f58fe661fc0b6c038bf5b6b273f0b9c17efbdb39249a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7312392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69196e3e63a2b670d4bf2057439e06429f02239928abe3070cebf0ad391e5074`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:08:54 GMT
ENV _BASH_COMMIT=2d4ba0c618584d3554165b9484d921ec8c4e4523
# Wed, 27 May 2026 00:08:54 GMT
ENV _BASH_VERSION=devel-20260520
# Wed, 27 May 2026 00:08:54 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 27 May 2026 00:09:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 27 May 2026 00:09:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 May 2026 00:09:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 May 2026 00:09:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9b4c50b00a061d86cbaaef250ade53a2f38470e7aa067b2d99360a328b5f3b`  
		Last Modified: Wed, 27 May 2026 00:09:39 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5d2534f11f53874123b5eccdc71b1a84f5e04706d8aafac9ff269d32499ea6`  
		Last Modified: Wed, 27 May 2026 00:09:39 GMT  
		Size: 3.1 MB (3111726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6b0a31dd6761e8945eb8742c5d34f1f08bb2c2fff746e24ee376becae90d03`  
		Last Modified: Wed, 27 May 2026 00:09:39 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:96c743300686f2760a4b4658c531c1dd1a5553350380ee0cd8f4e275bfaef858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.0 KB (134963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233fc06f330db7ed191484283e8357d21fbae5f8744b7c91bccf5c97116acede`

```dockerfile
```

-	Layers:
	-	`sha256:0948eb904d69f10c872b4608f51302ffeebd2e3883ff42ec64ff1ecabb888b16`  
		Last Modified: Wed, 27 May 2026 00:09:39 GMT  
		Size: 116.6 KB (116556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4076d26c8441e7027066c1ff6312324f8f8d6476789d2ec092987ae46f5c65`  
		Last Modified: Wed, 27 May 2026 00:09:39 GMT  
		Size: 18.4 KB (18407 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:82daa253bd457845bb698ca05e4c460e3ec4a3a603b4dc0cca2ead1e2d860304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6658338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d097f36ee8126138f27a45a3179fb6dc514c8a84759d95280f87e578dbb9f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 27 May 2026 00:09:13 GMT
ENV _BASH_COMMIT=2d4ba0c618584d3554165b9484d921ec8c4e4523
# Wed, 27 May 2026 00:09:13 GMT
ENV _BASH_VERSION=devel-20260520
# Wed, 27 May 2026 00:09:13 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 27 May 2026 00:09:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 27 May 2026 00:09:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 May 2026 00:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 May 2026 00:09:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44bab10ae9305436e30f55eee31a266be79777bc5d5b85fc3e51b803496c6a7`  
		Last Modified: Wed, 27 May 2026 00:10:01 GMT  
		Size: 460.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1b260fe3e91d2f6503c7146e5b135953b9e45b540010aab701bd14ad976580`  
		Last Modified: Wed, 27 May 2026 00:10:01 GMT  
		Size: 3.0 MB (2967094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8838f84cb5ae64b06853ba60b56bcb56199440252d33b56b8d0692c2055aba`  
		Last Modified: Wed, 27 May 2026 00:10:01 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:6b6108b6b17e8688492de6efc37bd23e2a55e8c24b4549fecb2edc7c9cf96e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 KB (135397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b334a41b24664c794a4179d0b665f314f959a88532cdc8180d502fe9204b5e`

```dockerfile
```

-	Layers:
	-	`sha256:5518f72f737280fb732dcbc554147e12b4883b80e46d0052108a8a0ecff19e83`  
		Last Modified: Wed, 27 May 2026 00:10:01 GMT  
		Size: 117.1 KB (117125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6c33a320a6dfcbedefd5c4e01f1aeefbaee870b767eb5c957869c00afe6fc9`  
		Last Modified: Wed, 27 May 2026 00:10:01 GMT  
		Size: 18.3 KB (18272 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:b44a92d8c7deb8fbac0af259721afb8ebdc2f8e1be1ae24a5375f06decef1123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7184829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6275ca49c69e7ee877b2b9e8ddcf8ddca1286fb247b7015a78dcf9496b26ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 22:30:46 GMT
ENV _BASH_COMMIT=2d4ba0c618584d3554165b9484d921ec8c4e4523
# Tue, 12 May 2026 22:30:46 GMT
ENV _BASH_VERSION=devel-20260520
# Tue, 12 May 2026 22:30:46 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 27 May 2026 00:09:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 27 May 2026 00:09:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 May 2026 00:09:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 May 2026 00:09:02 GMT
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
	-	`sha256:cd4ba65b0588bc5d6af67ec429c3876e38b119baa7f6d0f91c1dae8daa820cda`  
		Last Modified: Wed, 27 May 2026 00:09:11 GMT  
		Size: 3.4 MB (3353107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e309fce1b1c1656483b47df84d3a8b17a2faf9737ef2e0341b46d745c044cf`  
		Last Modified: Wed, 27 May 2026 00:09:10 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:d848c9e2bc77ca18a01adb76e45788ecae050a1d4dac5767cab2ea9a81fb448b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 KB (134881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e13d862d95627b8084dae11a27ac051f085b8e115f3e025eaf94c609808542`

```dockerfile
```

-	Layers:
	-	`sha256:c392d8c28e74b8e3efc45033b7b4123e6a84fddec50325db516293017fc8c252`  
		Last Modified: Wed, 27 May 2026 00:09:10 GMT  
		Size: 116.5 KB (116533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eba99efeb252675dd0cde4c736b2dd8598be5bb999f30c5a66830cb9ae84b7a9`  
		Last Modified: Wed, 27 May 2026 00:09:10 GMT  
		Size: 18.3 KB (18348 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:c7dc54acbf8d0754cc28ac604d671239617f90a19b2ae6df888d34807ebd0547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6807640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051576f4de0554815302b4432bfaddbb3a957fef1741c191301c95ac4922c032`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 13 May 2026 09:39:52 GMT
ENV _BASH_COMMIT=669b32f676a102193f65dcf88b98ba40bb361996
# Wed, 13 May 2026 09:39:52 GMT
ENV _BASH_VERSION=devel-20260508
# Wed, 13 May 2026 09:39:52 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 13 May 2026 09:48:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 13 May 2026 09:48:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 13 May 2026 09:48:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 13 May 2026 09:48:47 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7406b38ae22aa921be864db0bd889fffbb46f3b6b369b2171ddf4b873b25ed`  
		Last Modified: Wed, 13 May 2026 09:49:12 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b04070a040eb682bd0010dc7d7a5c338d5c9529a95c93c1d672e839ac2995c`  
		Last Modified: Wed, 13 May 2026 09:49:13 GMT  
		Size: 3.2 MB (3219183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5037b9c01581572b65a23cda9673394b44f05c5a640343e3c6ac1114f677e4`  
		Last Modified: Wed, 13 May 2026 09:49:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:f392749c2376ee4432cf560058d86044038286ca75d48652ed2fd5b83feb4b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 KB (134501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb0662348e628aaff0f3a8ab6e7a34b64266cfba44a8edc78a0679276ab98a2`

```dockerfile
```

-	Layers:
	-	`sha256:f911c77c488b7ec217aa43e82042791020547c7403f1d0ea254a0bc1211b2dc8`  
		Last Modified: Wed, 13 May 2026 09:49:12 GMT  
		Size: 116.5 KB (116529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f77d3cf50b01c3b8886216b7ec3211b239f736d875d01608ecb9a137870ef4b`  
		Last Modified: Wed, 13 May 2026 09:49:12 GMT  
		Size: 18.0 KB (17972 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:d3a338be72e7494597d4d24478d2b9555e001c85b7185e52ce989c8673fb91a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6859186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ee328a3b64dbbbe0f6fced0db5df5a263e3d44aab53ed4e2a50357d62f5700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 22:30:45 GMT
ENV _BASH_COMMIT=2d4ba0c618584d3554165b9484d921ec8c4e4523
# Tue, 12 May 2026 22:30:45 GMT
ENV _BASH_VERSION=devel-20260520
# Tue, 12 May 2026 22:30:45 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 27 May 2026 00:09:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 27 May 2026 00:09:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 May 2026 00:09:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 May 2026 00:09:19 GMT
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
	-	`sha256:da338369494d0eb0728d62b06b4242dba43838fc0b9c57a015b0353fbc8b0537`  
		Last Modified: Wed, 27 May 2026 00:09:31 GMT  
		Size: 3.1 MB (3131859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df347754504ccd196f4386ad768bc1274b45d89d11640d594469a00b514c1a9`  
		Last Modified: Wed, 27 May 2026 00:09:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:6555d50f1e2aa63c9c768a13eaae35e1908186674a54fc864e8cbb9d6bc0714a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552f699c496d95ccb78001f777e12516e014c61d150bea92cd833fc92c8593e5`

```dockerfile
```

-	Layers:
	-	`sha256:0804e4bec881c95ec74c36b85a50d7cb1cc6e48f6df381bc95fa2bc5a14fac86`  
		Last Modified: Wed, 27 May 2026 00:09:31 GMT  
		Size: 116.5 KB (116499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15dd5a216136b62103f860d7031240013ae1ce8e2c42ab91ad4bcaa2ba51ee8c`  
		Last Modified: Wed, 27 May 2026 00:09:31 GMT  
		Size: 18.3 KB (18304 bytes)  
		MIME: application/vnd.in-toto+json
