## `ruby:alpine`

```console
$ docker pull ruby@sha256:52f0dfe54ac1038133001d062beeda65b3d269a3134fcd6381c00e1f58c6ea77
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

### `ruby:alpine` - linux; amd64

```console
$ docker pull ruby@sha256:5473962d98ac86e6037b1060c53bc15ca4dd40d14c7925d792596390f90e0609
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49367939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79017689050c6c298eb3a212f1ed0d8bddcdaa2dbe751d2b82bfcfdefd38989`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.1-x86_64.tar.gz / # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["/bin/sh"]
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV LANG=C.UTF-8
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_VERSION=3.4.1
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.1.tar.xz
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=018d59ffb52be3c0a6d847e22d3fd7a2c52d0ddfee249d3517a0c8c6dbfa70af
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:245043d9199c263f869fc0558f43f7cb98bbc92acdd5def1b4f690adc0ac7807`  
		Last Modified: Mon, 06 Jan 2025 21:44:42 GMT  
		Size: 3.6 MB (3636222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b57bf7abf98a02b7dc2918907b5f7219b8f39da2adbb2fcf2b9147104a76aa`  
		Last Modified: Tue, 07 Jan 2025 03:21:17 GMT  
		Size: 6.7 MB (6720942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81c7d7567bc56bd182e08de8d896cbef9bb9284f07ba4050bc1d9d9be8a70d`  
		Last Modified: Tue, 07 Jan 2025 03:21:17 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d99b7764ecab6238f14a9eca2051c14e4d555d775b83fba617f65b367b6b2ed`  
		Last Modified: Tue, 07 Jan 2025 03:21:17 GMT  
		Size: 39.0 MB (39010449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b9658275cbecee5df6f178e46f0b2068c7c5db9d44fd3ca2fa9b8217becc86`  
		Last Modified: Tue, 07 Jan 2025 03:21:17 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:f9680da24adad3dc611b2838aa2563e481b34895590dcc0719bfb2bde915d809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.7 KB (991748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51108fa74c49598f1ef248625bd3bad697a3c4b70c3399ac47403e8526100201`

```dockerfile
```

-	Layers:
	-	`sha256:6e8b0ac3f0fee8470142b9f1019e9de512795a896933d9e919a4c0344a6d2f0b`  
		Last Modified: Tue, 07 Jan 2025 03:21:17 GMT  
		Size: 965.5 KB (965494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4dab738f187a4a74219098fadde8ea9f9caeebcc1be221c31979b9a5d025583`  
		Last Modified: Tue, 07 Jan 2025 03:21:17 GMT  
		Size: 26.3 KB (26254 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; arm variant v6

```console
$ docker pull ruby@sha256:0ec2331cf1d6cec450c431ae929bded8a8811cf4da32367a47f3527f719010c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44384102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416a12f07a9c833c041fac9adb1d90a8c21c3345d7e66e9b0df1a1c68862dd59`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV LANG=C.UTF-8
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_VERSION=3.4.1
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.1.tar.xz
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=018d59ffb52be3c0a6d847e22d3fd7a2c52d0ddfee249d3517a0c8c6dbfa70af
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b12c95f1fe69503a4e99b4118a13b41c40d0844feba72e2e756a769be5fa7`  
		Last Modified: Fri, 06 Dec 2024 22:32:43 GMT  
		Size: 6.6 MB (6568172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ca0d2bb66a7dcb23798d7aa23885d8544420f7868a1046f3f039325e9bbe07`  
		Last Modified: Thu, 12 Dec 2024 22:38:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb067dc479a792146c69fe332a79fe1d8fbaf44bcc1c57ee5bfb9e35184fbc8`  
		Last Modified: Thu, 26 Dec 2024 16:30:39 GMT  
		Size: 34.4 MB (34448420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cad3f5fcf8afc763c8842355de640b3a44dd08c0e21d924313bf01050efeef`  
		Last Modified: Thu, 26 Dec 2024 16:30:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:cc5ed3babd1764522afd09839952bbd8b11104d0899ffb2f69b0e2fff3a73cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7c37564cb65fc772d098661110f0a41251af0820f4e6777e2d7ba4a4db1aa9`

```dockerfile
```

-	Layers:
	-	`sha256:e84f8b9d1ff8071a21a619515e2a288652a4942ece51e0af5fa6df4d5e6574a1`  
		Last Modified: Thu, 26 Dec 2024 16:30:37 GMT  
		Size: 26.2 KB (26186 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; arm variant v7

```console
$ docker pull ruby@sha256:5e856a5443f75ddb4137a94a8efe60aef57ced15a64b383b4e209cfd03c8f9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43821973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804445b05cf382e9ccab0bfccb3e44d0dac6b0bdce9410343b25ad17c02cd8f5`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV LANG=C.UTF-8
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_VERSION=3.4.1
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.1.tar.xz
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=018d59ffb52be3c0a6d847e22d3fd7a2c52d0ddfee249d3517a0c8c6dbfa70af
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b26c224a9a1e46e5dfbc9bf70fcad8ef517f0a3c0bcf4815427a79622b385a`  
		Last Modified: Fri, 06 Dec 2024 22:33:32 GMT  
		Size: 6.4 MB (6408987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a6cefa53cbec58b80f6c0754a11c80ccf91e1b3e090d1a5b9687f91648e830`  
		Last Modified: Thu, 12 Dec 2024 23:18:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef34df5034fac6e48078d20bc7808ea86b3bf9813c1190d1cd63acac2af9283`  
		Last Modified: Thu, 26 Dec 2024 16:45:02 GMT  
		Size: 34.3 MB (34312621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6c7d281fe4d3037597289f54ed65f886de118939eadd754ad9a4d8e41a6f9a`  
		Last Modified: Thu, 26 Dec 2024 16:45:00 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:e9715d7f3ee23e24baac7359740329dd226c9746010bd765c7fff6d8d5e703b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.8 KB (980832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2166a032f2f8e4e6710ba4221db156d807fee30939730408d854503927a99c`

```dockerfile
```

-	Layers:
	-	`sha256:de940c57521ab538076284bad3a6d41deef7d188a5d7fa3a9d85661c9e5fb992`  
		Last Modified: Thu, 26 Dec 2024 16:45:01 GMT  
		Size: 954.4 KB (954431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5983f1aafb70041d2bcf3e5bab86958b0c78308c233105d5484c050fc5f4f341`  
		Last Modified: Thu, 26 Dec 2024 16:45:00 GMT  
		Size: 26.4 KB (26401 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:90f661a4cc5ae3bf9d7d8e7b32f63ac33ab9eb981912e82ac4f099eab1363f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49764115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c0eb0bc4c8a91c34507646e5f5241eea6cc4f2203b11700a07086bae01a67a`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV LANG=C.UTF-8
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_VERSION=3.4.1
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.1.tar.xz
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=018d59ffb52be3c0a6d847e22d3fd7a2c52d0ddfee249d3517a0c8c6dbfa70af
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8768c1cb67d700107587f1a01b3b69ecc681b49e487dfc7a461ef242515c6c`  
		Last Modified: Thu, 12 Dec 2024 23:11:44 GMT  
		Size: 6.8 MB (6776469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:375ce81c945782093cda3e7e6c9689a6849c2ef2dfe5385ab4b09180f84f6445`  
		Last Modified: Thu, 12 Dec 2024 23:11:44 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b75a445ac4bb80c573d873f3e7ddd72842fbd431a061fc7509f0230891d4656`  
		Last Modified: Thu, 26 Dec 2024 16:41:32 GMT  
		Size: 39.0 MB (38994138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67159f8e68aee2cc7218e61aa61c6d766983c922b0ca348781beeb3c904e375`  
		Last Modified: Thu, 26 Dec 2024 16:41:31 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:b0ec4ef87736b7ce43efc0d38ee599967b8b0bc2f19393768ed6a830590a8506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **982.1 KB (982131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbaed3e15cf87ae7e795cb4b75c512ecba397e780ad90b4ffe307938ae9660b5`

```dockerfile
```

-	Layers:
	-	`sha256:f99395a8f46e364edb0fcc940333e8dd4394caaa1ac4c604eea0982b1e1dbf8a`  
		Last Modified: Thu, 26 Dec 2024 16:41:31 GMT  
		Size: 955.7 KB (955680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6bfb2c611a26f4ae0f08296e54dcca7a37a03b85b79c84e15c07c65f45a0acd`  
		Last Modified: Thu, 26 Dec 2024 16:41:31 GMT  
		Size: 26.5 KB (26451 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; 386

```console
$ docker pull ruby@sha256:486d0ad2a5085e5e1f085e5a4af3c02e2a12fa1b1c5d4a1fe3692ca72cc68764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44575248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501dff2fb22d11c74a4c6d8cde908d2aa2400c14b99d02445c19b276b6c6f163`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.1-x86.tar.gz / # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["/bin/sh"]
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV LANG=C.UTF-8
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_VERSION=3.4.1
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.1.tar.xz
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=018d59ffb52be3c0a6d847e22d3fd7a2c52d0ddfee249d3517a0c8c6dbfa70af
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1b51cef20fac755ea70acf005c7461407387b0deae88500e38a1982868469f7a`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3458271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780c226b1f7f868db24097626f3e4ecc5afb644519c95d9f882f7a8cb1cb5b0f`  
		Last Modified: Tue, 07 Jan 2025 03:33:26 GMT  
		Size: 6.8 MB (6793606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b66d2b2ad29afb61e94f5057bdf910c4c38fc750868548a077cd948a1168b5`  
		Last Modified: Tue, 07 Jan 2025 03:33:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d3d7d825025582664534ed8624909ff11feb01bdb2ff5404209a85e2b81f6d`  
		Last Modified: Tue, 07 Jan 2025 03:33:26 GMT  
		Size: 34.3 MB (34323048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59ebdfd206fd9e9805f296d9050b8f59c2dfe1d574601b967e43769f671379d`  
		Last Modified: Tue, 07 Jan 2025 03:33:26 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:e5a570c69f23915bdb672461253e667b3104316c8e028f8c43f9a88d2881a997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.6 KB (991645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b9e9cadb27850ecf7bc1e4b5412668a1d35dd038faeb0d1da6a9c52b27dc4c`

```dockerfile
```

-	Layers:
	-	`sha256:ec1f3dacfb3e75bdb221ed9f8e355cd819a47fc41e6f71747c5d54c9519128a6`  
		Last Modified: Tue, 07 Jan 2025 03:33:26 GMT  
		Size: 965.4 KB (965449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e32666d3ffa8e06c9c957064a21b6de42220d058ad1eea8a1666aef5513477d`  
		Last Modified: Tue, 07 Jan 2025 03:33:25 GMT  
		Size: 26.2 KB (26196 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; ppc64le

```console
$ docker pull ruby@sha256:6e3de000c15b841810d59815678790244888bc1d84fa54f899af20d2a4d0740f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46447924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85556b50ed969ee6e91f852326793528aa7cfc4ed36f3c9e193c149f0a8be5ed`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.1-ppc64le.tar.gz / # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["/bin/sh"]
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV LANG=C.UTF-8
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_VERSION=3.4.1
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.1.tar.xz
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=018d59ffb52be3c0a6d847e22d3fd7a2c52d0ddfee249d3517a0c8c6dbfa70af
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9207393f0daad55cddbc775f55edde5baecdca9e0441c9c1f627f2394d28b7c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:05 GMT  
		Size: 3.6 MB (3567745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3af903844bd49007e4d6ca2e69b48a913626c6053b559b491b23908a5d61af`  
		Last Modified: Tue, 07 Jan 2025 09:16:51 GMT  
		Size: 6.9 MB (6932635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8312e828a293adddcd2c5297f5680161c56f4e1e97fc3d39fd3ddbcd3776ff`  
		Last Modified: Tue, 07 Jan 2025 09:16:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db4c7e715fbfd5b2197eac09e5615ed8d7d1dd90d0e64d2d660ac17238604f1`  
		Last Modified: Tue, 07 Jan 2025 09:16:52 GMT  
		Size: 35.9 MB (35947220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8b9625f4590ea77e8113861732982ffcfc293df5da92da9ddde3cae07cfffd`  
		Last Modified: Tue, 07 Jan 2025 09:16:51 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:fd4606dfd943bf0bc6fca68c1b0951005ce9dfcfe571d9938041243a34959311
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.7 KB (980749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6388b32d2b83f4b09c9958d6966ac813f2fb24986da584498d33745f425766ee`

```dockerfile
```

-	Layers:
	-	`sha256:7dcc25185412855607bbafa299962fa745d02023a90aaa956f42bba0721539cc`  
		Last Modified: Tue, 07 Jan 2025 09:16:51 GMT  
		Size: 954.4 KB (954422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ce61588d9cf709f8c9fd9b78788db3143b4b095a0815b914c82b67b27dd1e69`  
		Last Modified: Tue, 07 Jan 2025 09:16:51 GMT  
		Size: 26.3 KB (26327 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; riscv64

```console
$ docker pull ruby@sha256:4b79e83140eafbcce7278dbd31ceea603ea88040835208ccb0ff36c960f4008d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44748741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f861327602d627c0042b81bdc1dd9df4bcad5b4493d350081e50d3dc405fad`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV LANG=C.UTF-8
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_VERSION=3.4.1
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.1.tar.xz
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=018d59ffb52be3c0a6d847e22d3fd7a2c52d0ddfee249d3517a0c8c6dbfa70af
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b7db57ce6582cad423aa019d67c20ca5f5e16ec97e975335764cc1996c665f`  
		Last Modified: Sat, 07 Dec 2024 00:25:25 GMT  
		Size: 7.0 MB (7000654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b63656a2dd88416c17c13243099944dfea98286c4cdac0fbbd1551c76ce582`  
		Last Modified: Fri, 13 Dec 2024 08:26:39 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869c38b16fcda72d90dfc36e6662a5b2f3fc99a15ddea40eeddc430e90c6d600`  
		Last Modified: Thu, 26 Dec 2024 18:32:15 GMT  
		Size: 34.4 MB (34393736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a70570d0d12ccc7d46da5a647bf0e8d14791b2bad187bade19a8fc81315cd85`  
		Last Modified: Thu, 26 Dec 2024 18:32:10 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:8175f3e9b1ffc7b12c103a95737b847ff15552709a5d27b373d8e0b3069eb7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.4 KB (979384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445ebd2a027a6637d9df097a30a78d59c30c979408f9940ca36a8e1753dc4bbc`

```dockerfile
```

-	Layers:
	-	`sha256:c9094410047ea6d64a2b11a0dcd7e1aa3de9543858ff9a1b0b882c72672f8d4b`  
		Last Modified: Thu, 26 Dec 2024 18:32:11 GMT  
		Size: 953.1 KB (953056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3b8a5ba2aebcc1fa3bef2df09fe2f68681b7b8b46e1da657a78830561baac6`  
		Last Modified: Thu, 26 Dec 2024 18:32:10 GMT  
		Size: 26.3 KB (26328 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; s390x

```console
$ docker pull ruby@sha256:de008faebbfdfa5453fbd45d3273c3f2c77d2443fa0de87f08cefa558562c7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46285781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8c6f7b37a955060383b43d2a903a925e976d1a683802b6dc8c6af654f0062c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.1-s390x.tar.gz / # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["/bin/sh"]
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV LANG=C.UTF-8
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_VERSION=3.4.1
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.1.tar.xz
# Wed, 25 Dec 2024 12:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=018d59ffb52be3c0a6d847e22d3fd7a2c52d0ddfee249d3517a0c8c6dbfa70af
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Dec 2024 12:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Dec 2024 12:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Dec 2024 12:03:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:93a724ed1843277c272a09a7779ca31a802938fe3a88142df42e291e0dc759c3`  
		Last Modified: Tue, 07 Jan 2025 02:32:17 GMT  
		Size: 3.5 MB (3459449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755f6e4a958ea84a86fd1204c1eaf0fc000c4ad7d2d2917fbe078a92e9780dc`  
		Last Modified: Tue, 07 Jan 2025 15:00:53 GMT  
		Size: 7.1 MB (7105482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4ac21584bcf5d23e118f84e8303785d4c0f278c59663ae36bad43f3db75f90`  
		Last Modified: Tue, 07 Jan 2025 15:00:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1077f1e3233d899c2f201e20c9a6682de7f94020c739b13b047a4d6e656d1a61`  
		Last Modified: Tue, 07 Jan 2025 15:00:53 GMT  
		Size: 35.7 MB (35720525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac91ca89d83c793e6e24931cce143b01c0f1ae973c9576fa01b624c0a1607c7`  
		Last Modified: Tue, 07 Jan 2025 15:00:53 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:0c485815e0bee3e2dac58a6954fae2d6e2159a712c1ad045b0b24198af9b05cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **988.5 KB (988546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b90d7024bae6662f32491d14416570d130fbefdaeae1c4840f3a5dcae259317`

```dockerfile
```

-	Layers:
	-	`sha256:4c710dc2cec45a8749da207def52ff37fd50475ee282b143f041c615a658c668`  
		Last Modified: Tue, 07 Jan 2025 15:00:53 GMT  
		Size: 962.3 KB (962292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f664d8a300312fb079ebd56fe509c1d1d703375c060cadc4af02cdb28b2dfae`  
		Last Modified: Tue, 07 Jan 2025 15:00:53 GMT  
		Size: 26.3 KB (26254 bytes)  
		MIME: application/vnd.in-toto+json
