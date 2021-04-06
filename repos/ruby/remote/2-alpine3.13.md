## `ruby:2-alpine3.13`

```console
$ docker pull ruby@sha256:9b06894c1791a5a5c8b1b3eed6c3db0a9129b522c97583fc4a8eb8d835d3f083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `ruby:2-alpine3.13` - linux; amd64

```console
$ docker pull ruby@sha256:0e236ac55ed154188f3b30e9b261e5a923d0c608f1c8ce5dfb115173bfe7f8ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27238763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2742d0de4c8e1105d13679282cab84c139375671cd5e5c6d2d119b95edf55d0e`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Mar 2021 20:10:06 GMT
ADD file:7119167b56ff1228b2fb639c768955ce9db7a999cd947179240b216dfa5ccbb9 in / 
# Wed, 31 Mar 2021 20:10:06 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 10:39:43 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 01 Apr 2021 10:39:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 01 Apr 2021 10:39:45 GMT
ENV LANG=C.UTF-8
# Thu, 01 Apr 2021 10:47:42 GMT
ENV RUBY_MAJOR=2.7
# Mon, 05 Apr 2021 19:16:34 GMT
ENV RUBY_VERSION=2.7.3
# Mon, 05 Apr 2021 19:16:34 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Mon, 05 Apr 2021 19:20:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 05 Apr 2021 19:20:59 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 05 Apr 2021 19:20:59 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 05 Apr 2021 19:20:59 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Apr 2021 19:21:02 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 05 Apr 2021 19:21:02 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ca3cd42a7c9525f6ce3d64c1a70982613a8235f0cc057ec9244052921853ef15`  
		Last Modified: Wed, 31 Mar 2021 20:10:46 GMT  
		Size: 2.8 MB (2811947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9df2de4dab84e51acacca9e65a3d9f7c9fa2f038bc11c2830bd9a97980823a0`  
		Last Modified: Thu, 01 Apr 2021 11:09:32 GMT  
		Size: 1.2 MB (1218696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc339b259bb6448a756fb9b42044f3450a7dcd6fc3bc0102a3cb6b7594daca19`  
		Last Modified: Thu, 01 Apr 2021 11:09:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67bf4c0832c8a73d79344879220b7a99ed4ecccf6eb758384bec64d8719c63b8`  
		Last Modified: Mon, 05 Apr 2021 20:15:04 GMT  
		Size: 23.2 MB (23207724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e0141082ecc3e69444f52c2c25989a96c26e3f1db52ed818a2415be78f134a`  
		Last Modified: Mon, 05 Apr 2021 20:15:02 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.13` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:4912b17f703b9de40c580d6002fd5b3bfa86b269372a5cbd57eb4173d8cfe884
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26959267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb0f419e663fa975ed761e8df1b5d3ed2fcbb5430c3714b11e5ad3cbb88177a1`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 11:22:47 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 01 Apr 2021 11:22:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 01 Apr 2021 11:22:51 GMT
ENV LANG=C.UTF-8
# Thu, 01 Apr 2021 11:30:03 GMT
ENV RUBY_MAJOR=2.7
# Mon, 05 Apr 2021 21:55:38 GMT
ENV RUBY_VERSION=2.7.3
# Mon, 05 Apr 2021 21:55:39 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Mon, 05 Apr 2021 21:58:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 05 Apr 2021 21:58:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 05 Apr 2021 21:58:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 05 Apr 2021 21:58:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Apr 2021 21:59:01 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 05 Apr 2021 21:59:02 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ad87e22eb6e6823616c9c7d49b75e77927a94fb70ad219aad372b48d4e912a`  
		Last Modified: Thu, 01 Apr 2021 11:53:53 GMT  
		Size: 1.2 MB (1221079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36680847d0d64157ef36dc0019fd9024c2685cf93ecb0d81eacd38dd66765340`  
		Last Modified: Thu, 01 Apr 2021 11:53:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4edf46ce9fd1b74a276e0570bde058b6c3e528ba423e0e3a69bf3c866cae0e70`  
		Last Modified: Mon, 05 Apr 2021 22:46:50 GMT  
		Size: 23.0 MB (23025872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5de04617aeb680dfeeeb50e00df67fef621792030e0b09e67d104dd8b6360b1`  
		Last Modified: Mon, 05 Apr 2021 22:46:41 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.13` - linux; 386

```console
$ docker pull ruby@sha256:156b878b2a45db6bfab387ca885b588a8609f34324792a22da2fd0a66e204336
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26513541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e28a0bd87f4020b5d2505c02b05158359980232c4c125e920380adf21c04842`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:00 GMT
ADD file:245767f958e2b5e6fad41d45d3361849e7c6b2255303e3c785f0f2c86019553a in / 
# Wed, 31 Mar 2021 17:43:00 GMT
CMD ["/bin/sh"]
# Wed, 31 Mar 2021 23:55:30 GMT
RUN apk add --no-cache 		gmp-dev
# Wed, 31 Mar 2021 23:55:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 31 Mar 2021 23:55:32 GMT
ENV LANG=C.UTF-8
# Thu, 01 Apr 2021 00:05:12 GMT
ENV RUBY_MAJOR=2.7
# Mon, 05 Apr 2021 19:04:14 GMT
ENV RUBY_VERSION=2.7.3
# Mon, 05 Apr 2021 19:04:15 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Mon, 05 Apr 2021 19:09:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 05 Apr 2021 19:09:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 05 Apr 2021 19:09:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 05 Apr 2021 19:09:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Apr 2021 19:09:50 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 05 Apr 2021 19:09:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b22e590ebf70a9a5901c380b07232ef3c07cb13440402934dfdffb8f8721a949`  
		Last Modified: Wed, 31 Mar 2021 17:44:05 GMT  
		Size: 2.8 MB (2818802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3f50d953b6447de874c74f6f24c01f9db5f651cbc744d6bea0fc813e020a95`  
		Last Modified: Thu, 01 Apr 2021 00:35:20 GMT  
		Size: 1.3 MB (1257444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4caf3f7461bbef426586b45a0f318a08668425242d5e555a8108c49396c83c5`  
		Last Modified: Thu, 01 Apr 2021 00:35:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b894e3a81cfd40602ad8d09d5af0be4e4fec54b3ae945d3671f0af5cac162b4`  
		Last Modified: Mon, 05 Apr 2021 20:13:40 GMT  
		Size: 22.4 MB (22436900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d958713533522b082b2c6786b0ab25cf2c5f6ef3346f51aefa03a8574db46c89`  
		Last Modified: Mon, 05 Apr 2021 20:13:36 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:2-alpine3.13` - linux; ppc64le

```console
$ docker pull ruby@sha256:fe3509e251ac79553b0753c4e904f4306564f8d6844c47f8970b454e1ad63bca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27846359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec59755383d482ca817d09e67ee868dd80b9e0aa4ba27c4875f8527fe6aa1166`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Mar 2021 18:55:41 GMT
ADD file:1dd3315eb685a1b6729efb6f5b634e414f3da0f065078952bc6c0339dc09512d in / 
# Wed, 31 Mar 2021 18:55:49 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 18:21:24 GMT
RUN apk add --no-cache 		gmp-dev
# Thu, 01 Apr 2021 18:21:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 01 Apr 2021 18:21:44 GMT
ENV LANG=C.UTF-8
# Thu, 01 Apr 2021 18:31:38 GMT
ENV RUBY_MAJOR=2.7
# Mon, 05 Apr 2021 19:23:09 GMT
ENV RUBY_VERSION=2.7.3
# Mon, 05 Apr 2021 19:23:16 GMT
ENV RUBY_DOWNLOAD_SHA256=5e91d1650857d43cd6852e05ac54683351e9c301811ee0bef43a67c4605e7db1
# Mon, 05 Apr 2021 19:26:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	; 	make -j "$(nproc)"; 	make install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps 		$runDeps 		bzip2 		ca-certificates 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	! apk --no-network list --installed 		| grep -v '^[.]ruby-rundeps' 		| grep -i ruby 	; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Mon, 05 Apr 2021 19:26:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 05 Apr 2021 19:26:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 05 Apr 2021 19:26:40 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 Apr 2021 19:26:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 777 "$GEM_HOME"
# Mon, 05 Apr 2021 19:26:55 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:dc4792b25345295bf964e1db1bceedb2338bfad8f0fb64f0cc07b152df9aef84`  
		Last Modified: Wed, 31 Mar 2021 18:57:19 GMT  
		Size: 2.8 MB (2813219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2844bec71be93b6a990c709d31b39d16a54da1edeb0058f3c10de9975c01bc40`  
		Last Modified: Thu, 01 Apr 2021 19:01:50 GMT  
		Size: 1.3 MB (1302664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db92fb641ba2e00ba2604ba6191f4af3cd2b087445ea604400878d3b08d41689`  
		Last Modified: Thu, 01 Apr 2021 19:01:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c316a37c692ea3b7bcba2419bf75baae4d0ed799b4c26b243ef69c4ca61434d3`  
		Last Modified: Mon, 05 Apr 2021 20:30:05 GMT  
		Size: 23.7 MB (23730080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459ac66558778512bc90389f64e72243fc3a7b1c180e051e21dd9f9dee9b9de1`  
		Last Modified: Mon, 05 Apr 2021 20:30:01 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
