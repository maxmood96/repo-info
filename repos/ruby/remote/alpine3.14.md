## `ruby:alpine3.14`

```console
$ docker pull ruby@sha256:876df894fdb2c3c8e829e8dff2e12838363332716563af9fd745262b67d2cf38
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

### `ruby:alpine3.14` - linux; amd64

```console
$ docker pull ruby@sha256:c2072846fec42f6a619c2b1f6133a318423dc3e1bc984b2f1ad6999d9e1bacd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36013055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea746c969e9e6e7fcf48a7b7b96b0b885d202fd674121a8268746f24953b6a04`
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
# Tue, 05 Apr 2022 03:21:33 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:32:24 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:32:25 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:34:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:34:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:34:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:34:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:34:56 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:34:56 GMT
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
	-	`sha256:72dc36b13b4dbb426a88fe53f878298111856ae01d1027f58529c8a71f2353c8`  
		Last Modified: Tue, 12 Apr 2022 19:15:54 GMT  
		Size: 29.6 MB (29561888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c08a78e9ec9aae561ac0d3dcfa9faabb5d91a50b97ef0a72913f93f04b1cdea`  
		Last Modified: Tue, 12 Apr 2022 19:15:51 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.14` - linux; arm variant v6

```console
$ docker pull ruby@sha256:3d18da58f8844477edf586df2f288390af466006a199e9ce3e93ac761dc8a6c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34191297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e12b6206cd9077d0bf65a5ae6b23baae60b80e3433674aba4c9f4446ac1376eb`
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
# Tue, 05 Apr 2022 01:58:49 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:55:06 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:55:07 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:59:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:59:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:59:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:59:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:59:38 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:59:38 GMT
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
	-	`sha256:8d7855f02fb2a69fca374093d71eabf225bcedacd90fea2e42cf114fbc9516d3`  
		Last Modified: Tue, 12 Apr 2022 19:30:03 GMT  
		Size: 28.2 MB (28155033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38963f295f582d08802635db1f1cbbb88a770c34d11ab20a80677ae30f532287`  
		Last Modified: Tue, 12 Apr 2022 19:29:50 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.14` - linux; arm variant v7

```console
$ docker pull ruby@sha256:fabdc4207bd02c3d670ef4419f5257b7808115903da61a9b47e467568acc6f38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33756356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf1611ba14142699b35c256b82503add82d3c3cb0d41f94054a0eaab5c308a3`
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
# Tue, 05 Apr 2022 03:29:21 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 19:24:33 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 19:24:34 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 19:28:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 19:28:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 19:28:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 19:28:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 19:28:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 19:28:42 GMT
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
	-	`sha256:3079376204da13723a7f9e334b962c63d147edb497f8bd15b47c2996338b6446`  
		Last Modified: Tue, 12 Apr 2022 20:59:12 GMT  
		Size: 28.0 MB (28047715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf01971ff7f598f6984c280ced0d6a8177e58ef6e7bd7f597a599977cfc14d1`  
		Last Modified: Tue, 12 Apr 2022 20:59:04 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.14` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:fffc8b2893d1a6e6979e1587ac22330f4cc2f7950a1e165f791363eda30c2bae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35255894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:358f43c00d38961492819968a0149d9d125fb9c4648dde5dcf1fd909abdccb9e`
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
# Tue, 05 Apr 2022 02:20:04 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:53:15 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:53:16 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:55:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:55:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:55:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:55:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:55:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:55:38 GMT
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
	-	`sha256:3f3ba722d420ec80b9cad312cc634d828630d7cc48365bc3068bb316a62f6e3c`  
		Last Modified: Tue, 12 Apr 2022 19:39:57 GMT  
		Size: 28.9 MB (28918569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4fe51a30a174ca9e84a0fdbeda7f6920e29db79146fc04365c7ddc9108cb2a`  
		Last Modified: Tue, 12 Apr 2022 19:39:54 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.14` - linux; 386

```console
$ docker pull ruby@sha256:761cfc758aab94d2cd12e6a2ba486a176256cd5a6ac8411545f26c6e58730735
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34658850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f683beb01acb9e0bed3e0b8aeb0f168e2103d71e862563cffb9888c5e39663f1`
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
# Tue, 05 Apr 2022 01:52:33 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:51:36 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:51:37 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:53:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:53:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:53:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:53:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:54:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:54:01 GMT
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
	-	`sha256:e35726b922480607c8297ba0655b15d38e5e14df634012deefbce4456aec1519`  
		Last Modified: Tue, 12 Apr 2022 19:38:21 GMT  
		Size: 28.2 MB (28166684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c794d682bed0bf5f15ab7dfd83601b5de126951262b3500af7733a483295cdcb`  
		Last Modified: Tue, 12 Apr 2022 19:38:13 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.14` - linux; ppc64le

```console
$ docker pull ruby@sha256:4990d2f34f9c70d91ba2b1af0165475b764f55cbd3e7ccbeab5f3c875a1cc4bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36211078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c7cf0228cbdae8e90b71e6d0fb91359ac63c7984deaf545d4f94ddcf465496`
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
# Tue, 05 Apr 2022 05:55:05 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 19:24:40 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 19:24:44 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 19:28:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 19:28:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 19:28:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 19:28:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 19:28:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 19:28:21 GMT
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
	-	`sha256:0a7f0077a563018deadeefdcf48edf2b078e23e9689747a3d0ec82b943b502a7`  
		Last Modified: Tue, 12 Apr 2022 21:17:51 GMT  
		Size: 29.6 MB (29620559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c1a6f08228ca7e8f4c99032b95d3f9057ae850069415a234785990c73cf1f5`  
		Last Modified: Tue, 12 Apr 2022 21:17:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.14` - linux; s390x

```console
$ docker pull ruby@sha256:355e0c136ee00d03c5e7e1daa33c4ee2fbcbe3cad0c3034fb4eb1a16b188d906
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35712697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f98fcb20a146bcdf8eea0419814767ab3d137127f3f2b27c47f7bd5b8d4ab72`
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
# Tue, 05 Apr 2022 03:14:04 GMT
ENV RUBY_MAJOR=3.1
# Tue, 12 Apr 2022 18:56:55 GMT
ENV RUBY_VERSION=3.1.2
# Tue, 12 Apr 2022 18:56:55 GMT
ENV RUBY_DOWNLOAD_SHA256=ca10d017f8a1b6d247556622c841fc56b90c03b1803f87198da1e4fd3ec3bf2a
# Tue, 12 Apr 2022 18:59:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 12 Apr 2022 18:59:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 Apr 2022 18:59:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 Apr 2022 18:59:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Apr 2022 18:59:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 12 Apr 2022 18:59:13 GMT
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
	-	`sha256:28ef1fb672bef6fbafa92b179322ac6ebccc577097cfd6d52941e615fc4e9aba`  
		Last Modified: Tue, 12 Apr 2022 20:01:57 GMT  
		Size: 29.4 MB (29382832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d30ee9128b8609d2623ccb52f64329b7afda6b1ff28232b6e6b30cd73139a1`  
		Last Modified: Tue, 12 Apr 2022 20:01:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
