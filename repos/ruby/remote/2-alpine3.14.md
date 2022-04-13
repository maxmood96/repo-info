## `ruby:2-alpine3.14`

```console
$ docker pull ruby@sha256:a27b3ab5a2957e4a68cee78a137df4c502fde60b0899e56918ae79863ecba012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `ruby:2-alpine3.14` - linux; amd64

```console
$ docker pull ruby@sha256:9d488913f898ddb40fd839467108150427f3deeaadf6a6d939a941cb3fd49f21
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20477536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be4766e06ac5c815f892041a870d908699a453a8027949a19d741856f3c1b9e`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:13:52 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 05 Apr 2022 03:13:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 05 Apr 2022 03:13:53 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 03:35:21 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 18:57:35 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 18:57:36 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 18:59:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:59:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:59:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:59:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:59:21 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:59:21 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a481311129209687f586af3bd7110ea614355bfd7a6b459d1bb718cf0ead3fe`  
		Last Modified: Tue, 05 Apr 2022 03:46:57 GMT  
		Size: 3.6 MB (3632401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3451d03ed41de2372aaacdc51111f8fd73256b66da366816093bbe16a89334`  
		Last Modified: Tue, 05 Apr 2022 03:46:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2160385b9597b1601206481ff7d3e7e2bdc7530a7c924dc59985603257e2db7`  
		Last Modified: Tue, 12 Apr 2022 19:19:38 GMT  
		Size: 14.0 MB (14026369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0523000687a450ecfc3c15fb7296269494b146f43d1d532c2fe82030b00d2d8`  
		Last Modified: Tue, 12 Apr 2022 19:19:36 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.14` - linux; arm variant v6

```console
$ docker pull ruby@sha256:4f17528d9c8d5dbe1d8c5df4141a67b8b1e68c797a0343554de39a6cffd42e82
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19505789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2ed9c871590088ecf42e7a7cc0c32bbf7f4f75f2a1f625183edf0f2f2e16ce`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 01:49:38 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 05 Apr 2022 01:49:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 05 Apr 2022 01:49:40 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 02:16:34 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 19:13:32 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 19:13:32 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 19:17:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 19:17:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 19:17:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 19:17:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 19:17:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 19:17:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97161bd013762e1140bd1858eadf62d0bc3a47076b2038c6ee6a43f548ab78b`  
		Last Modified: Tue, 05 Apr 2022 02:32:11 GMT  
		Size: 3.4 MB (3409812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f8f374a42af1515a646e2c545a475ef065d092da220405c1b47bbcbadf8044`  
		Last Modified: Tue, 05 Apr 2022 02:32:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019846fd263d64a91a6855deb1eeb4e23f9ce979a30e81e4f2da0b5fbffeb435`  
		Last Modified: Tue, 12 Apr 2022 19:31:55 GMT  
		Size: 13.5 MB (13469525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b365a01e5acd4550dcb950753939fee0e1672bec2e7cd8c74470da6a00c26fad`  
		Last Modified: Tue, 12 Apr 2022 19:31:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.14` - linux; arm variant v7

```console
$ docker pull ruby@sha256:fb4e4cd80bc7f909086d330c740bb1f768592dc18eb6d4e9d29de24df17998db
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19062471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f701bcd5d681f18504e5f50c404119123a949480f88241c8271d924730eb9345`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:52 GMT
ADD file:97f7b59ed0e40e7771daab294820763a7bb86c843317be55725baf1cab39aa12 in / 
# Mon, 04 Apr 2022 23:57:52 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:19:24 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 05 Apr 2022 03:19:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 05 Apr 2022 03:19:26 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 03:47:06 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 20:15:49 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 20:15:50 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 20:19:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 20:19:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 20:19:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 20:19:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 20:19:10 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 20:19:11 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:380010979fdd8a9a4b0bf397034a27ec6cabe61d36e9e6d460ea986f0ddaef38`  
		Last Modified: Mon, 04 Apr 2022 23:59:45 GMT  
		Size: 2.4 MB (2427969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e847ad452980efdf07740ef9acbf4d037d40a5eb4be522c3a5fa9dd49468d40`  
		Last Modified: Tue, 05 Apr 2022 04:09:21 GMT  
		Size: 3.3 MB (3280276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64598c97662ba1360fab8dfec625b4ab0af1bc08be9987f28111e0618a595795`  
		Last Modified: Tue, 05 Apr 2022 04:09:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8158f91c02222c37201b34db303122febba2574f9b933199940c2376220d79f`  
		Last Modified: Tue, 12 Apr 2022 21:04:32 GMT  
		Size: 13.4 MB (13353830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698b36e9823fbd01e50f43a8e008035458a63a69bfeca6c4b9c90d2d0078ccec`  
		Last Modified: Tue, 12 Apr 2022 21:04:27 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:ecf78667415980615afad5b018f80d26314dd6f9a2f95578a433ba683be04153
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20195732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5e1bef781e6d10a54fe5bad4310443ecd86704b25b1fc6b03ef2f70c5a971f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 02:14:18 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 05 Apr 2022 02:14:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 05 Apr 2022 02:14:20 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 02:30:30 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 19:19:01 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 19:19:01 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 19:20:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 19:20:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 19:20:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 19:20:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 19:20:55 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 19:20:56 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e7cd1e159509fe49fafe061cfb64f6a5dc77d5c4a053d56edd8c789c53f739`  
		Last Modified: Tue, 05 Apr 2022 02:42:12 GMT  
		Size: 3.6 MB (3619598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3306f6709e512d13375007c4c3abbccc8b8899299f857701cd5335058f6843de`  
		Last Modified: Tue, 05 Apr 2022 02:42:11 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c12dc1af46106076da07f5704320fda224163ac03ae58568707a5f018fbf2ed`  
		Last Modified: Tue, 12 Apr 2022 19:44:05 GMT  
		Size: 13.9 MB (13858409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137120c001fae4e80698e03846ec0f7878485e95fa98bd05047c1650852a6e71`  
		Last Modified: Tue, 12 Apr 2022 19:44:03 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.14` - linux; 386

```console
$ docker pull ruby@sha256:d54234e1b8f248788b47ce47920185b0f070a716163bebec55d472956fb33929
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.8 MB (19829902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c181bd3518794c1065a36f84316c3dea6ea78e1cd006ebfe414911e54d62d3ec`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:32 GMT
ADD file:6508514d43b69774a3307679ef8f6dba0faf707e62ad6c6c1c8cf40d84e12d1d in / 
# Mon, 04 Apr 2022 23:38:32 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 01:46:45 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 05 Apr 2022 01:46:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 05 Apr 2022 01:46:47 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 02:02:47 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 19:17:11 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 19:17:12 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 19:18:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 19:18:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 19:18:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 19:18:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 19:18:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 19:18:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c11e5e1035714514f6e237dffd1836a4d03b48af64e55a8e08f9bd9e998e24a9`  
		Last Modified: Mon, 04 Apr 2022 23:39:35 GMT  
		Size: 2.8 MB (2821213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6931fd2572c80a6ca348513895c3bdffe1cd5da0ab1a582b4236cc8c6a0cb6a9`  
		Last Modified: Tue, 05 Apr 2022 02:14:45 GMT  
		Size: 3.7 MB (3670618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79fccdfd7d47a47935005771f056ac3695e500054c212695a30e687574c987e`  
		Last Modified: Tue, 05 Apr 2022 02:14:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2368d29f6576b0e63560427e327558d8a9c342182d1d3da160081647c0fe1d3`  
		Last Modified: Tue, 12 Apr 2022 19:42:45 GMT  
		Size: 13.3 MB (13337736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cf69409e90917daa7933ae6f20a8676f65b3d9f1e930fde7833bf4c310c74f`  
		Last Modified: Tue, 12 Apr 2022 19:42:43 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.14` - linux; ppc64le

```console
$ docker pull ruby@sha256:a31785773db664153d5f16f44922dbe5d8d5fdeddc8882c50cf809c24e46f9ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21084303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553eface861ed719f86e584047f5bc3ef253cb465dd9a9826bdb52ac7782fc81`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 Apr 2022 00:23:44 GMT
ADD file:0b9367758b91930d9d69fd3901262e3a696f7a9f6d9e209e35da83ea6e785837 in / 
# Tue, 05 Apr 2022 00:23:46 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 05:45:40 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 05 Apr 2022 05:45:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 05 Apr 2022 05:45:52 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 06:11:30 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 20:34:59 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 20:35:02 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 20:37:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 20:37:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 20:37:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 20:37:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 20:37:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 20:38:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ee5f6345565e7aeda814a5c097612cacb0a74186b1f01bf5199e1b812b5d3065`  
		Last Modified: Tue, 05 Apr 2022 00:25:06 GMT  
		Size: 2.8 MB (2814167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce078c88ab345c783bb2bf8dcf4fce85d5aeba26681815e001da7762f2812e01`  
		Last Modified: Tue, 05 Apr 2022 06:29:54 GMT  
		Size: 3.8 MB (3775956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba77811c2081ef3fb0dc6594fdfe1ca63263ee0b9f1152738ee29dacc258d737`  
		Last Modified: Tue, 05 Apr 2022 06:29:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8474ed2dc7eb8b147a2af46338cb305442205c2b34c93c6a5978aff056836084`  
		Last Modified: Tue, 12 Apr 2022 21:22:06 GMT  
		Size: 14.5 MB (14493784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f07ca4626be8912cc4d97f895c7d9649c6c4bbe95d7cfd13faa152a9ec567`  
		Last Modified: Tue, 12 Apr 2022 21:22:04 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.14` - linux; s390x

```console
$ docker pull ruby@sha256:a31b6b87ace19b58dd0376e97b8e07e901430399526a973b26ddd40df6399e9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20514966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182c2343e6312ad3d8f13e01625fc1b0ceea09c5f3cfb1c6d1a7f2cb0d52d535`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 04 Apr 2022 23:41:47 GMT
ADD file:0f70e0f0075bee67acb44e5ef01bf6b9df1f69a25b7aa6fd15bd5bb6ec5bcc9f in / 
# Mon, 04 Apr 2022 23:41:48 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 03:08:40 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 05 Apr 2022 03:08:40 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 05 Apr 2022 03:08:40 GMT
ENV LANG=C.UTF-8
# Tue, 05 Apr 2022 03:23:48 GMT
ENV RUBY_MAJOR=2.7
# Tue, 12 Apr 2022 19:23:58 GMT
ENV RUBY_VERSION=2.7.6
# Tue, 12 Apr 2022 19:23:59 GMT
ENV RUBY_DOWNLOAD_SHA256=54dcd3044726c4ab75a9d4604720501442b229a3aed6a55fe909567da8807f24
# Tue, 12 Apr 2022 19:27:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		s390x | armhf | armv7) 			apk add --no-cache libucontext-dev; 			export LIBS='-lucontext'; 			;; 	esac; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 19:27:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 19:27:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 19:27:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 19:27:42 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 19:27:43 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6f6a6c77b1bd5dfb3e759efaa292f964f197ae4b96be74d80ef059f87317997a`  
		Last Modified: Mon, 04 Apr 2022 23:42:47 GMT  
		Size: 2.6 MB (2604075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12f62a049e08b2c143adc0ac789d99fc82da9785d291f585ba33aaf8aeef41e`  
		Last Modified: Tue, 05 Apr 2022 03:33:59 GMT  
		Size: 3.7 MB (3725392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d4564e21e57e7060ec39f1b2e7f0ef2284a73341e52034e7d944e39ae5fba3`  
		Last Modified: Tue, 05 Apr 2022 03:33:59 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f380be575aabe7e3c26a7251d9bd068df7f6b4f829b4e3a4ee7457cbf2a41bc4`  
		Last Modified: Tue, 12 Apr 2022 20:04:48 GMT  
		Size: 14.2 MB (14185104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43b13fe7a772102ecc15097720d161301fc6e122f855fba4abfdf848165218f`  
		Last Modified: Tue, 12 Apr 2022 20:04:47 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
