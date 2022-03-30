## `ruby:3-alpine3.14`

```console
$ docker pull ruby@sha256:7e428ee3c78e4aa39ad403e132ddefcda2c3b9a5b541ec7225cdde7acf8202ae
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

### `ruby:3-alpine3.14` - linux; amd64

```console
$ docker pull ruby@sha256:6e95f6bbc1148b184aaae3307946db95f72f996dd72739eac1e9558e93c3c5b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.0 MB (36012176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb700e16742742264badccc9682ed086c2981a17b26a9c14dc8ec1b2311a1e93`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:39:26 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 29 Mar 2022 10:39:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 10:39:26 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 10:39:26 GMT
ENV RUBY_MAJOR=3.1
# Tue, 29 Mar 2022 10:39:26 GMT
ENV RUBY_VERSION=3.1.1
# Tue, 29 Mar 2022 10:39:27 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Tue, 29 Mar 2022 10:43:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 29 Mar 2022 10:43:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 29 Mar 2022 10:43:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 29 Mar 2022 10:43:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 10:43:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 29 Mar 2022 10:43:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba338dd6a7be1d47c904ee0d289b25ed879a572d1a706e96b9716caa84a32cd`  
		Last Modified: Tue, 29 Mar 2022 11:20:10 GMT  
		Size: 3.6 MB (3632328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d728a07297a2dc913ceb1ce5e861f4fdec0b4af013ec0b127fb4335b2a16b8a`  
		Last Modified: Tue, 29 Mar 2022 11:20:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c8f3afb54136f59c4b9bcb344a674c7bd72fa42c05ebb7efcc649c30c3f2ca`  
		Last Modified: Tue, 29 Mar 2022 11:20:12 GMT  
		Size: 29.6 MB (29561098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1074c0b7a306541d24531300ba5f09f2844ceecb7568895dd80467deb4e80717`  
		Last Modified: Tue, 29 Mar 2022 11:20:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; arm variant v6

```console
$ docker pull ruby@sha256:fb6c5fead68bc35ecdd224aec1bcc06af93b2c6910b5ebb8b34ab36118d3b32d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.2 MB (34191368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7444d5687ef9559abbe477ca86e8600425a1b5e793cc830281a00e0726a6b82`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:49:46 GMT
ADD file:9670f4f7de6a9b8eb844e418daedd0dbad90009126790eb65e246b29cac5ea47 in / 
# Tue, 29 Mar 2022 00:49:46 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 12:44:32 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 29 Mar 2022 12:44:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 12:44:33 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 12:44:34 GMT
ENV RUBY_MAJOR=3.1
# Tue, 29 Mar 2022 12:44:34 GMT
ENV RUBY_VERSION=3.1.1
# Tue, 29 Mar 2022 12:44:35 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Tue, 29 Mar 2022 12:48:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 29 Mar 2022 12:48:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 29 Mar 2022 12:48:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 29 Mar 2022 12:49:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 12:49:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 29 Mar 2022 12:49:02 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:79f5c9df0b90097bae07a9861e9e0e3f52a16b0bfde2793c4e14ad033cfb47f4`  
		Last Modified: Tue, 29 Mar 2022 00:51:45 GMT  
		Size: 2.6 MB (2626017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e2b364b0344d9e4df55e792f6ce3bad413c9b33b29be808ebb04d7217c4a53`  
		Last Modified: Tue, 29 Mar 2022 13:18:01 GMT  
		Size: 3.4 MB (3409759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c080f7d53d091fa19f23aa6cd78c9a46f962d03fce200524e113e9424a5ec486`  
		Last Modified: Tue, 29 Mar 2022 13:17:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6101a76aaeea607bfe778e8bbdfe37e88b01298fe511b002a8d96b0f3c2a9be3`  
		Last Modified: Tue, 29 Mar 2022 13:18:12 GMT  
		Size: 28.2 MB (28155198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaee601323da416f54e0ebdabbcbe54219325e4ca38c8e436259fd5358107cb`  
		Last Modified: Tue, 29 Mar 2022 13:17:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; arm variant v7

```console
$ docker pull ruby@sha256:55dcea0a2dfc767f2ba3613fc59bd80f98fc1769dff192f2c67c8ee5ed15f625
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.8 MB (33760096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b088af0dc9501664830c4986748c00292254878da926e06871c5a2647194a3f0`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 17:21:06 GMT
ADD file:c25fcf153ea349f64e08a1bd0756ce550f2a081ad56cc40c89027d85d1bc26da in / 
# Thu, 17 Mar 2022 17:21:06 GMT
CMD ["/bin/sh"]
# Fri, 18 Mar 2022 12:51:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 18 Mar 2022 12:51:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 18 Mar 2022 12:51:25 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 12:51:26 GMT
ENV RUBY_MAJOR=3.1
# Fri, 18 Mar 2022 12:51:26 GMT
ENV RUBY_VERSION=3.1.1
# Fri, 18 Mar 2022 12:51:27 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Fri, 18 Mar 2022 12:55:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 18 Mar 2022 12:55:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 18 Mar 2022 12:55:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 18 Mar 2022 12:55:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 12:55:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 18 Mar 2022 12:55:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c3a1157c36d8d156f7664fa098212ab2149a64bcb59767cdf4595a86617c17fd`  
		Last Modified: Thu, 17 Mar 2022 17:22:45 GMT  
		Size: 2.4 MB (2430456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0131dad5781fb997af9b3f3e5063248a5c95bf495a4a106d4b5cc25176121051`  
		Last Modified: Fri, 18 Mar 2022 13:56:23 GMT  
		Size: 3.3 MB (3280076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf39a755d92a89f881e64fe80daa0410bb1effe4b633d8bcf688dc8a135957ba`  
		Last Modified: Fri, 18 Mar 2022 13:56:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398a43bfd78b5e5feff4329cf49933c95af1747ae63d9472de6ece86e1a2f9dc`  
		Last Modified: Fri, 18 Mar 2022 13:56:33 GMT  
		Size: 28.0 MB (28049169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd52b74aa0599ea459a2a3dab44b5da113eaa9dc3e555803e46666fd1554191`  
		Last Modified: Fri, 18 Mar 2022 13:56:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:0ef13640951665e27dbdddcd6d03cf4ffa2d76cd32d98564bfb85d98fc2ca488
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35255273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:350ecbb383f2ae26b791261576cc3521a87da52ac87e34d19dbeff2923ec18fb`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 20:19:10 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 20:19:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 20:19:12 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 20:19:13 GMT
ENV RUBY_MAJOR=3.1
# Thu, 17 Mar 2022 20:19:14 GMT
ENV RUBY_VERSION=3.1.1
# Thu, 17 Mar 2022 20:19:15 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Thu, 17 Mar 2022 20:21:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 20:21:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 20:21:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 20:21:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 20:21:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 20:21:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51423f003b4a30e1c802d94a05186a9e33c962bffbfcc00d8fa8be148e387cee`  
		Last Modified: Thu, 17 Mar 2022 20:52:53 GMT  
		Size: 3.6 MB (3619428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4c434ff7766b761a53f6b99d455bc705f3e6a44a015e5d6b257fbf4f325d09`  
		Last Modified: Thu, 17 Mar 2022 20:52:52 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb4686882251cdbc40b6b08bf4b37dca7c0a6bea4192b58eca4b68a9aea9a5f`  
		Last Modified: Thu, 17 Mar 2022 20:52:55 GMT  
		Size: 28.9 MB (28919621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c625d085c9e4dd81a067fc10ae2b2fd452be05b364c4c493a0981277039799`  
		Last Modified: Thu, 17 Mar 2022 20:52:52 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; 386

```console
$ docker pull ruby@sha256:e0488b34ed99a8ac8eacbd8e8b1d5cc575b126d2271e3ec9e418c7881e07373b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34658963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0244649396d32b1854cf6a42e2aa2e3def902befc1cdf770a399ba7b9537b13`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:38:40 GMT
ADD file:b779b35f4afe33387545e54afc23f09a30d43ad4817cc92ed6b083099748b3cb in / 
# Tue, 29 Mar 2022 00:38:40 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 10:05:32 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 29 Mar 2022 10:05:33 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 10:05:34 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 10:05:35 GMT
ENV RUBY_MAJOR=3.1
# Tue, 29 Mar 2022 10:05:36 GMT
ENV RUBY_VERSION=3.1.1
# Tue, 29 Mar 2022 10:05:37 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Tue, 29 Mar 2022 10:07:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 29 Mar 2022 10:07:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 29 Mar 2022 10:07:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 29 Mar 2022 10:07:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 10:08:00 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 29 Mar 2022 10:08:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ff47816780f28cb5e3d0a86624e638d039b84373892ba3065b1ff9cd4b55b356`  
		Last Modified: Tue, 29 Mar 2022 00:39:52 GMT  
		Size: 2.8 MB (2821065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02f3fdcf5a65e7b2cc3c89f567bae48e0ea81609f184673788d311cfd1ff362`  
		Last Modified: Tue, 29 Mar 2022 10:39:34 GMT  
		Size: 3.7 MB (3670513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3851e5fee2f9219038a7ac3dfcef35fce9dddfa4ade3b2c82b3fce08fd89c79`  
		Last Modified: Tue, 29 Mar 2022 10:39:33 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814bb69ded0858566e8e532e01629171e4435b2ea466fa6dbfc61db2d3418095`  
		Last Modified: Tue, 29 Mar 2022 10:39:37 GMT  
		Size: 28.2 MB (28167048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b18b1ff394970285e621ae012edab87116bdd2fe5fe2dadeb4c0b1f39514502`  
		Last Modified: Tue, 29 Mar 2022 10:39:33 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; ppc64le

```console
$ docker pull ruby@sha256:ca125fa8933051e011cada860757ec2dc560657467f6c54a2bbe567a2af7e8a3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36211422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e24a0d15302558ead50f06b76c93f8f9a87324b4b0033b299b982525f2a6cf8`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 29 Mar 2022 00:17:09 GMT
ADD file:b8083e0e4f4eed014eb6c7e881671b4c58af2bb5d05d9e60d0e1d217fab852a1 in / 
# Tue, 29 Mar 2022 00:17:12 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 20:34:39 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 29 Mar 2022 20:34:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 29 Mar 2022 20:34:46 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 20:34:49 GMT
ENV RUBY_MAJOR=3.1
# Tue, 29 Mar 2022 20:34:50 GMT
ENV RUBY_VERSION=3.1.1
# Tue, 29 Mar 2022 20:34:52 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Tue, 29 Mar 2022 20:38:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 29 Mar 2022 20:38:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 29 Mar 2022 20:38:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 29 Mar 2022 20:38:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 20:38:23 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Tue, 29 Mar 2022 20:38:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9b3885e1b82e42fc12e5a6c0b16a783379e4f96c6287d6b56d2aa2120d68c486`  
		Last Modified: Tue, 29 Mar 2022 00:18:44 GMT  
		Size: 2.8 MB (2814183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efcf053a9293ac964cd976fc81fa5f9c474e0d71eb9f59029bf1e9c4e0fa5da`  
		Last Modified: Tue, 29 Mar 2022 21:52:37 GMT  
		Size: 3.8 MB (3776072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d875f13c382fe91951f38e50acef288877887637e552d34ef21b04ebcd4b90c4`  
		Last Modified: Tue, 29 Mar 2022 21:52:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086983225f97ccdc64ef3b54030c790ae09de7b929018f551b8a406bbe6181cf`  
		Last Modified: Tue, 29 Mar 2022 21:52:41 GMT  
		Size: 29.6 MB (29620770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd62c52aa39d09d2ccc73cf58f0c0bc26a37f35c24f072c9f5743e385be50363`  
		Last Modified: Tue, 29 Mar 2022 21:52:36 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.14` - linux; s390x

```console
$ docker pull ruby@sha256:911c621ea8cde2f5be4165145029e9a0225b88b882f55f01861e5ad956f518e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35713771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1162f272067fc13ac272bd707e06cc9b873c1737d3c9ff25bda7d8c431053672`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Mar 2022 14:35:54 GMT
ADD file:cd4f7409c75ce2e40b46bbdeca277e2c4500aab51e1a7b6fa518c60e371f0a33 in / 
# Thu, 17 Mar 2022 14:35:55 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:54:17 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 17 Mar 2022 15:54:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 17 Mar 2022 15:54:18 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 15:54:18 GMT
ENV RUBY_MAJOR=3.1
# Thu, 17 Mar 2022 15:54:18 GMT
ENV RUBY_VERSION=3.1.1
# Thu, 17 Mar 2022 15:54:18 GMT
ENV RUBY_DOWNLOAD_SHA256=7aefaa6b78b076515d272ec59c4616707a54fc9f2391239737d5f10af7a16caa
# Thu, 17 Mar 2022 15:56:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 17 Mar 2022 15:56:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 17 Mar 2022 15:56:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 17 Mar 2022 15:56:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 15:56:27 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Thu, 17 Mar 2022 15:56:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1a9a9eea18bd912112f7ed42a3730393bafbb84387ab6790fe9358d09100f3a3`  
		Last Modified: Thu, 17 Mar 2022 14:36:47 GMT  
		Size: 2.6 MB (2605208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8910ce04a166727ce411aec06b1373524ca416945226e3acb2474abbee12c9e3`  
		Last Modified: Thu, 17 Mar 2022 16:23:54 GMT  
		Size: 3.7 MB (3725160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7137af0e926acc7dda6c84b96aac684bb66eaeebf68fdbd21537312e7251a144`  
		Last Modified: Thu, 17 Mar 2022 16:23:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78462df056803918964a4bb0592d8167f11637b18b6395efa083cb8b1bd3b354`  
		Last Modified: Thu, 17 Mar 2022 16:23:56 GMT  
		Size: 29.4 MB (29383006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ebaeb4786a184de91e77ba7e6752e4a979f879e9327d382eb363fc8681a52f`  
		Last Modified: Thu, 17 Mar 2022 16:23:53 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
