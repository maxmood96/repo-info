## `bash:devel-20260608-alpine3.24`

```console
$ docker pull bash@sha256:a7206761da3a43a88f27d4fc1e2919cc410712d644ebcc8b8db9dafb7ab7ceef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `bash:devel-20260608-alpine3.24` - linux; amd64

```console
$ docker pull bash@sha256:d84d65f552c394bddfd3c78f603a8d231cc616513d407c0139996c1fb40168e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6907956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd7b4fc7405bd36555f1b3fd3fe9327820f05e661966ff06907ab458c1432f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 23:11:22 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 09 Jun 2026 23:11:22 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 09 Jun 2026 23:11:22 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Jun 2026 23:11:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jun 2026 23:11:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 23:11:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 23:11:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44affc9edf0885b189f28337845c747e64c5119165906570d32eb0ecc1fd952`  
		Last Modified: Tue, 09 Jun 2026 23:12:04 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ceb3d79deb47160dcc4a91903f5ac6112472ffc55ddcbd0c1f8d1dbb046988`  
		Last Modified: Tue, 09 Jun 2026 23:12:05 GMT  
		Size: 3.0 MB (3040417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147214ee3309ee118a289baeac68de2ae9d72fc18a154f05291ce36d15e76754`  
		Last Modified: Tue, 09 Jun 2026 23:12:04 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:bedf2ef57eb6f1a3f852282b4c06711b7385576448a7cc3abcc4b9ad2ae8e532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415a9b11355e8b416d808e59074efabe33f22ea5784a7342540e9253ce6fb958`

```dockerfile
```

-	Layers:
	-	`sha256:8ebdb870e11d146aea1b8e4c6d1c71fa306b12b085d5ad5d8620a9facbf5d0f0`  
		Last Modified: Tue, 09 Jun 2026 23:12:04 GMT  
		Size: 117.1 KB (117128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172da7c5374c2a5a56a30fe9c9e974d918813a3b9cb7053fb3d46b86e329bfc7`  
		Last Modified: Tue, 09 Jun 2026 23:12:04 GMT  
		Size: 18.1 KB (18084 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; arm variant v6

```console
$ docker pull bash@sha256:8b5b154c57dba85aa4a99fe57fac412360162c0d3a2c381b8a4c50438f4fcc97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6577098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e62375bb2b3f387555159501ed7a487625db00430dbdbaaad8ef1ad7882d17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 23:11:25 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 09 Jun 2026 23:11:25 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 09 Jun 2026 23:11:25 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Jun 2026 23:12:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jun 2026 23:12:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 23:12:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 23:12:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94543c7995c0ad1f43161e69dfe17362c53faef19deff8599f8e41ffecd6d844`  
		Last Modified: Tue, 09 Jun 2026 23:12:19 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b1b1dd70b967a38bb8f026af57fb8b9d08e8c60e4015baa338467607dc193f`  
		Last Modified: Tue, 09 Jun 2026 23:12:19 GMT  
		Size: 3.0 MB (3000998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abffdedd0edf47cac0f9a809682ae52c400575d75d1059404e882f2275bdf28c`  
		Last Modified: Tue, 09 Jun 2026 23:12:19 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:df81c09518d8cfd9324b51a4ed89fad669f798dc16e2d75a37ec64ac9e903738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3733e73c27a82c9277f5fce9888ac1f3b1bd9366864082fde52509d4eb8bc6e`

```dockerfile
```

-	Layers:
	-	`sha256:2567c827f9740dfcea88919f32e54ad5e5e1e0e58d659a7962e92760186d06ef`  
		Last Modified: Tue, 09 Jun 2026 23:12:19 GMT  
		Size: 17.9 KB (17949 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; arm variant v7

```console
$ docker pull bash@sha256:a6c93b107c6fad78628e27ee639a6bb39d939e7f1a084625e1bf60392a246334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6236552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83716e9efbaf6a12ac2fdd8210729a9a67c3c7f552122a1e0f712f9b4ae8181f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 23:11:24 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 09 Jun 2026 23:11:24 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 09 Jun 2026 23:11:24 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Jun 2026 23:12:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jun 2026 23:12:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 23:12:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 23:12:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532fd74e3fd2e60715e9dafb1227b7134f2e533ec0cf82075e1c9b7866f47aa8`  
		Last Modified: Tue, 09 Jun 2026 23:12:16 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f2aa5b89fd02a70ba41f5d482e68592fa286b87513772f08d061e4cf47e93`  
		Last Modified: Tue, 09 Jun 2026 23:12:16 GMT  
		Size: 2.9 MB (2949605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc941e014ddad975404a6bbb565bf94bebd6a9bf34182e081317f21eecccb8e6`  
		Last Modified: Tue, 09 Jun 2026 23:12:16 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:6eda38d2e1ba18f74d84ac144945f14f69c4807dde939e872d90ad83d62abb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f88a65d40e44d48eff52a3c9bf1ba8f962b1ae5f14a085988f6968aa98668ebd`

```dockerfile
```

-	Layers:
	-	`sha256:7c848ca1bb0b5dc0feffe12561bd1727b1e3471ccda7ab176458a79ab4962a77`  
		Last Modified: Tue, 09 Jun 2026 23:12:16 GMT  
		Size: 116.5 KB (116514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eed4e19f2c2502b9858d9867bd75d28af7f89767c6c72f5b774c2e252c585ca`  
		Last Modified: Tue, 09 Jun 2026 23:12:16 GMT  
		Size: 18.2 KB (18164 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:85b0012632ab32e6a759a1f5ed4cc801b830aef0bcaabcc24e0dbb02368d19b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7315857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23acf42a93ba373a34aacc6e5462aacfb178e5a02bc45e0be65c98c247151506`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 23:11:22 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 09 Jun 2026 23:11:22 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 09 Jun 2026 23:11:22 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Jun 2026 23:12:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jun 2026 23:12:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 23:12:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 23:12:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffebcffa766b411c29c754338d97c4b1ece15be7e47cbf5ffe3afab89b16c25`  
		Last Modified: Tue, 09 Jun 2026 23:12:10 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd1d6c04d65176a1a52d2e1333e2adb43778a5199d0f952ea974528887396a`  
		Last Modified: Tue, 09 Jun 2026 23:12:10 GMT  
		Size: 3.1 MB (3112734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c2f83defc3ac84d0d2a1bd23c27f70ae28fb16eac954a6a9c2fecc351bcc28`  
		Last Modified: Tue, 09 Jun 2026 23:12:10 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:19b0e71e30c4b36f3906ba6982368fcca3ee36b600b594c41f121acd57ae4b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da08e6d3756cb961f7785896bdfd370a71bf15534c99389d7502a82fc3fe3232`

```dockerfile
```

-	Layers:
	-	`sha256:c3c04bad0f02030a78f28010a24b9c956f9d79d37978b02922654827da676056`  
		Last Modified: Tue, 09 Jun 2026 23:12:10 GMT  
		Size: 116.5 KB (116534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e5dbd7c3e4fad6e3c7281b021201adfff96eea95f60a5b93d4eb9d826d9312`  
		Last Modified: Tue, 09 Jun 2026 23:12:10 GMT  
		Size: 18.2 KB (18188 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; 386

```console
$ docker pull bash@sha256:0420e17714e7ad7d42d5ee3c1a90b0b6dd1b624ed3f3fd13f9223d2237e73132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0604d697b18c18a08c150cb958d6a2b5f02c69cd98b65fc7aa61542f9dc27398`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 23:11:45 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 09 Jun 2026 23:11:45 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 09 Jun 2026 23:11:45 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Jun 2026 23:12:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jun 2026 23:12:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 23:12:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 23:12:28 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fd4651d434aaaac1bfc66830b4d81ce7d046c9b5cf029a6260a5fc63adce04`  
		Last Modified: Tue, 09 Jun 2026 23:12:32 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbeae6d4fd1b2539518d592bb41f79947fae6bc6ea553f19771e3b9543d26c5`  
		Last Modified: Tue, 09 Jun 2026 23:12:32 GMT  
		Size: 3.0 MB (2968168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0ce4aa9ef3c435a37c558580d77f70f266687ccce61db6e7a5ed8bb4eb7bf0`  
		Last Modified: Tue, 09 Jun 2026 23:12:32 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:a823aed4b1bb796ec511844e6203b1807ce57ee1770ce5ba50822dce69869e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 KB (135155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c19aa91277a5299f2d6554cc0787c4ed025254c9fea3a80b7643cc43f153b5b`

```dockerfile
```

-	Layers:
	-	`sha256:7a2417d4da4198a28da17ec835986fb816085e56ec02a55e623bef5828d7141e`  
		Last Modified: Tue, 09 Jun 2026 23:12:32 GMT  
		Size: 117.1 KB (117103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b7101c07039a98145cdd88f22c8af2f465b25ecb23b540967116c6668b34aa7`  
		Last Modified: Tue, 09 Jun 2026 23:12:32 GMT  
		Size: 18.1 KB (18052 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; ppc64le

```console
$ docker pull bash@sha256:fddf92f7d43bf31cf5a6a64934d22290a6ad5460d2141f0ac2eee25a8682c648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7188948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad84142f212391837de800f80e29099405022decf492a2db4689da8f2f57ee5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 23:10:28 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 09 Jun 2026 23:10:28 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 09 Jun 2026 23:10:28 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Jun 2026 23:11:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jun 2026 23:11:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 23:11:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 23:11:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabd24973ee1046e69301ab7f9fa2f2b7e8a7cc194a874e20bdd8f4abccfb07e`  
		Last Modified: Tue, 09 Jun 2026 23:11:41 GMT  
		Size: 455.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afd4284a65954bf211c15bcd15dc023bdd4082407d9e1db3785cee4e806852b`  
		Last Modified: Tue, 09 Jun 2026 23:11:41 GMT  
		Size: 3.4 MB (3354199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c432d3c1deaefcff2285c6a06250db75ce06be395dc0b6fa7b7889b508bc702`  
		Last Modified: Tue, 09 Jun 2026 23:11:41 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:e3dc657cfad2712f00ae0b058ad3efe1e6bd002a252da0da3e89234909d4c6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d118e85bbecd3aaeed72f2981aa8f2c307918cf48aedf0695a162512349a3d`

```dockerfile
```

-	Layers:
	-	`sha256:3ce5fe1e4f38c3dee63a5d9ce10d419b525ca014aa3f5350b6dc28e8670566ec`  
		Last Modified: Tue, 09 Jun 2026 23:11:40 GMT  
		Size: 116.5 KB (116511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29789cd01b6e0c744dbcfbc28a51343144dc601f9463e1ae8ffa590474e801fc`  
		Last Modified: Tue, 09 Jun 2026 23:11:41 GMT  
		Size: 18.1 KB (18127 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel-20260608-alpine3.24` - linux; s390x

```console
$ docker pull bash@sha256:cba730fe85f062d3cc1569396d416d0ba653f3f4f0c07079a02b84ec1655438c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6863697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2a87e861dc9360ada2092c8f5413a2331e784635dbec52f2fef2dba3ca1a00`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Jun 2026 23:10:23 GMT
ENV _BASH_COMMIT=8085ee139645391bb392cc06dd25717238b65455
# Tue, 09 Jun 2026 23:10:23 GMT
ENV _BASH_VERSION=devel-20260608
# Tue, 09 Jun 2026 23:10:23 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Jun 2026 23:11:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Jun 2026 23:11:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jun 2026 23:11:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jun 2026 23:11:24 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7461922403e7ea9d88a94ce3e01df69cdc262a6df3e7b576816407c18e2afd`  
		Last Modified: Tue, 09 Jun 2026 23:11:43 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718b3cf4d61265420a51b574cb53338ee02e175787d8f8da34c2bb208161d40d`  
		Last Modified: Tue, 09 Jun 2026 23:11:44 GMT  
		Size: 3.1 MB (3132692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e4f6c28601bd254dbb86fd7e9447224a34a1f8201fc4e42855c282525ca5bc`  
		Last Modified: Tue, 09 Jun 2026 23:11:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel-20260608-alpine3.24` - unknown; unknown

```console
$ docker pull bash@sha256:f6b2824750a5ec3b412067d6c838ce8c4c3db7b720c785e47596c672334c40d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89e037193b54e52cec83de7d85dde6b0f56feaf29414e90e71b7b115ce03cd1`

```dockerfile
```

-	Layers:
	-	`sha256:e22f1788dc461ca761f978d0b10f10ece51957a8ef071c3d0a220db7e9203ad3`  
		Last Modified: Tue, 09 Jun 2026 23:11:43 GMT  
		Size: 116.5 KB (116477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57109c0bce1b99d1025787b049100da4e71dfec9a55bb8c282dfcec737748d4`  
		Last Modified: Tue, 09 Jun 2026 23:11:43 GMT  
		Size: 18.1 KB (18084 bytes)  
		MIME: application/vnd.in-toto+json
