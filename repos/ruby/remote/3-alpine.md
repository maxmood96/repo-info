## `ruby:3-alpine`

```console
$ docker pull ruby@sha256:4ee802083cd5ae9ee2d287460814c9c5397617c60e3e603eb840722458f33ddb
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

### `ruby:3-alpine` - linux; amd64

```console
$ docker pull ruby@sha256:911e18cd14b0a90cfe361627c72776e00b183e09baa4e843bb07951badb743c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39351870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49414a6e04139eb3cff309c1e21c7342dc16adb8f0785c4131c52309cf314b13`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 03:56:24 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 15 Jun 2023 03:56:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Jun 2023 03:56:25 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jun 2023 04:02:33 GMT
ENV RUBY_MAJOR=3.2
# Thu, 15 Jun 2023 04:02:33 GMT
ENV RUBY_VERSION=3.2.2
# Thu, 15 Jun 2023 04:02:34 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Thu, 15 Jun 2023 04:05:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 15 Jun 2023 04:05:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 15 Jun 2023 04:05:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 15 Jun 2023 04:05:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 04:05:16 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 15 Jun 2023 04:05:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05eb7308df9f7638a609c3e45583778fff62729a8b3e25c81f4feee7457d921`  
		Last Modified: Thu, 15 Jun 2023 04:16:39 GMT  
		Size: 4.1 MB (4129278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5165e58f1b8e67d96732a0e073778069794b1af20e23c36587e528b6ddb939d7`  
		Last Modified: Thu, 15 Jun 2023 04:16:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507c3e05814f202f3026d78ffd3af9d9723c65245be1e3c73f3468710ee88e91`  
		Last Modified: Thu, 15 Jun 2023 04:17:15 GMT  
		Size: 31.8 MB (31824316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083943f3c4eb614da30dadcc1683292a258e958523ce7d6cb7420062e4f7b8fd`  
		Last Modified: Thu, 15 Jun 2023 04:17:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine` - linux; arm variant v6

```console
$ docker pull ruby@sha256:a87596ec7398b424c158231239a455bb2ab4452458036cb03cb1341193fea9c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35055887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd21c264d0447f9d77b7b8f4c72cf5fc629601894630f876a3207dbd34074277`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 06:22:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 15 Jun 2023 06:22:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Jun 2023 06:22:15 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jun 2023 06:27:14 GMT
ENV RUBY_MAJOR=3.2
# Thu, 15 Jun 2023 06:27:14 GMT
ENV RUBY_VERSION=3.2.2
# Thu, 15 Jun 2023 06:27:14 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Thu, 15 Jun 2023 06:29:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 15 Jun 2023 06:29:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 15 Jun 2023 06:29:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 15 Jun 2023 06:29:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 06:29:39 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 15 Jun 2023 06:29:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbb41f6d53774ead70775e4898e7d641569ec35d648f303665bf4c67da428f6`  
		Last Modified: Thu, 15 Jun 2023 06:40:10 GMT  
		Size: 3.8 MB (3805898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34701827a131c444dbff21ffb954e85d6b723c516bf03394085825eacce603e3`  
		Last Modified: Thu, 15 Jun 2023 06:40:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292416920a6087d26741e7772c2b4e5d1afdcd68911b994af04dbf7fd3fa0e90`  
		Last Modified: Thu, 15 Jun 2023 06:40:42 GMT  
		Size: 28.1 MB (28106238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551b8c96596182e5998b83ea55d1548c2a4483f0a53e00056b0fa638adfa42ad`  
		Last Modified: Thu, 15 Jun 2023 06:40:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine` - linux; arm variant v7

```console
$ docker pull ruby@sha256:0c0bd348e52a0afc8d90a7aa1f43bb78cedffcf4f207c58559d5194bcfdb81a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34580449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63921c1108c54ec29c51ab6e0bf69534b3e2f5dd161a78b71ad616be700998f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 21:21:02 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Tue, 08 Aug 2023 21:21:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 08 Aug 2023 21:21:03 GMT
ENV LANG=C.UTF-8
# Tue, 08 Aug 2023 21:28:10 GMT
ENV RUBY_MAJOR=3.2
# Tue, 08 Aug 2023 21:28:10 GMT
ENV RUBY_VERSION=3.2.2
# Tue, 08 Aug 2023 21:28:10 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Tue, 08 Aug 2023 21:31:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 08 Aug 2023 21:31:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 08 Aug 2023 21:31:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 08 Aug 2023 21:31:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 21:31:26 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Tue, 08 Aug 2023 21:31:26 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe3832d12f95d1aa87f713df90a7b1be9e0007b4d032c7a0d2fcab335d5b5dd`  
		Last Modified: Tue, 08 Aug 2023 21:48:25 GMT  
		Size: 3.7 MB (3716124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0949fe4764725130832196beb9a6e6ab2885d054df2460504e5cabba293cc140`  
		Last Modified: Tue, 08 Aug 2023 21:48:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe2a07434b28c1eeddb5e8b8747d222f6e0d9b1039b8600f0b077e711fe1e12`  
		Last Modified: Tue, 08 Aug 2023 21:49:09 GMT  
		Size: 28.0 MB (27964449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8b4e3f3f5673df33ecf9165b591753bf4110032a9336021da19a77f76f6fcb`  
		Last Modified: Tue, 08 Aug 2023 21:49:05 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:e3e89d025839cf658a63ea1240e4be35150402800a872d8cb233372b28c8bfba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39187692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28ac1562e0b00fbb96a1e7638a950111e936dd2a7a8cc4cc81be7f7091d745`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:11:55 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 15 Jun 2023 05:11:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Jun 2023 05:11:55 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jun 2023 05:16:14 GMT
ENV RUBY_MAJOR=3.2
# Thu, 15 Jun 2023 05:16:14 GMT
ENV RUBY_VERSION=3.2.2
# Thu, 15 Jun 2023 05:16:14 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Thu, 15 Jun 2023 05:18:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 15 Jun 2023 05:18:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 15 Jun 2023 05:18:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 15 Jun 2023 05:18:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:18:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 15 Jun 2023 05:18:08 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5649d186f416eccc10dbcbc57e68cb47de09565ee69266a4455bbd40a01a543`  
		Last Modified: Thu, 15 Jun 2023 05:26:52 GMT  
		Size: 4.1 MB (4059788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b850834ea1df3d55d4fbf94ce15afe629a2d457de24f0e8a34d647daff9a967c`  
		Last Modified: Thu, 15 Jun 2023 05:26:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ac1a07fd46f98c6be4b875efc723652ea6d0e219e1ecbbb8dee44c0e84383a`  
		Last Modified: Thu, 15 Jun 2023 05:27:30 GMT  
		Size: 31.8 MB (31798257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b609298bc3c94c14f6ca96ec6e85178cefe3985ae65ad4873a244af851d966fd`  
		Last Modified: Thu, 15 Jun 2023 05:27:27 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine` - linux; 386

```console
$ docker pull ruby@sha256:27ccbe8d10d3e3a3408724dab70a55cf52cba2e7902b90590acabfa4e8182cea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.3 MB (35256219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345a4383037394d838c95591ebc2de96aff9f729ff540d4c29de1ec8a39141ab`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:22 GMT
ADD file:94bec00e2c0c7f47c81ec4355a29ca23a81b439797d037b1a5a455f36a25dab4 in / 
# Wed, 14 Jun 2023 22:33:22 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:48:24 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 15 Jun 2023 05:48:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Jun 2023 05:48:25 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jun 2023 05:56:13 GMT
ENV RUBY_MAJOR=3.2
# Thu, 15 Jun 2023 05:56:13 GMT
ENV RUBY_VERSION=3.2.2
# Thu, 15 Jun 2023 05:56:13 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Thu, 15 Jun 2023 05:59:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 15 Jun 2023 05:59:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 15 Jun 2023 05:59:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 15 Jun 2023 05:59:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:59:52 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 15 Jun 2023 05:59:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b3f50075abd13aad1cb7d8c1427aa59d7fcac88f3690d3f9c3efdbec80fd0856`  
		Last Modified: Wed, 14 Jun 2023 22:33:48 GMT  
		Size: 3.2 MB (3233951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3e2b59e36a718da8d254bef52b5f02e04e9cd5600d9347a5bc384f1ecda7d9a`  
		Last Modified: Thu, 15 Jun 2023 06:17:10 GMT  
		Size: 4.1 MB (4135668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0affad649d3cfa7c3a16258c50c4a720f72ae7fdd173533e81cad26912ec4c3d`  
		Last Modified: Thu, 15 Jun 2023 06:17:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aadd84bb52d441f3607abe69427f628689b91ef013614309f9368061b003a7f`  
		Last Modified: Thu, 15 Jun 2023 06:17:49 GMT  
		Size: 27.9 MB (27886204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0c70c4ef3e1c4ac9a475f2c74af6439d9fc84c5c9ab404223336ddfdf2dc83`  
		Last Modified: Thu, 15 Jun 2023 06:17:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine` - linux; ppc64le

```console
$ docker pull ruby@sha256:40cbceec637ef04b4bbb112d95afb1d5c79b3507ffae417e3a8a36d21c021214
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36890242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1ab61367aa92cf1160f9288cf10692201a65f5cfe483b1fb79efb11bcf1cbf`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:49 GMT
ADD file:694c636c0dd19fd01accbc189e4c1dc4d063952692c6e7eb26dce02a7adba833 in / 
# Thu, 15 Jun 2023 00:39:49 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 11:10:33 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 15 Jun 2023 11:10:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Jun 2023 11:10:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jun 2023 11:18:30 GMT
ENV RUBY_MAJOR=3.2
# Thu, 15 Jun 2023 11:18:31 GMT
ENV RUBY_VERSION=3.2.2
# Thu, 15 Jun 2023 11:18:31 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Thu, 15 Jun 2023 11:21:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 15 Jun 2023 11:21:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 15 Jun 2023 11:21:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 15 Jun 2023 11:21:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 11:21:57 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 15 Jun 2023 11:21:57 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ffa4a466dbb8eebd7e7f25590a9df12390de9016abf82279c29c9a64aa76491a`  
		Last Modified: Thu, 15 Jun 2023 00:40:26 GMT  
		Size: 3.3 MB (3344781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594d1c10713a9371a17e6dbb6d0a4ec3187565c969358c2ef668a3c8da5706a5`  
		Last Modified: Thu, 15 Jun 2023 11:38:23 GMT  
		Size: 4.3 MB (4278208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b475e6db42c59e56d8308e0804afa3160331b29c960e048caaf3c8901f0a12`  
		Last Modified: Thu, 15 Jun 2023 11:38:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52b9300614888cde457b66cf461400a85edb400c7890a95dac26f88edfeedd4`  
		Last Modified: Thu, 15 Jun 2023 11:39:05 GMT  
		Size: 29.3 MB (29266856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eac5057d2569d30e9198a7ed9533865933bf7e78e7f137405dd7b234e1f38d7`  
		Last Modified: Thu, 15 Jun 2023 11:38:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine` - linux; s390x

```console
$ docker pull ruby@sha256:380ff417e0cddb337efc086686ba6204590532de35c93fe231c39a70c6ab690e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36141473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745f635ac2dea5e1d880de54d190a953330854ec406ed8f3c7a41cc7640f29f1`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 15:41:55 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Thu, 15 Jun 2023 15:41:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Jun 2023 15:41:56 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jun 2023 16:03:28 GMT
ENV RUBY_MAJOR=3.2
# Thu, 15 Jun 2023 16:03:28 GMT
ENV RUBY_VERSION=3.2.2
# Thu, 15 Jun 2023 16:03:29 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Thu, 15 Jun 2023 16:05:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Thu, 15 Jun 2023 16:05:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 15 Jun 2023 16:05:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 15 Jun 2023 16:05:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 16:05:53 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Thu, 15 Jun 2023 16:05:53 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4188228dbd7e545d3595c0a7e42f1637ee6dcc9ded923039211c8dedd8b8496`  
		Last Modified: Thu, 15 Jun 2023 17:11:15 GMT  
		Size: 4.2 MB (4234778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c29a5e09df75dfda37923024f8a763e3ece37b61d199c3fd0214deb7c25e1f`  
		Last Modified: Thu, 15 Jun 2023 17:11:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4bc4281cb42155413ef45c3f642140ee9a7232a3ceab4c9d675bfb0d4d930cb`  
		Last Modified: Thu, 15 Jun 2023 17:18:40 GMT  
		Size: 28.7 MB (28692802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c04bcec8de9a267fa571d736c858671c203e0df2fa4d64bd36f390d0dda355a`  
		Last Modified: Thu, 15 Jun 2023 17:18:37 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
