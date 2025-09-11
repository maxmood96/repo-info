## `bash:devel`

```console
$ docker pull bash@sha256:3035871c50f24d6e9e73107c3d72388e75bdb189532cfa29b503fb27d77b3ff7
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
$ docker pull bash@sha256:806bc775c269590b38c49f694aaeca10b743e7788f01e34f8a41c260ad69128a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6799277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1955c3813dbf48748d532e8c11c19f2e8b05a638c2f53ab8a210f9a423e58f24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 04:26:14 GMT
ENV _BASH_COMMIT=a451bfc3f57201bc0933b62c2fb721940a4c33f5
# Tue, 09 Sep 2025 04:26:14 GMT
ENV _BASH_VERSION=devel-20250904
# Tue, 09 Sep 2025 04:26:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 04:26:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42d6eb12a14bc38ac10fe7885ab6a74455243d9bfd9bfdb888de5cfed1b3e1b`  
		Last Modified: Wed, 10 Sep 2025 23:33:43 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e45cf97a9f3d90546e8795de99fbca1da68c8a5117efe2c388ed38bf578dfd`  
		Last Modified: Wed, 10 Sep 2025 23:33:43 GMT  
		Size: 3.0 MB (2998799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b244c0d22c4f786afe1ac0d95c121d381967556b204f575e5c5aaefe7d7d62d9`  
		Last Modified: Wed, 10 Sep 2025 23:33:43 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:1d2b0627bdc810580ffac5bc4de12a56fd41892fafeb3860ceebe83cb14f7350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 KB (136600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a8b12f664b7f82f8853061a3898002bbcc91b941ca1f49e85c44a9d31ec64e`

```dockerfile
```

-	Layers:
	-	`sha256:cd18f31be3aa2bb6dcd85e423d1352a50771a7a5269ae1559a825f9ad736a4d6`  
		Last Modified: Thu, 11 Sep 2025 00:02:37 GMT  
		Size: 118.4 KB (118429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcc716412065011a94e7033c58e250f7908805515d3c6a127905a5139613fa9a`  
		Last Modified: Thu, 11 Sep 2025 00:02:38 GMT  
		Size: 18.2 KB (18171 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v6

```console
$ docker pull bash@sha256:5f501466eaddd6951fa3be7232105f13e700fdf864ac7536b5768080d72fbe6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a7d9b2dd85d2f307e10a527e32c21c13185630bd87cbd0f198fbea4a7f9395`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 04:30:17 GMT
ENV _BASH_COMMIT=ab17ddb7af948ee6e1a6370aac4ee57b4179cd9c
# Tue, 26 Aug 2025 04:30:17 GMT
ENV _BASH_VERSION=devel-20250822
# Tue, 26 Aug 2025 04:30:17 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 26 Aug 2025 04:30:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Aug 2025 04:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 04:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Aug 2025 04:30:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf24ffdbb65ab87dd158bd5004e983e7efabb24f8ba37db7ffa1599cf714f638`  
		Last Modified: Tue, 22 Jul 2025 18:03:32 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cebab59bce13cd46eb658ba6f09c72f81eb705f52dcf06d88333607be84d95`  
		Last Modified: Wed, 27 Aug 2025 17:06:07 GMT  
		Size: 2.9 MB (2936817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3759c3afe4db1348dc44e264ad38bbd65fe786c55a841b69337050c7ebb320fa`  
		Last Modified: Wed, 27 Aug 2025 17:06:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:7c4dc64dee2e55f54719f67b35c73aac708b08d3973b527ab1d59a53c17780f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 KB (17948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5541eff86cfe3b814b2bc553112db5696c7f87e03fa7bd7ef3d6e957a06581`

```dockerfile
```

-	Layers:
	-	`sha256:daf326ffb55994a75c7f3da709e3869097a2588189be2be201cf1950ce888a47`  
		Last Modified: Wed, 27 Aug 2025 18:02:58 GMT  
		Size: 17.9 KB (17948 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm variant v7

```console
$ docker pull bash@sha256:76ba9fd976843bbdcc719cd087601a36d9a6cda732117b16fc2fd59334aa6b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6108764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4423ce39238160f7505f052f293431cebe9ec647c5b55d2f26feeff88a86491`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 04:30:17 GMT
ENV _BASH_COMMIT=ab17ddb7af948ee6e1a6370aac4ee57b4179cd9c
# Tue, 26 Aug 2025 04:30:17 GMT
ENV _BASH_VERSION=devel-20250822
# Tue, 26 Aug 2025 04:30:17 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 26 Aug 2025 04:30:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Aug 2025 04:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 04:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Aug 2025 04:30:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ae91dfc30adc9b9b9b47e1a22df7eee110ca2b5b6b2b08aff0eb4210851f6d`  
		Last Modified: Tue, 05 Aug 2025 20:59:50 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c32f725a591c1238c4f5f9b868b1dc013725ff58cb1a5cd3d68f710ba4f4`  
		Last Modified: Wed, 27 Aug 2025 17:06:12 GMT  
		Size: 2.9 MB (2888936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464b77c6dfbec93fb424b50c70a4b41aa3e89dca47e168db9d55249e4b9710fb`  
		Last Modified: Wed, 27 Aug 2025 17:06:17 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:8c0fbc8fbeda9f20e913cce895d950c597c418fa3d78a514d08e1280f11bcf03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 KB (136628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd0947ff0a2b8727894a33f35462d4782c6f4a88f15c0622ff26016fed1734c`

```dockerfile
```

-	Layers:
	-	`sha256:af0f2427115b8664c09647265e3fdb9b46b79134b036eaecec68244f3dc928c7`  
		Last Modified: Wed, 27 Aug 2025 18:03:01 GMT  
		Size: 118.5 KB (118465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fbc377355a87c6a1071e76bf018464d8e4fdd680200842dd9e40fb4a4cae71`  
		Last Modified: Wed, 27 Aug 2025 18:03:02 GMT  
		Size: 18.2 KB (18163 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; arm64 variant v8

```console
$ docker pull bash@sha256:b31c0ad9e9ead18c1c6cc2dc7287cbf8be551810194921d556ac2503b80af8af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d8e8bca8bd23ce0bf31365ba05dfe91c78235c30ab4d769587d8ec2cbb56ec3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 04:26:14 GMT
ENV _BASH_COMMIT=a451bfc3f57201bc0933b62c2fb721940a4c33f5
# Tue, 09 Sep 2025 04:26:14 GMT
ENV _BASH_VERSION=devel-20250904
# Tue, 09 Sep 2025 04:26:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 04:26:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362e03ce3b3a3f4f805eac128ba90b71c06ad3ea7a8ed6d2b154c918f52f1620`  
		Last Modified: Wed, 10 Sep 2025 23:33:59 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098e5e405a760e655781d5986edc119a0a60024aa79d2eff5425f8688cca52c4`  
		Last Modified: Wed, 10 Sep 2025 23:34:00 GMT  
		Size: 3.1 MB (3087052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea76596b6dc28ddb3b5fdf5bc4b31a58d5baf361733bb799706eab142c471c9`  
		Last Modified: Wed, 10 Sep 2025 23:33:59 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:58923f2ed771f2c1b741a69fe4904178c558516b56d3787e60b2e96696ebb8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 KB (136760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190c65b5b6e01a28678983cf9b16a99b7e911646df6ca3a175096af85183f698`

```dockerfile
```

-	Layers:
	-	`sha256:24a157e30dc802cf6665294fae217774cdcfa42b7a1ca9a678a01bdadc4230bf`  
		Last Modified: Thu, 11 Sep 2025 00:02:45 GMT  
		Size: 118.5 KB (118485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b593639268fa640eab994ee6286f809ff2d5f9db4dfdb4feebe8dfcd634bcdae`  
		Last Modified: Thu, 11 Sep 2025 00:02:45 GMT  
		Size: 18.3 KB (18275 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; 386

```console
$ docker pull bash@sha256:a2711da0c3223014e60cf968c570aae06c39f9b913798c5fd10abc3291ac02e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8fd5d40ce5c730a4df03bc02e09142d2d1c49b488cebf03263b7a8a10230d33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 04:26:14 GMT
ENV _BASH_COMMIT=a451bfc3f57201bc0933b62c2fb721940a4c33f5
# Tue, 09 Sep 2025 04:26:14 GMT
ENV _BASH_VERSION=devel-20250904
# Tue, 09 Sep 2025 04:26:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 04:26:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd2e35ab0ba1968b6442852a8b753ccaff6de68dec4866a2d406105a66e652e`  
		Last Modified: Wed, 10 Sep 2025 23:33:46 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b36b0740dc69e702ac3fb8beac7eea6406e9f7b824c1a8f2cccc5f7e81e61ac`  
		Last Modified: Wed, 10 Sep 2025 23:33:46 GMT  
		Size: 2.9 MB (2925496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2306b47cdf14e37dc90c1515043db1a69521bf84a5722bff50eccf9ceb5c4344`  
		Last Modified: Wed, 10 Sep 2025 23:33:46 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:2853a1a994ca627c83fb5ae37f741c590dac4723804a1c2198d349b679b8dae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.5 KB (136543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebcc227d96fa92c519e2b575de3703edc0fed1ad07342400498ae0b30d54051`

```dockerfile
```

-	Layers:
	-	`sha256:7e03f0219926e2f0a75b5ab3d313add4194c0766cb2330723539b85f46ee1fe2`  
		Last Modified: Thu, 11 Sep 2025 00:02:49 GMT  
		Size: 118.4 KB (118404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05da77d46da4fdf542ca6dd72a1da7e44156fc6cc57edb5151ee6deb7b068b9d`  
		Last Modified: Thu, 11 Sep 2025 00:02:49 GMT  
		Size: 18.1 KB (18139 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; ppc64le

```console
$ docker pull bash@sha256:c8bd4dd970142db03f508e98fa1ee8c0f482ace5ddfc76ab2fa973891de8655b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7000481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da5b6c50f5d5a3a96e3054267d61fb4ff5966dfab8f64f400ded7bdaeefccce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 04:26:14 GMT
ENV _BASH_COMMIT=a451bfc3f57201bc0933b62c2fb721940a4c33f5
# Tue, 09 Sep 2025 04:26:14 GMT
ENV _BASH_VERSION=devel-20250904
# Tue, 09 Sep 2025 04:26:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 04:26:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808855f34cf773f1a15be2e4c8001daa9698f55b2de8815f0415946f1583febf`  
		Last Modified: Wed, 10 Sep 2025 23:33:53 GMT  
		Size: 459.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc07136054a60363ef334e514225be798d4b0e0adcb17cd5ed2447a7b503185`  
		Last Modified: Wed, 10 Sep 2025 23:33:55 GMT  
		Size: 3.3 MB (3272576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6f0cde5a6f0fde1608d2bcb2b87dc2805037e68524cc129f9e07a09d15e4ae`  
		Last Modified: Wed, 10 Sep 2025 23:33:53 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:def6150a8b388a7c146b5982b2c402fdacc85147e3695084dc7fe6449b445983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 KB (134727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a4ae660711a43f36c0faaf343bbc0989c2c4a3f84cac26594821563546cc549`

```dockerfile
```

-	Layers:
	-	`sha256:d58450ed434bf38b4bddd4d5e9b1f48bdee825b192aaabc1a35eb7b79d0a6449`  
		Last Modified: Thu, 11 Sep 2025 00:02:53 GMT  
		Size: 116.5 KB (116512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba00cd583c631bf679ddfe0a0a9d5d34cd891286a909b3c089ecd7cbb07f03b5`  
		Last Modified: Thu, 11 Sep 2025 00:02:54 GMT  
		Size: 18.2 KB (18215 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; riscv64

```console
$ docker pull bash@sha256:dcfe7e319a3b11768eb0ba5df1815417bcca66569639d9e229dfb52fa1b29949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6461093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:010b56c553d448c5e5652a734409283a74002b3044586b99fe27e0f6647e9137`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 26 Aug 2025 04:30:17 GMT
ENV _BASH_COMMIT=ab17ddb7af948ee6e1a6370aac4ee57b4179cd9c
# Tue, 26 Aug 2025 04:30:17 GMT
ENV _BASH_VERSION=devel-20250822
# Tue, 26 Aug 2025 04:30:17 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 26 Aug 2025 04:30:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 26 Aug 2025 04:30:17 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 26 Aug 2025 04:30:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Aug 2025 04:30:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d13bcc41d7b7db4b9482cb455ffdc1fbf24e37a6203d336c9a5c3bcb775b3e7`  
		Last Modified: Fri, 22 Aug 2025 02:06:18 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77272932cd0736756eebd47b07ba3324aa3ea51c33d4617e6e46653d4275c2`  
		Last Modified: Thu, 28 Aug 2025 18:27:03 GMT  
		Size: 2.9 MB (2947498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184256a61d20f14e11dc0e9eeea6ddb5f25d8dab3d85f14a0d7944d0673da5cd`  
		Last Modified: Thu, 28 Aug 2025 18:27:03 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:4a78102c07ee2d43f53ebb0130b808d669ebe4686831b253a38141f52cb49830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4219de7150c5101a9de6d5d0bd914796bb0b3d705139876654cc0f1eb8f7af`

```dockerfile
```

-	Layers:
	-	`sha256:339e543bbc7c0c9e9c26f8d6297ee28e829d019f8354d6242bb92ec61ac9c69d`  
		Last Modified: Thu, 28 Aug 2025 21:02:54 GMT  
		Size: 116.5 KB (116508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f87479e13bf9d03465b1c57b56fc0d2f0dbad9f775c181e561db09cf5a1f8cd`  
		Last Modified: Thu, 28 Aug 2025 21:02:54 GMT  
		Size: 18.1 KB (18131 bytes)  
		MIME: application/vnd.in-toto+json

### `bash:devel` - linux; s390x

```console
$ docker pull bash@sha256:2d5255428d3883fb6a42f36dbb8368fe16ae228a5222c8399f31e3014c307def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6737130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119c879b54e63e2a39cbfb2b330524fa17c2e5515ea6fb50b9d7048c8ab8cd43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 09 Sep 2025 04:26:14 GMT
ENV _BASH_COMMIT=a451bfc3f57201bc0933b62c2fb721940a4c33f5
# Tue, 09 Sep 2025 04:26:14 GMT
ENV _BASH_VERSION=devel-20250904
# Tue, 09 Sep 2025 04:26:14 GMT
COPY alpine-strcpy.patch /usr/local/src/tianon-bash-patches/ # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		gcc 		libc-dev 		make 		ncurses-dev 		patch 		tar 	; 		wget -T2 -O bash.tar.gz "https://git.savannah.gnu.org/cgit/bash.git/snapshot/bash-$_BASH_COMMIT.tar.gz" || 		wget -O bash.tar.gz "https://github.com/tianon/mirror-bash/archive/$_BASH_COMMIT.tar.gz"; 		mkdir -p /usr/local/src/bash; 	tar 		--extract 		--file=bash.tar.gz 		--strip-components=1 		--directory=/usr/local/src/bash 	; 	rm bash.tar.gz; 		if [ -d bash-patches ]; then 		apk add --no-cache --virtual .patch-deps patch; 		for p in bash-patches/*; do 			patch 				--directory=/usr/local/src/bash 				--input="$(readlink -f "$p")" 				--strip=0 			; 			rm "$p"; 		done; 		rmdir bash-patches; 		apk del --no-network .patch-deps; 	fi; 		for p in /usr/local/src/tianon-bash-patches/*; do 		patch 			--directory=/usr/local/src/bash 			--input="$p" 			--strip=1 		; 	done; 		cd /usr/local/src/bash; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-readline 		--with-curses 		--without-bash-malloc 	|| { 		cat >&2 config.log; 		false; 	}; 	make -j "$(nproc)"; 	make install; 	cd /; 	rm -r /usr/local/src/bash; 		rm -rf 		/usr/local/share/doc/bash/*.html 		/usr/local/share/info 		/usr/local/share/locale 		/usr/local/share/man 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .bash-rundeps $runDeps; 	apk del --no-network .build-deps; 		[ "$(which bash)" = '/usr/local/bin/bash' ]; 	bash --version; 	bash -c 'help' > /dev/null # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Sep 2025 04:26:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Sep 2025 04:26:14 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139ad2e6975d7917a8c6b7c8f4bb03646c270442a7deb3d72ba449c8dfedb3a8`  
		Last Modified: Thu, 11 Sep 2025 00:45:33 GMT  
		Size: 461.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179d28b55ba8f14d342f69253ede5587cc9f8e6be0ce6587e59edc7e8e1b7cb5`  
		Last Modified: Thu, 11 Sep 2025 00:45:37 GMT  
		Size: 3.1 MB (3091363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddccf4e290bdf5322c6e35b13fdeaebea413f330d16ac33cd0c76a0329bd079`  
		Last Modified: Thu, 11 Sep 2025 00:45:45 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `bash:devel` - unknown; unknown

```console
$ docker pull bash@sha256:66c7212797b33f67413e99e19654e654a4a42fd228fcea36361bdafb99e624b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 KB (134649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e65de5fcc41eb30eb090dd5def83f884953a646e986e5a21408cf4b2dd8bc7f`

```dockerfile
```

-	Layers:
	-	`sha256:6c62990415fc23a363d911a84f54f4eb57dd051e366410fecbc6949bca33375f`  
		Last Modified: Thu, 11 Sep 2025 03:02:43 GMT  
		Size: 116.5 KB (116478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c16c521ddb8d157e29f29b375b2e672c6ffe96b7f9570f1f61cd0757fc9dfb9a`  
		Last Modified: Thu, 11 Sep 2025 03:02:43 GMT  
		Size: 18.2 KB (18171 bytes)  
		MIME: application/vnd.in-toto+json
