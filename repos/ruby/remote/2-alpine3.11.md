## `ruby:2-alpine3.11`

```console
$ docker pull ruby@sha256:bb12b3cbdb3fc915c29dc11445a7b0df6896b9598b8b5bba22e0eb4bf621913d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ruby:2-alpine3.11` - linux; amd64

```console
$ docker pull ruby@sha256:076b5950768b06ed292e57541a4804bdbe6b6c9f46ceaa43042ce6e1f9c584ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27188265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94a71e9022258d90aae3bebd10cdb199b43623801525150d68382f381afe8b9`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 00:55:02 GMT
RUN apk add --no-cache 		gmp-dev
# Tue, 24 Mar 2020 00:55:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 Mar 2020 00:55:04 GMT
ENV RUBY_MAJOR=2.7
# Wed, 01 Apr 2020 02:44:41 GMT
ENV RUBY_VERSION=2.7.1
# Wed, 01 Apr 2020 02:44:42 GMT
ENV RUBY_DOWNLOAD_SHA256=b224f9844646cc92765df8288a46838511c1cec5b550d8874bd4686a904fcee7
# Wed, 01 Apr 2020 02:47:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 01 Apr 2020 02:47:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 01 Apr 2020 02:47:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 01 Apr 2020 02:47:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 02:47:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 01 Apr 2020 02:47:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca28d9d22b9db22fe924a8dea99a0f2b6dd9bd713535ee3469f5d5d97f67871`  
		Last Modified: Tue, 24 Mar 2020 01:16:42 GMT  
		Size: 1.1 MB (1131843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46ee7bc75f66e10d9b504cc4dcdc6546a700b1c62a007d608e3774ad2edd402`  
		Last Modified: Tue, 24 Mar 2020 01:16:41 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1bb95caf3bb6afa55a9fd22946d1c3d7f5c3c5de93cd44ebbc2d1e6d1825fb`  
		Last Modified: Wed, 01 Apr 2020 03:48:57 GMT  
		Size: 23.3 MB (23252832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e95017f9d8ed520ceb9e60639cd97f32df83a0511d3490d49a24f436c2bd89`  
		Last Modified: Wed, 01 Apr 2020 03:48:54 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.11` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:0fc670d34e31cc81423a5c7090d0888db9a50bbd85e2b78d76b50fff7fd535a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26968850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4d509b75530c73e8ee40174413a32d4f5ddcdbb9dbb11efc62d15552c5189d`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Mar 2020 21:39:52 GMT
ADD file:746a5c3838a898d6acf7877552ff13d1ab40d0036ace7a662e7c747018315ddb in / 
# Mon, 23 Mar 2020 21:39:53 GMT
CMD ["/bin/sh"]
# Tue, 24 Mar 2020 05:32:56 GMT
RUN apk add --no-cache 		gmp-dev
# Tue, 24 Mar 2020 05:32:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 24 Mar 2020 05:32:58 GMT
ENV RUBY_MAJOR=2.7
# Wed, 01 Apr 2020 01:44:03 GMT
ENV RUBY_VERSION=2.7.1
# Wed, 01 Apr 2020 01:44:03 GMT
ENV RUBY_DOWNLOAD_SHA256=b224f9844646cc92765df8288a46838511c1cec5b550d8874bd4686a904fcee7
# Wed, 01 Apr 2020 01:46:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 01 Apr 2020 01:46:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 01 Apr 2020 01:47:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 01 Apr 2020 01:47:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Apr 2020 01:47:04 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Wed, 01 Apr 2020 01:47:05 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8a0637ca1ac98db4cf29f7632449c92801adc80cf0da2cd9c9e39882ce466561`  
		Last Modified: Mon, 23 Mar 2020 21:40:19 GMT  
		Size: 2.7 MB (2723139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685287eea26ef533d6c99437d78546783dfc714fbfbdbdfb086b38b081c120cb`  
		Last Modified: Tue, 24 Mar 2020 05:50:45 GMT  
		Size: 1.1 MB (1140912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8ce51b45bad417588608b59d28c6d353db6388527e0840adf0e6b4f5208bb6`  
		Last Modified: Tue, 24 Mar 2020 05:50:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc4eb0188d339d0d2426d1c6af45669fd1a8c55ec85852154c2773b56b487d9`  
		Last Modified: Wed, 01 Apr 2020 03:17:36 GMT  
		Size: 23.1 MB (23104404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46253083e139ecb51600f0ea891574db3dfe1da11aaadc6e0c46a4f1acce4a3c`  
		Last Modified: Wed, 01 Apr 2020 03:17:32 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.11` - linux; 386

```console
$ docker pull ruby@sha256:23794d5d0c5d643a5a8fa6e3ac77e90bbc362be136f189a6fe06f1dc77ac73e6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26627002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e451e95d9c3296452041f45f845cfad364c69568ba2ab114d975f76602da7db3`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:04 GMT
ADD file:63bd8a316cba8c404cc2e32a5120406c24aee8db3224c469a6077b941d900863 in / 
# Thu, 23 Apr 2020 21:16:04 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 08:33:37 GMT
RUN apk add --no-cache 		gmp-dev
# Fri, 24 Apr 2020 08:33:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 24 Apr 2020 08:33:38 GMT
ENV RUBY_MAJOR=2.7
# Fri, 24 Apr 2020 08:33:38 GMT
ENV RUBY_VERSION=2.7.1
# Fri, 24 Apr 2020 08:33:38 GMT
ENV RUBY_DOWNLOAD_SHA256=b224f9844646cc92765df8288a46838511c1cec5b550d8874bd4686a904fcee7
# Fri, 24 Apr 2020 08:37:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 24 Apr 2020 08:37:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 24 Apr 2020 08:37:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 24 Apr 2020 08:37:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 08:37:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 24 Apr 2020 08:37:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2826c1e79865da7e0da0a993a2a38db61c3911e05b5df617439a86d4deac90fb`  
		Last Modified: Thu, 23 Apr 2020 21:16:32 GMT  
		Size: 2.8 MB (2808418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badbfc2f321dd86048f9b75a361a17872b08bb72f999362b1b0ee380eaab2c80`  
		Last Modified: Fri, 24 Apr 2020 08:55:23 GMT  
		Size: 1.2 MB (1169346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ef0fa5210037c0700bdfdb24a85e5ba32af22fe77d8c25c175088cb24ee8f2`  
		Last Modified: Fri, 24 Apr 2020 08:55:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3796c3e74bac089bf93e6ece82a834f6f8adf77d96988ca65f3570e2a50d82c3`  
		Last Modified: Fri, 24 Apr 2020 08:55:27 GMT  
		Size: 22.6 MB (22648901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:252f8030202692cfd1dd85cee88f54cd4b9ee5c44365c1156ec0edb40a66c51b`  
		Last Modified: Fri, 24 Apr 2020 08:55:23 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.11` - linux; ppc64le

```console
$ docker pull ruby@sha256:a3de2d617573a55b31a943a723ca97af14ef92244ca36a23c74e179762537998
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.9 MB (27927012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869474d047cb04474907ac99041d81f5e50b871ee0267c521d2f47ae95a88c1c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 23 Apr 2020 20:39:04 GMT
ADD file:1aaebe252dfb1885e066fcbc84aaa915bae149c3608f19600855ad1d4f7450c1 in / 
# Thu, 23 Apr 2020 20:39:06 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 09:10:44 GMT
RUN apk add --no-cache 		gmp-dev
# Fri, 24 Apr 2020 09:10:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 24 Apr 2020 09:10:54 GMT
ENV RUBY_MAJOR=2.7
# Fri, 24 Apr 2020 09:10:57 GMT
ENV RUBY_VERSION=2.7.1
# Fri, 24 Apr 2020 09:11:02 GMT
ENV RUBY_DOWNLOAD_SHA256=b224f9844646cc92765df8288a46838511c1cec5b550d8874bd4686a904fcee7
# Fri, 24 Apr 2020 09:13:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 24 Apr 2020 09:13:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 24 Apr 2020 09:14:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 24 Apr 2020 09:14:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 09:14:12 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Fri, 24 Apr 2020 09:14:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9a8fdc5b698322331ee7eba7dd6f66f3a4e956554db22dd1e834d519415b4f8e`  
		Last Modified: Thu, 23 Apr 2020 20:41:33 GMT  
		Size: 2.8 MB (2821843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49693a1e6f48a395e6a546e95130a89b7eac0adbf2ad2cdda8d5e9c8cb9ead11`  
		Last Modified: Fri, 24 Apr 2020 09:33:35 GMT  
		Size: 1.2 MB (1214857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475454095cd08d1fef73f4c5ee3030c235b53c87fa40210ea525394dd8ad61e0`  
		Last Modified: Fri, 24 Apr 2020 09:33:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c48bfd2f77655c0149fe4b404b5c68c3b332da4e6bf5e7e18fc442d061aa648`  
		Last Modified: Fri, 24 Apr 2020 09:33:54 GMT  
		Size: 23.9 MB (23889917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e353948d2d0a669f162f5200b68f9edeb7678e46be6923d2f43ef135227deb`  
		Last Modified: Fri, 24 Apr 2020 09:33:33 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
