## `ruby:alpine3.11`

```console
$ docker pull ruby@sha256:7150eaf4eef7e2261c15d3c8b229ebeb40e701880c8d5628403c374e475d0ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ruby:alpine3.11` - linux; amd64

```console
$ docker pull ruby@sha256:38b28c79d63f99fe670437c881c9e37205e333fed2c473b156919418c5bb76ae
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27197497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850bf24f9cfea42cc85a85d296f66217819484e18d8ebc3bee443bde17594d80`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:49 GMT
ADD file:8ed80010e443da19d72546bcee9a35e0a8d244c72052b1994610bf5939d479c2 in / 
# Thu, 17 Dec 2020 00:19:49 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 15:29:18 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 17 Dec 2020 15:29:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Dec 2020 15:29:20 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 15:29:20 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Dec 2020 15:29:20 GMT
ENV RUBY_VERSION=2.7.2
# Thu, 17 Dec 2020 15:29:20 GMT
ENV RUBY_DOWNLOAD_SHA256=1b95ab193cc8f5b5e59d2686cb3d5dcf1ddf2a86cb6950e0b4bdaae5040ec0d6
# Thu, 17 Dec 2020 15:35:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Dec 2020 15:35:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Dec 2020 15:35:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Dec 2020 15:35:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Dec 2020 15:35:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Dec 2020 15:35:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0a6724ff3fcd51338afdfdc2b1d4ffd04569818e31efad957213d67c29b45101`  
		Last Modified: Thu, 17 Dec 2020 00:20:26 GMT  
		Size: 2.8 MB (2814864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac597affe204b012db965ae97c5ac133819ec2fdd7c0847a41c976fae919683`  
		Last Modified: Thu, 17 Dec 2020 15:57:51 GMT  
		Size: 1.1 MB (1133799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2877e2a04786e33c2a6e54226bcf38e83a296e16d1a154066a1cc183f37d1a`  
		Last Modified: Thu, 17 Dec 2020 15:57:51 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b12aba1d7feace81058d7720b063ad342b5db3c5903acf137fe57abe7d099a8`  
		Last Modified: Thu, 17 Dec 2020 15:58:00 GMT  
		Size: 23.2 MB (23248498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199631f239de17dd8ed8ca955f2333550931f70029e55f38bb7daa28b5fc8d3d`  
		Last Modified: Thu, 17 Dec 2020 15:57:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.11` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:8fe5a1f34e9d63445d171cdf34860d44e5c49542fce186d30b6358169a8d72ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26975349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdfa541333fe48efd7edfe35392954bcadf4712a7d5472f8ae2a685d10460ed`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:37 GMT
ADD file:47bb1b85a4eb4d0b355ae89ec5c71c09e2c2b7e21e1851a2896365eb17134f57 in / 
# Wed, 16 Dec 2020 23:40:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 09:23:50 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 17 Dec 2020 09:23:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Dec 2020 09:23:54 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 09:23:54 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Dec 2020 09:23:55 GMT
ENV RUBY_VERSION=2.7.2
# Thu, 17 Dec 2020 09:23:56 GMT
ENV RUBY_DOWNLOAD_SHA256=1b95ab193cc8f5b5e59d2686cb3d5dcf1ddf2a86cb6950e0b4bdaae5040ec0d6
# Thu, 17 Dec 2020 09:26:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Dec 2020 09:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Dec 2020 09:26:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Dec 2020 09:27:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Dec 2020 09:27:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Dec 2020 09:27:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:20d8a246443a66e74e17f2a0e81a51fe774876ca0c2676691c37ee1b0e4d3cd5`  
		Last Modified: Wed, 16 Dec 2020 23:41:20 GMT  
		Size: 2.7 MB (2725216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79ba03b385b54cf0be0de393d22d4c725322049e85943f36c05fa2f51c6d9ae6`  
		Last Modified: Thu, 17 Dec 2020 09:42:39 GMT  
		Size: 1.1 MB (1142317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddd29e0532c936941968d50873b4e7bf1b58b3b841f7edf6022cd75cee7768e`  
		Last Modified: Thu, 17 Dec 2020 09:42:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea2be73d28c740b9d63fcc8d70df0f5188cf71ce4516eae2c572e0059897fcc`  
		Last Modified: Thu, 17 Dec 2020 09:42:43 GMT  
		Size: 23.1 MB (23107420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722b24dc841e3e8c1844010a836ce529c84866c38e3cdda63bee6d74306ffb5a`  
		Last Modified: Thu, 17 Dec 2020 09:42:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.11` - linux; 386

```console
$ docker pull ruby@sha256:ce33d0fd26559f6fecc6e417ebc4bfdd9bb7ec265d8032c0c5d1af2d50b15bf8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26623732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92976530fcd432f729236ca0a8f33d7f53ad49ce48d994a746a21ab993099234`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:39 GMT
ADD file:c8f5b26cfa9b90dfe6ca805f2101bd199c87b93faed2af74df0cbe54ea28fa6d in / 
# Thu, 17 Dec 2020 00:38:39 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 07:32:29 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 17 Dec 2020 07:32:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Dec 2020 07:32:30 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 07:32:30 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Dec 2020 07:32:30 GMT
ENV RUBY_VERSION=2.7.2
# Thu, 17 Dec 2020 07:32:30 GMT
ENV RUBY_DOWNLOAD_SHA256=1b95ab193cc8f5b5e59d2686cb3d5dcf1ddf2a86cb6950e0b4bdaae5040ec0d6
# Thu, 17 Dec 2020 07:36:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Dec 2020 07:36:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Dec 2020 07:36:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Dec 2020 07:36:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Dec 2020 07:36:13 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Dec 2020 07:36:13 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:60519712d04c07db59906a2e14fa87c037b6504d612ba116ea1ef94ae08a650b`  
		Last Modified: Thu, 17 Dec 2020 00:39:32 GMT  
		Size: 2.8 MB (2810512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57586e8a8a48fcc75ac997408329a76f8d6732491a8d1ad93ba3777649981372`  
		Last Modified: Thu, 17 Dec 2020 07:52:50 GMT  
		Size: 1.2 MB (1171603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e9c4094aa5bad0484dc3a5bbae106a6382893bd8391bc712fd9073b0690ddd`  
		Last Modified: Thu, 17 Dec 2020 07:52:49 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bcc927d15d8f34d9276e7ac1f3119cd4daaceedc4b6b5fe91d8fc0b37b6fd5`  
		Last Modified: Thu, 17 Dec 2020 07:52:54 GMT  
		Size: 22.6 MB (22641280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daca65e629c6a94551a49dc7a887b1982c7c0007e58cbc165a994ac00f61068d`  
		Last Modified: Thu, 17 Dec 2020 07:52:49 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:alpine3.11` - linux; ppc64le

```console
$ docker pull ruby@sha256:93362a503c8f2607d6a3601876341713b1cdd2c72e9386f8e0acc35c7555ba60
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27938007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7a31a26cee8457fbbb3664dd791bbdf660332158da23bced815aaaaf6f80af`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Dec 2020 00:21:03 GMT
ADD file:4a7a7b8454234532546faed6d4d392f006f235e86744822034cb829a16205d11 in / 
# Thu, 17 Dec 2020 00:21:06 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 09:06:50 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 17 Dec 2020 09:06:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Dec 2020 09:07:02 GMT
ENV LANG=C.UTF-8
# Thu, 17 Dec 2020 09:07:05 GMT
ENV RUBY_MAJOR=2.7
# Thu, 17 Dec 2020 09:07:10 GMT
ENV RUBY_VERSION=2.7.2
# Thu, 17 Dec 2020 09:07:14 GMT
ENV RUBY_DOWNLOAD_SHA256=1b95ab193cc8f5b5e59d2686cb3d5dcf1ddf2a86cb6950e0b4bdaae5040ec0d6
# Thu, 17 Dec 2020 09:10:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Dec 2020 09:10:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Dec 2020 09:10:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Dec 2020 09:10:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Dec 2020 09:10:48 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Dec 2020 09:10:55 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2c090b1a59445fb94c5fb14edf51af12a8f8bc2259535b08191f26ea84a7bb05`  
		Last Modified: Thu, 17 Dec 2020 00:21:49 GMT  
		Size: 2.8 MB (2821993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056e4cde0f3e10c168bfb3132fdb6345789a0352888b31e5ed07eafe16bd9f00`  
		Last Modified: Thu, 17 Dec 2020 09:27:22 GMT  
		Size: 1.2 MB (1215410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b52ddf286a4a73ea6a12476f61003cf4f2c47cbc97a7567f350876c58f44005`  
		Last Modified: Thu, 17 Dec 2020 09:27:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecb5cccbc6a4c9acc2cb629d5664bfb0da85ab7a85aee9b9876b26fd93f90d2`  
		Last Modified: Thu, 17 Dec 2020 09:27:25 GMT  
		Size: 23.9 MB (23900209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce76901f581b69c770d8874186a704349ecce7ee81c9dcbeeebc4361c6686c7`  
		Last Modified: Thu, 17 Dec 2020 09:27:22 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
