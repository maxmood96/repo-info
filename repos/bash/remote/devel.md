## `bash:devel`

```console
$ docker pull bash@sha256:711c88b7449ab25af703ba2773a3e01d1d45decdbad15df853b06dd7c52700f6
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
$ docker pull bash@sha256:7282ab1e76f58017cc0e53bc3e4deb50252a264d1925c77f144f28a85289d77d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6892515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c852300a64e148a3cbf5c1c48037536b169a440840fe11dafbc85250ce40b83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:12 GMT
ENV _BASH_COMMIT=1cbe8c04bb0aa62e0493e096472528cdea983fc2
# Wed, 15 Apr 2026 20:16:12 GMT
ENV _BASH_VERSION=devel-20260402
# Wed, 15 Apr 2026 20:16:12 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 15 Apr 2026 20:16:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 15 Apr 2026 20:16:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:16:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f6bfa3feb4e12a71edb8fd889cfb3443ed85367dc820f46e581ea6280808bf`  
		Last Modified: Wed, 15 Apr 2026 20:16:50 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef627b3a4429a3f900dd90481a13a63d800e5f08ef053e2e3ca62c9d04364207`  
		Last Modified: Wed, 15 Apr 2026 20:16:50 GMT  
		Size: 3.0 MB (3027543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef17e956d779622452c684b45ce8e0fd568ce6e59da4293f67e385ad1dd507e`  
		Last Modified: Wed, 15 Apr 2026 20:16:50 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7ca978825e993441aa10756d25605a227fb133569df952a89c4ceac5002918a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 KB (135258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da009661af1ae4f693c6bca736d1c29877fd8a51b136d1c6376469bae0e33134`

```dockerfile
```

-	Layers:
	-	`sha256:69fe6c24582aa62b9edd579600a6717d18ff86215d8e66ad3ea4ac1849f8ee29`  
		Last Modified: Wed, 15 Apr 2026 20:16:50 GMT  
		Size: 117.2 KB (117150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1216d494e85a36870e7fd00eae675b82effc2f299deb85f8850d50df4dd9fedf`  
		Last Modified: Wed, 15 Apr 2026 20:16:50 GMT  
		Size: 18.1 KB (18108 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:86853bcf992d7c61c9b5d489bf5ca68321aa2dd2fc8dc32f34a64c4ce70ed246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fc70158975a151923e869612e94a3a6389ad218b7ff15a82c550744d67a954`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:09:24 GMT
ENV _BASH_COMMIT=1cbe8c04bb0aa62e0493e096472528cdea983fc2
# Wed, 15 Apr 2026 20:09:24 GMT
ENV _BASH_VERSION=devel-20260402
# Wed, 15 Apr 2026 20:09:24 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 15 Apr 2026 20:10:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 15 Apr 2026 20:10:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:10:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:10:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e211fa4b4881fd60ef1125ab06065049e7122172a57c46cb26a737ae23e387fb`  
		Last Modified: Wed, 15 Apr 2026 20:10:12 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de074f846981b0d6098c3c23950f0a9db486ea66141b8fb118ca92337490da0e`  
		Last Modified: Wed, 15 Apr 2026 20:10:13 GMT  
		Size: 3.0 MB (2986802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5dc47db75d180cc5ea1f19d4cf5e3dbaf53ac24a17abc59683550322a29f9ae`  
		Last Modified: Wed, 15 Apr 2026 20:10:12 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:c36fd880ad2165b4fef115030ad26667628a8ddc5e295191910e829bfbb6fa69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 KB (17973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1458408f92ddbf9e9832591ecb62cc755f9669f412ab26747905a5018a1d8b35`

```dockerfile
```

-	Layers:
	-	`sha256:5e6ab542bb3d88c58aa138226bb21f272e43e1737dc387b86f03bbf073158436`  
		Last Modified: Wed, 15 Apr 2026 20:10:12 GMT  
		Size: 18.0 KB (17973 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:44f485ab2a41509a4f2d89da0166bc8a496ae399ea638bd064eed25a66cefc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6220545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fec46b38b5ca32566cce314c45be97279ada0f3f31705a77193fa7c85a26356`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:11:52 GMT
ENV _BASH_COMMIT=1cbe8c04bb0aa62e0493e096472528cdea983fc2
# Wed, 15 Apr 2026 20:11:52 GMT
ENV _BASH_VERSION=devel-20260402
# Wed, 15 Apr 2026 20:11:52 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 15 Apr 2026 20:12:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 15 Apr 2026 20:12:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:12:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:12:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a314368b101d20a0e79637b750ff9e8514ce0c4142fd94096790f9c78a9b83a`  
		Last Modified: Wed, 15 Apr 2026 20:12:37 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f810ef64f67ae2a55158289bb009d15c30d839c50f2593468109418775b06548`  
		Last Modified: Wed, 15 Apr 2026 20:12:38 GMT  
		Size: 2.9 MB (2936631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4987080683e9c8498264082d890fd49120a267ef715a1ce84c88197b997bd18e`  
		Last Modified: Wed, 15 Apr 2026 20:12:37 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:a032726f5f392c6273154f14c40649e8f1b54640f0d33f22cee03d21c2c41615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8072ebe78421e5b42f90e740c5d520bdaea0e77d11483c4a64732bd16f0c1ace`

```dockerfile
```

-	Layers:
	-	`sha256:e234b5e887fde2ec941e21845f545d0625610370c02add5769ea8eca306b95ab`  
		Last Modified: Wed, 15 Apr 2026 20:12:37 GMT  
		Size: 116.5 KB (116536 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98ceb18a4adab97b4bcec53a4714a1a3bbe32db1cb89272318d037cd55bf9827`  
		Last Modified: Wed, 15 Apr 2026 20:12:37 GMT  
		Size: 18.2 KB (18188 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:1940de7146c420995e2cefe6090157c706b12c358bc4f974e0f796831bbc798b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7298289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca866872c7b3163a135c81a0d4fb8d274331d4cf5b972d8b982454540f780ad9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:12:09 GMT
ENV _BASH_COMMIT=1cbe8c04bb0aa62e0493e096472528cdea983fc2
# Wed, 15 Apr 2026 20:12:09 GMT
ENV _BASH_VERSION=devel-20260402
# Wed, 15 Apr 2026 20:12:09 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 15 Apr 2026 20:12:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 15 Apr 2026 20:12:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:12:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:12:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3915754a3b32123e1ea92385bfe0586662170357bdbd108935c819c210799da1`  
		Last Modified: Wed, 15 Apr 2026 20:12:55 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7738fdc7180a1dabe512880ec480ddc4522f5bb77b620d432f23fb4dd435576b`  
		Last Modified: Wed, 15 Apr 2026 20:12:55 GMT  
		Size: 3.1 MB (3097632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67dd9c43736a0caf935482d7e753913bfd96163df21447ae0601ac1356aa0c4`  
		Last Modified: Wed, 15 Apr 2026 20:12:55 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:9b0a453ee170e1ec14dec5d329ad9f9094e15db1f0f88e3e33e388ab599c3a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 KB (134768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d2b8b366030f67f4fdd4241aefd04a600d66469d73d63e5d3ae39c2a637951`

```dockerfile
```

-	Layers:
	-	`sha256:e7b32089f63b734013b05515f5bee28b341c898d59f5256a21581bd91a544802`  
		Last Modified: Wed, 15 Apr 2026 20:12:55 GMT  
		Size: 116.6 KB (116556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:085d4a1c3ae5904352bd85ad0e897fc0d99e211ac49ef187e9db751fc23b5ff1`  
		Last Modified: Wed, 15 Apr 2026 20:12:55 GMT  
		Size: 18.2 KB (18212 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:f9704c973a880d16979b769d54ef657fbd2eb0e5a1a55514c110802ce4a3a191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6642253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:664c21192a8843c1fad55f0ba05692c41ac3d4b4b742d03a43b42176c7739256`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 07 Apr 2026 17:49:04 GMT
ENV _BASH_COMMIT=1cbe8c04bb0aa62e0493e096472528cdea983fc2
# Tue, 07 Apr 2026 17:49:04 GMT
ENV _BASH_VERSION=devel-20260402
# Tue, 07 Apr 2026 17:49:04 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 07 Apr 2026 17:49:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 07 Apr 2026 17:49:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 17:49:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Apr 2026 17:49:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdc84be47535ffdfd21e1cf91a1ded78c884c8a1829c3a1670255a85da105f5`  
		Last Modified: Tue, 07 Apr 2026 17:49:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeeec76111fde4caf684d936de33fd46a49855820e5904844d69f6d3846040e6`  
		Last Modified: Tue, 07 Apr 2026 17:49:50 GMT  
		Size: 3.0 MB (2954466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299752e53416d157d4c9972af9bd5e135566ef21790e6482ec527292f714d512`  
		Last Modified: Tue, 07 Apr 2026 17:49:50 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:357e4f9286779a6e3ce1b54aeb8a76c777e440446a2a37b9696847ef37466459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:122b89a94b92a29dd11bba63a12b08bf48633a525f99e79e0aa280ddae184d31`

```dockerfile
```

-	Layers:
	-	`sha256:998168400ee65a4a928bac4ec30f7acbb9152ff8e698e1301052d13d80712de0`  
		Last Modified: Tue, 07 Apr 2026 17:49:50 GMT  
		Size: 117.1 KB (117097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:484181e204b4b650e4a8f7dd623ae4b17c0f6995cd1966b3ea8be0736dc5712b`  
		Last Modified: Tue, 07 Apr 2026 17:49:50 GMT  
		Size: 18.1 KB (18076 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:730df58964005621fc3e196011a550ae398b5aad758b1771ae39d6c3c9a06f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7169362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9d92e9c17d5137d9e392e7964fafc2bc0932acf3cd7717b36a975141076f1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:09:47 GMT
ENV _BASH_COMMIT=1cbe8c04bb0aa62e0493e096472528cdea983fc2
# Wed, 15 Apr 2026 20:09:47 GMT
ENV _BASH_VERSION=devel-20260402
# Wed, 15 Apr 2026 20:09:47 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 15 Apr 2026 20:10:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 15 Apr 2026 20:10:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:10:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:10:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7366a81355efdc0ece7f9b362fa739c043ffb0aac427b70756f25f59c5daf60`  
		Last Modified: Wed, 15 Apr 2026 20:11:09 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18db605174e834c8bf221e8e36edd7dce490d92a4005af7cf4d83ba0882856a8`  
		Last Modified: Wed, 15 Apr 2026 20:11:09 GMT  
		Size: 3.3 MB (3337640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c78e49901e30c950ecd1f107a380d4a216fe674e4580c153df19ac18c615ce`  
		Last Modified: Wed, 15 Apr 2026 20:11:09 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:dd5ac11a1bf5c6fb6564082e9072cb1410c3202204ea82570e75a7de9b9b47bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d674b293027ffbf158ac42a21ab31d4bff28ab11b0d209601242226f95cb6dd5`

```dockerfile
```

-	Layers:
	-	`sha256:4500d1e095666d8201c97649b58d5e9956791cce016758e8e08c305bf0bf75fc`  
		Last Modified: Wed, 15 Apr 2026 20:11:09 GMT  
		Size: 116.5 KB (116533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af5b5d90f2398c1f1b9ea4fe50ecb96654f2d06058a62884e5ac13e2edd3b2c`  
		Last Modified: Wed, 15 Apr 2026 20:11:09 GMT  
		Size: 18.2 KB (18152 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:6d5e8c44b24a770615a9d63315f6384c3acd3d0abad625261c14c7794a8ad86c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6807221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b0abe06e32179cc883e4582dc0ea3c50fd50628b2b91303e09fdc71d0cf9c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 21:18:59 GMT
ENV _BASH_COMMIT=1cbe8c04bb0aa62e0493e096472528cdea983fc2
# Wed, 15 Apr 2026 21:18:59 GMT
ENV _BASH_VERSION=devel-20260402
# Wed, 15 Apr 2026 21:18:59 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 15 Apr 2026 21:28:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 15 Apr 2026 21:28:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:28:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:28:00 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a281c521e8944b423ef98f3b76413505c9e5c827fbc05de2fb351ecf3f85cdd`  
		Last Modified: Wed, 15 Apr 2026 21:28:34 GMT  
		Size: 458.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8f82b5989cf4c706c5947fc88eb745e2364b53100cedaba335404ad35ba019`  
		Last Modified: Wed, 15 Apr 2026 21:28:34 GMT  
		Size: 3.2 MB (3218766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5aefdd7afb11f74db94f4b74abced9c9e61f4908fd9faced4812c87eab8481`  
		Last Modified: Wed, 15 Apr 2026 21:28:34 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:3ee2132c82d027d57ea1c53acd16ed077b78bcddbc6fb0a2a5b787689718ac3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd29a3cd05eafed13506bff0a7a1e6a57bbb105b16a669568a21020500dc3725`

```dockerfile
```

-	Layers:
	-	`sha256:df46d8ce32400269631c90fdfb57c10bcab47059e91317caabc1b82f06c33104`  
		Last Modified: Wed, 15 Apr 2026 21:28:34 GMT  
		Size: 116.5 KB (116529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ebbc9429da55ac2fe8d399057b02d8b2b53023628279055e0b6709b1c10923a`  
		Last Modified: Wed, 15 Apr 2026 21:28:34 GMT  
		Size: 18.2 KB (18151 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:6ec84ddad873c1925d0254893403e319d7b3b7b43ec5d229c16f1bdfbda62040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6847969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44bb0283fe38c85b53f0176adf6faeb2ab9bc8d41f08dab837ce90cd165c102`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:09:44 GMT
ENV _BASH_COMMIT=1cbe8c04bb0aa62e0493e096472528cdea983fc2
# Wed, 15 Apr 2026 20:09:44 GMT
ENV _BASH_VERSION=devel-20260402
# Wed, 15 Apr 2026 20:09:44 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Wed, 15 Apr 2026 20:10:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Wed, 15 Apr 2026 20:10:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:10:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:10:31 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36608347164e95cac33fd5a1d6b63a0a6da59d410d0da223ead87b7db12dce47`  
		Last Modified: Wed, 15 Apr 2026 20:10:40 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d560e1184483668eb957f72293bddeed5e53d3d60ba5ae774b05d8a44a41d07`  
		Last Modified: Wed, 15 Apr 2026 20:10:40 GMT  
		Size: 3.1 MB (3120646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1a421d3056511aafdc2cc153c84e1ffcf78bc186e75aea43cb82925308ad5a`  
		Last Modified: Wed, 15 Apr 2026 20:10:40 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:731ad6e3993413431b56112b882cb7b8a6a537d6b47d7b4ffce58932b6ad9e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33844d7533d269a397d9d795945b33c965edf9dbc6076b89d769496fb8a3d8d`

```dockerfile
```

-	Layers:
	-	`sha256:001a29997bae79c82d82449e58f87d07469e4c84289f9a6587bffce0fbc2dd8d`  
		Last Modified: Wed, 15 Apr 2026 20:10:40 GMT  
		Size: 116.5 KB (116499 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1aa03ae919973a9c7eb537fec02fe10b60678a03cc1de3e014ebe069d18117`  
		Last Modified: Wed, 15 Apr 2026 20:10:40 GMT  
		Size: 18.1 KB (18108 bytes)  
		MIME: application/vnd.in-toto+json
