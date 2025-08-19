## `bash:devel-20250814-alpine3.22`

```console
$ docker pull bash@sha256:137f1fe75e8247caf98fce7be9fadd658f5ddc1494b7cc65f3940e8f5131a51c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `bash:devel-20250814-alpine3.22` - linux; amd64

```console
$ docker pull bash@sha256:e3042d57b470f0e09f0ce10a5a51663237ad12e74c66d58566ffc943e09a8f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6798460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c03a415c6027e84200b2bc4c0f4f874ff7a8e064c0bb4b624ed1225ad138367`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_COMMIT=3160c0b89ce4f3934e791de94f9370b6cfc26ae5
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_VERSION=devel-20250814
# Tue, 19 Aug 2025 04:18:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7e16eca0bdfccd549e753eed57a8bd9c7b0361ea80aef8a9c894706a5e1c25`  
		Last Modified: Tue, 19 Aug 2025 17:10:40 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3130d9d560c4b60fc68c16c1c25134fc1138818aa792407316d535cbbac9daa`  
		Last Modified: Tue, 19 Aug 2025 17:10:41 GMT  
		Size: 3.0 MB (2997982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4f78257a83d46391e18845c3330eba883b7abd4412054100298346b340ae52`  
		Last Modified: Tue, 19 Aug 2025 17:10:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250814-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:247d1b15e4f9b09bc558740f8a355429c45dca99c4ee8177ec3d9659557edbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 KB (136491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:473f7b1ef677dc770c63be924a18da6cef11dc3866a179111ce28a84b12367b8`

```dockerfile
```

-	Layers:
	-	`sha256:14103b0fcc137fa6f0d4f67d6a4b22d1db250ae9acd8927c91d52c2478616481`  
		Last Modified: Tue, 19 Aug 2025 18:02:49 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3522bb35765326f63152eced455bd013c93f47506e239fc29f19dcbea97a46ef`  
		Last Modified: Tue, 19 Aug 2025 18:02:50 GMT  
		Size: 18.1 KB (18062 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250814-alpine3.22` - linux; 386

```console
$ docker pull bash@sha256:2d11a837591cf5be96a12918a6f9568816c10e8644904b6af5b73bc008a55680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6540593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092a35cf3e049ce9757149662e2e7919ca41f2a55ef310ca40901c76c7d53786`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_COMMIT=3160c0b89ce4f3934e791de94f9370b6cfc26ae5
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_VERSION=devel-20250814
# Tue, 19 Aug 2025 04:18:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18231143459242c90b1fcbae33e7b63065871453a1307eb1da29a6d31ead3b9e`  
		Last Modified: Tue, 19 Aug 2025 17:10:42 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e12dc8483509fa907582e53408a9798072a3f4721b951adb5bf6a3a8cfd338`  
		Last Modified: Tue, 19 Aug 2025 17:10:43 GMT  
		Size: 2.9 MB (2924798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f7849cb29ad3034818bf099388bc2c2d31da4ced3a5923aec1f03d1235896`  
		Last Modified: Tue, 19 Aug 2025 17:10:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250814-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:ccf3f5714abef436808b9c2bc5b2e25c9f8892e1f4c3fa7da20bb98d628780ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 KB (136435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cddd335796620ae09979e2eb596952d74bd4cf9b2a90b2e530ef6bafb045043`

```dockerfile
```

-	Layers:
	-	`sha256:d3bb881a3f4a016398f965d34899649c97a8e0555f1f95b42aff55f124f48b22`  
		Last Modified: Tue, 19 Aug 2025 18:02:53 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:901f83f3bbf14084593f0ff91dc07d627367e8ff3d853af0e1041d5628ac2e11`  
		Last Modified: Tue, 19 Aug 2025 18:02:54 GMT  
		Size: 18.0 KB (18031 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20250814-alpine3.22` - linux; ppc64le

```console
$ docker pull bash@sha256:b6fe7a3681d3e389d5827afdd4ff31a6df3031ce51b221457644e5c9570b6227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6999781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b5dd0aa8f33d4ab57739b2f33429f29692573a7064d317469a8e94309c6709`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_COMMIT=3160c0b89ce4f3934e791de94f9370b6cfc26ae5
# Tue, 19 Aug 2025 04:18:14 GMT
ENV _BASH_VERSION=devel-20250814
# Tue, 19 Aug 2025 04:18:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 04:18:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Aug 2025 04:18:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ff06a1a69f7247d5e96a6980c0e47c568e805fafbc8fc62a80e2fceeaa7d7a`  
		Last Modified: Tue, 19 Aug 2025 17:10:41 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac2eb4b6b597c5f4b78a43289860442863059dc1cba6dad1f064703f034968a`  
		Last Modified: Tue, 19 Aug 2025 17:10:41 GMT  
		Size: 3.3 MB (3271874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8080e740b64625753bc26a06a1c5231b0d7cd039d1c0c515467165a3e9a4e3a4`  
		Last Modified: Tue, 19 Aug 2025 17:10:41 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20250814-alpine3.22` - unknown; unknown

```console
$ docker pull bash@sha256:5dd9607d8778ff4492ea50e1fb1d8ee54dd176fafc6c8659b4813b734391d78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e655407a2dc55980a9245ec459afa986009a59aef9d1cffba578cecbd0834867`

```dockerfile
```

-	Layers:
	-	`sha256:5a1024fa6eceb22781adf12b72d4bc1f4470593e9123191b4b46a0ba8907d19e`  
		Last Modified: Tue, 19 Aug 2025 18:02:57 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6006f556d200de47597fd8616223a66dbb3c64bd896f0ed7babef1647686c621`  
		Last Modified: Tue, 19 Aug 2025 18:02:58 GMT  
		Size: 18.1 KB (18107 bytes)  
		MIME: application/vnd.in-toto+json
