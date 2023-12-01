## `ruby:3-alpine3.17`

```console
$ docker pull ruby@sha256:ab02a738d52d0077fe0d00fc7e9e7c014616bd175f163e7b15c4451b904ee04b
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

### `ruby:3-alpine3.17` - linux; amd64

```console
$ docker pull ruby@sha256:5e11b2787dfc1891744171ba0112435d2fcd2d4b13019e57d0696b1bf360bea0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39322970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc069cfc4113d49e432d6e44330a87cb385377354961c12ba4db51058dafc542`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:40:10 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 01 Dec 2023 05:40:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 01 Dec 2023 05:40:10 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 05:46:20 GMT
ENV RUBY_MAJOR=3.2
# Fri, 01 Dec 2023 05:46:20 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 01 Dec 2023 05:46:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 01 Dec 2023 05:49:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 01 Dec 2023 05:49:07 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 01 Dec 2023 05:49:07 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 01 Dec 2023 05:49:07 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 05:49:08 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 01 Dec 2023 05:49:08 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483120b6e93a3f0c99a3333bebde74a4236a5b2346de09fde22b7f9c8328a74e`  
		Last Modified: Fri, 01 Dec 2023 05:57:40 GMT  
		Size: 4.1 MB (4126455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8014301d882d8224ffe51e7659dd0acf2e5e95eea7304cebbb9c37ab2b3ad9`  
		Last Modified: Fri, 01 Dec 2023 05:57:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401feed4d188acdc73d3cb7d2807e5ed9960b1670e441a43271c3b099f498280`  
		Last Modified: Fri, 01 Dec 2023 05:58:22 GMT  
		Size: 31.8 MB (31816796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d08c21e8ff8bf48d4cfd40daa0fa6a4ad0bf039df1f6d812e382dfc2a8f8798d`  
		Last Modified: Fri, 01 Dec 2023 05:58:19 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.17` - linux; arm variant v6

```console
$ docker pull ruby@sha256:b892d220ddba13d6cf809956b794b77b5fe52cc7f4e14dc2d30087c27d015118
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35099825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5806171b8371cbc21ee3f42bbaea4c5a6729602098e5fd030efcf7428adf46e3`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:21 GMT
ADD file:90d3bdc6a557ead63796de0110e2fda87e65aa091070cbae612dfb2126568253 in / 
# Thu, 30 Nov 2023 22:49:21 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 11:20:39 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 01 Dec 2023 11:20:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 01 Dec 2023 11:20:39 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 11:25:22 GMT
ENV RUBY_MAJOR=3.2
# Fri, 01 Dec 2023 11:25:22 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 01 Dec 2023 11:25:22 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 01 Dec 2023 11:27:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 01 Dec 2023 11:27:40 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 01 Dec 2023 11:27:40 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 01 Dec 2023 11:27:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 11:27:41 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 01 Dec 2023 11:27:41 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f0440ff44d712e5fc701b84856116589b428157893ac461b633b1ab30b627eed`  
		Last Modified: Thu, 30 Nov 2023 22:49:52 GMT  
		Size: 3.1 MB (3113003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ae7b613b795d30a42a20b989853f2c7903f697d2b37f812cfc63149f4204f5`  
		Last Modified: Fri, 01 Dec 2023 11:36:11 GMT  
		Size: 3.9 MB (3868221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb175dbc2e3ed7e4e665d94d00a99924f12e8b11fc1b3040f37f374424255f8`  
		Last Modified: Fri, 01 Dec 2023 11:36:10 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e7c7a153ac9d1b43882e1af23bbaebff0d6a23b0c03ab6eba47b0bdd218bd7`  
		Last Modified: Fri, 01 Dec 2023 11:36:47 GMT  
		Size: 28.1 MB (28118204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3338189aad3963eea54f97ecb70f7344d3bed984d014ce687bcb1c88ba3a427e`  
		Last Modified: Fri, 01 Dec 2023 11:36:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.17` - linux; arm variant v7

```console
$ docker pull ruby@sha256:05d621c87473563cab784596870e1c20aea4db2be9ac1ca7b04b604f9b2841b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.6 MB (34590125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aed04dcd460e50705a74fb1357ccfe9b73e9312272cb3eb463f75da59ad6d7e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:34 GMT
ADD file:02a6ccbee2a71a547141a8480f3a3912c7bb0934df31124f4a4720204d326698 in / 
# Thu, 30 Nov 2023 22:49:34 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:53:53 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 01 Dec 2023 08:53:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 01 Dec 2023 08:53:54 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 08:57:57 GMT
ENV RUBY_MAJOR=3.2
# Fri, 01 Dec 2023 08:57:57 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 01 Dec 2023 08:57:57 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 01 Dec 2023 08:59:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 01 Dec 2023 08:59:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 01 Dec 2023 08:59:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 01 Dec 2023 08:59:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 08:59:48 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 01 Dec 2023 08:59:48 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d4ee79c42f17f258e1c67dc32e0776c934799d208cd0a9b6264f65d60f1a26fc`  
		Last Modified: Thu, 30 Nov 2023 22:50:08 GMT  
		Size: 2.9 MB (2869713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4881a453d9a61b1e49a4875c23314a563d5fc4c1d54ba8ba1047e9ab877e6fd6`  
		Last Modified: Fri, 01 Dec 2023 09:06:50 GMT  
		Size: 3.7 MB (3722749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f0eeff2cae5f755ac0df64db5d8d418cfae777a80897bcfa6ae1485c6b65a1`  
		Last Modified: Fri, 01 Dec 2023 09:06:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87f1f4eba5ddb345df23814a36cac3cf57d5bb83b07a45a534e162e6852ea42`  
		Last Modified: Fri, 01 Dec 2023 09:07:37 GMT  
		Size: 28.0 MB (27997267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a670b352605a25414d707a6a8d04c3a1deffb4d51569f38fa5baa1573e4f89b`  
		Last Modified: Fri, 01 Dec 2023 09:07:33 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:5561175f76dab30841a40ff7e6d5c0728a6fcc62eb34c369bda490d3b15fd918
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39154804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036f9298818617063af63243c894a935e274e8d616fdefb1bfce9c1d10d12186`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:07 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Thu, 30 Nov 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:13:47 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 01 Dec 2023 09:13:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 01 Dec 2023 09:13:48 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 09:18:22 GMT
ENV RUBY_MAJOR=3.2
# Fri, 01 Dec 2023 09:18:22 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 01 Dec 2023 09:18:22 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 01 Dec 2023 09:20:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 01 Dec 2023 09:20:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 01 Dec 2023 09:20:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 01 Dec 2023 09:20:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 09:20:20 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 01 Dec 2023 09:20:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a49788f7aec5cc3d6215bd0a746b96d2f2c0222d8191faf6085aad6655605b`  
		Last Modified: Fri, 01 Dec 2023 09:27:00 GMT  
		Size: 4.1 MB (4118334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685aa69fdc183ac290d3160ba466558ae85c73c1fde0722f2a20ed55ed451ebc`  
		Last Modified: Fri, 01 Dec 2023 09:27:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c42f98fa8f11ee19189f280024da12e39409aa6aec3fc7d9627c454ef0ad700`  
		Last Modified: Fri, 01 Dec 2023 09:27:39 GMT  
		Size: 31.8 MB (31777725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff2022da0de1d0d722df9dcaf2545dcd5295956d964e6ce9dbf5b90ec4e4c21`  
		Last Modified: Fri, 01 Dec 2023 09:27:37 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.17` - linux; 386

```console
$ docker pull ruby@sha256:feb3bc1835245651c2f1e2042620943770a353ec4afb71032c70690a7b61e742
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35497896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926674e36dffb13ee568e1bb886789c5034919ce120d7f1af29b45c3dd584fe7`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 01 Dec 2023 02:03:50 GMT
ADD file:4ad1e09b0030ebbf09adcc7c616502a079dc61aff7c6edce2f2ea248cd85b2df in / 
# Fri, 01 Dec 2023 02:03:50 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:22:42 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 01 Dec 2023 09:22:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 01 Dec 2023 09:22:43 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 09:31:32 GMT
ENV RUBY_MAJOR=3.2
# Fri, 01 Dec 2023 09:31:32 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 01 Dec 2023 09:31:32 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 01 Dec 2023 09:35:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 01 Dec 2023 09:35:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 01 Dec 2023 09:35:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 01 Dec 2023 09:35:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 09:35:31 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 01 Dec 2023 09:35:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7583c43471b6e056e4cc98119de7f0921ba6ad8cd2645554165c3d9869b344dc`  
		Last Modified: Fri, 01 Dec 2023 02:04:31 GMT  
		Size: 3.4 MB (3414867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80870829e7e8f30bf6ca167052dd2c64cbe64eda8b0830f3dea1d3d589b4866a`  
		Last Modified: Fri, 01 Dec 2023 09:49:59 GMT  
		Size: 4.2 MB (4196085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649adbd529d54b5228e6f62a4d0b0f4faeeaab8a81dd13dd876f81628da4f6d3`  
		Last Modified: Fri, 01 Dec 2023 09:49:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2286744a9bc015357a677bccf2a65889f5920885ea75e98bac8ccf3608329df7`  
		Last Modified: Fri, 01 Dec 2023 09:50:43 GMT  
		Size: 27.9 MB (27886546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a26fb5e602096face63228cf4678c4f156b4595757adbafd53b7950a98c6cb4`  
		Last Modified: Fri, 01 Dec 2023 09:50:40 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.17` - linux; ppc64le

```console
$ docker pull ruby@sha256:750cc2f629ea50c39ef9d55270321dd917fb3291740629801f88e177bf06e30f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36932060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f58bae9d6c4fc4b3e14edd5eea82bf9bda17c905b7df0496388abf8622b0e6e`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 30 Nov 2023 23:19:15 GMT
ADD file:e3eb0ea4f652282ad08228d0d146f33998b9e93641756d780ac0205aa828c070 in / 
# Thu, 30 Nov 2023 23:19:17 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 09:25:55 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 01 Dec 2023 09:26:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 01 Dec 2023 09:26:10 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 09:33:01 GMT
ENV RUBY_MAJOR=3.2
# Fri, 01 Dec 2023 09:33:02 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 01 Dec 2023 09:33:03 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 01 Dec 2023 09:35:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 01 Dec 2023 09:35:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 01 Dec 2023 09:35:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 01 Dec 2023 09:35:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 09:35:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 01 Dec 2023 09:35:34 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c7d387f1f267ea360529df8d70b246f949e1afdb2317cdf84b028cda80a093d1`  
		Last Modified: Thu, 30 Nov 2023 23:20:17 GMT  
		Size: 3.4 MB (3391875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610892369dc855307a731bf9e79037d41e616a816ea0b388658e1233d771502f`  
		Last Modified: Fri, 01 Dec 2023 09:45:19 GMT  
		Size: 4.3 MB (4281983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fad899ebab804ea2a98c521b154fd3d26a9b41b1f8bfc13722a7742127a4875`  
		Last Modified: Fri, 01 Dec 2023 09:45:18 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093a007e0109e1b0cef402048caf863eb68a86ec75ea4e9aff9a9f69339aa6bd`  
		Last Modified: Fri, 01 Dec 2023 09:46:04 GMT  
		Size: 29.3 MB (29257807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3b66813bece62f6d4b2ef7ded7f9381a67806136fc4017626b1ab8bf9249fa`  
		Last Modified: Fri, 01 Dec 2023 09:46:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:3-alpine3.17` - linux; s390x

```console
$ docker pull ruby@sha256:950ae2c3e0ad3ce54c713f8ec62a20df51b0cdc71979d9d4da191eb6eed7d7dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36060370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a05d5ee63401a20ccdc9f94f8adbf60d2170f56077dc18722d5089fd9251cb6`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:16 GMT
ADD file:bf416048d22b9a0deecb508385355d79b8d5d12b655c600dbdc0948f7dcbb2c2 in / 
# Thu, 30 Nov 2023 22:42:17 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 08:27:45 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	;
# Fri, 01 Dec 2023 08:27:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 01 Dec 2023 08:27:46 GMT
ENV LANG=C.UTF-8
# Fri, 01 Dec 2023 08:33:38 GMT
ENV RUBY_MAJOR=3.2
# Fri, 01 Dec 2023 08:33:39 GMT
ENV RUBY_VERSION=3.2.2
# Fri, 01 Dec 2023 08:33:39 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Fri, 01 Dec 2023 08:36:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bison 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		readline-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='95427cb0592e32ed39c8bd522fe2a40a746ba07afb8149f91e936cddb4d6eeac' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7855404cdc50c20040c743800c947b6f452490d47f8590a4a83bc6f75d1d8eda' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Fri, 01 Dec 2023 08:36:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 01 Dec 2023 08:36:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 01 Dec 2023 08:36:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 08:36:11 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Fri, 01 Dec 2023 08:36:11 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7e9e7e53b618240d2e82e8cab6b677eab6786c4210dcc2b1a35bfd4cb492757e`  
		Last Modified: Thu, 30 Nov 2023 22:43:01 GMT  
		Size: 3.2 MB (3176332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02b03da3e183aae8e8f120bac6bf2f9fe8606a8248f0567e3dea15cefd8aaa5`  
		Last Modified: Fri, 01 Dec 2023 08:46:39 GMT  
		Size: 4.2 MB (4199166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb52eb5db795ca059885989e0cebd0bbdcbf608b0a84d5f24903337486108e2`  
		Last Modified: Fri, 01 Dec 2023 08:46:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecb05a098dc5958a0310c2f601b77940d7f29ad9b5cc2b599fe29504bb65a1d`  
		Last Modified: Fri, 01 Dec 2023 08:47:14 GMT  
		Size: 28.7 MB (28684473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c28044d9a4e12fa653a6a20c540afe99f7d20c5fa1fff837e96ee4d6e242159`  
		Last Modified: Fri, 01 Dec 2023 08:47:11 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
