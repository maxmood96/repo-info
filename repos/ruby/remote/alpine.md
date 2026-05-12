## `ruby:alpine`

```console
$ docker pull ruby@sha256:d74f431b0adecda2c66e0215ddb235cefc50ecc644efa6f1de4bdfd605ae25fc
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
$ docker pull ruby@sha256:9f9f8c4d4f8a3c96ff43ffaf43ca12afb08bc3b29a72a97b964f549118026c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50010087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3373a889b907bbdc22ba1fa0b04591f375f70130047927c2ed7c96321003804c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:22:35 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:24:50 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:24:50 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:24:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:24:50 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:24:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:24:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:24:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:24:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:24:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:24:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4818b355a6ed50f1243c45bdd1fb016c626daf395f75ea838aeeff6118f59e`  
		Last Modified: Tue, 12 May 2026 00:24:58 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80620863a53445b9d05a1ee2d2d52d7d862a32f7278330aceac0c58c348e6ce`  
		Last Modified: Tue, 12 May 2026 00:25:00 GMT  
		Size: 46.1 MB (46145568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3060ca4f1f803d0f4ce0bab09122811092422444fe29e083548c8a6b7470e991`  
		Last Modified: Tue, 12 May 2026 00:24:58 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:c2fd6fa7f05d58bf229d9f4fb6d4cc24efa1e8839082edfabc97e7bcf8611d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 KB (226544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e386e5e46d3c27a289d5d0a867890416188745d145fe8824759c6064c3c0105`

```dockerfile
```

-	Layers:
	-	`sha256:b1494c87554c291f8e1c33072c767ad538cb93f5937d1b2865a8aebc2f9926c4`  
		Last Modified: Tue, 12 May 2026 00:24:58 GMT  
		Size: 202.8 KB (202776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96741885ac62070912d829445e90f4390345584fb8c3f3850c39f631c5096458`  
		Last Modified: Tue, 12 May 2026 00:24:58 GMT  
		Size: 23.8 KB (23768 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; arm variant v6

```console
$ docker pull ruby@sha256:c02660c5657350ae287dc175e8df1b936f6fc5c4eda68efe1bf66aff8ca08986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42609590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6beeaa3ee12a9d12378eef196096ea5f030cbfd7b16543f04c96a4f631b2ff04`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:07:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:09:30 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:09:30 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:09:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:09:30 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:09:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:09:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:09:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:09:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:09:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:09:30 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bfa99c09ca9ccf94784e583d5d5bd617c5a75a737d1f8c326eaad9767d8ce74`  
		Last Modified: Tue, 12 May 2026 00:09:36 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc95f2715b41241973008b4dc81d222c167b773a40b27ba3839a245d744f70b`  
		Last Modified: Tue, 12 May 2026 00:09:37 GMT  
		Size: 39.0 MB (39037399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8db993bd732e71bed4153437e778b9fb99e4d3dc934183ae986e67d9673b24`  
		Last Modified: Tue, 12 May 2026 00:09:36 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:b6962ef7ded5943c4085866c23f65a9db68cb10a6313250aa41a843060467bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 KB (23691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b3f763a87434336fb6d8a6d7954d5d89405ed4be2fa555bec6f9a944df20ab`

```dockerfile
```

-	Layers:
	-	`sha256:c6d34fde289c3c4be6877dcea4b47c72628c258d7bd4af6cedbcf31c5ba8839b`  
		Last Modified: Tue, 12 May 2026 00:09:36 GMT  
		Size: 23.7 KB (23691 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; arm variant v7

```console
$ docker pull ruby@sha256:bfdbb38b6e39b8c558b3d028d5f2175b6ada47f3323dfa73e3811d0d4dc6d183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42151093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8763cddd18001093103402e3f72cb058b0fc1f0819db48c15da15afaad369f3f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:07:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:10:25 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:10:25 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:10:25 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:10:25 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:10:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:10:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:10:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:10:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:10:25 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:10:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a3ef3e75ea4a3afecfbfce4cc8df6902e9509aa0e7ce00f5f26d5c91378fd7f`  
		Last Modified: Tue, 12 May 2026 00:10:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe3dc8cfbccd67612ab70bc6c6a39a1de025d7994755a13183f7cedfbc8185b`  
		Last Modified: Tue, 12 May 2026 00:10:35 GMT  
		Size: 38.9 MB (38867641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3189a7c344b207534b017c73ca1dcbeb8f78b037a226d07c792f3753bf6dd725`  
		Last Modified: Tue, 12 May 2026 00:10:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:84dc529f69da4ce33ded96053f96c64187be5d72ab98fc134cf1773d4ac98732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 KB (226100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bf2006e597ceafd413743d4b6b6784aa0057fc6824ab2624974ec5a3ce6a3a`

```dockerfile
```

-	Layers:
	-	`sha256:49b80194dfc34e9916dbbaae9a4154a5a88a1ab25625f7e155560702a771b5d1`  
		Last Modified: Tue, 12 May 2026 00:10:33 GMT  
		Size: 202.2 KB (202194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5177291db734e53775e14c9e3d7274e39effb48d6ef29d5b19138970e53fd3e0`  
		Last Modified: Tue, 12 May 2026 00:10:33 GMT  
		Size: 23.9 KB (23906 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:61f881df0debf98c7f2cc3d34765b64ea84b0594c9ee76a0f6cef66978397d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50322753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f5a14b82d3f721390ff13d8e28bd1f5a31b7aff78b45c073e81ad1fb280bde`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:18:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:21:13 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:21:13 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:21:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:21:13 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:21:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:21:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:21:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:21:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:21:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:21:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a4a92e815bd5353a5e1d86da3b8ab4e2147a95688e2b9b17452391d1537d81`  
		Last Modified: Tue, 12 May 2026 00:21:23 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b190b8c48da9b8c2fdff3908ff5c5d8ae67361c254e91cdd6ed6d554cb20b91d`  
		Last Modified: Tue, 12 May 2026 00:21:25 GMT  
		Size: 46.1 MB (46122552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c701bd5ca4d470676ccdb5549e9fc6e03bc8781f69e3b34f60723fefeb4d8d`  
		Last Modified: Tue, 12 May 2026 00:21:23 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:70ecb14343db6f59d7167f75610b46ab73ce4e596d431a3b90f4930c66ff8db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 KB (226180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839a425f78bad4894d994a8392b0de04da88cf910fe701d3fc19a22834cc3a5a`

```dockerfile
```

-	Layers:
	-	`sha256:d974c6c1bf6ab3254af0447a53e0d3929ed627eda2d9c776ed31cb9a76b01a03`  
		Last Modified: Tue, 12 May 2026 00:21:23 GMT  
		Size: 202.2 KB (202230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44aab54a17755dd0509016c854c6d2d2301f608ecbc601dc035944edd73cbb81`  
		Last Modified: Tue, 12 May 2026 00:21:23 GMT  
		Size: 23.9 KB (23950 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; 386

```console
$ docker pull ruby@sha256:f108dec7b57f8e32b8ae1311add42f8a52f7bfbd1c01ee753945eded9911371e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42588160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c9dd8a35f68f885d3b5ed6170ec95bda8b7a9b24b7fac146d9700d45ee23d8`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:05:23 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:07:23 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:07:23 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:07:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:07:23 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:07:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:07:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:07:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:07:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:07:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:07:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf060da0439b8583efe8bd49ef7f203632f7b99eb9bef2b304df73d3e8df95`  
		Last Modified: Tue, 12 May 2026 00:07:30 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215bd61036550198da2417de490adab3f1df3f7a9e1a96955c1e1596755a5706`  
		Last Modified: Tue, 12 May 2026 00:07:31 GMT  
		Size: 38.9 MB (38897384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8860dbaa909c6bc5e650525a4ce923bf749c14e7cd744f558660d6de4fd40b7`  
		Last Modified: Tue, 12 May 2026 00:07:30 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:8c2d7fb8a10700e637b53d7e978765caa0e731edda3c3c9dac525dca2a76e630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 KB (223453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812c2e9865b366f5931077f9a60834b44e9fcca22d0309195a51977f0731231d`

```dockerfile
```

-	Layers:
	-	`sha256:965c509312e6dcd52db33babab120550fcd85ac763ae79077896b477208c2b66`  
		Last Modified: Tue, 12 May 2026 00:07:30 GMT  
		Size: 199.7 KB (199741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d9751601245792c448131e4b76c63ed169709ff56f619592ce661b8fc9ab21`  
		Last Modified: Tue, 12 May 2026 00:07:30 GMT  
		Size: 23.7 KB (23712 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; ppc64le

```console
$ docker pull ruby@sha256:dc9b585ad84d1cda32d38beeb8b5b66af070911811e65f51b10968d344e66921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44733211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7575f7617cd34e46945152be433c905370cea1f1f509840e04784fd2fb6a158`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 01:02:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 01:05:45 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 01:05:45 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 01:05:45 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 01:05:45 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 01:05:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 01:05:45 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 01:05:45 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 01:05:45 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 01:05:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 01:05:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314499a7a0af48f77ea9a03677698f927c34635f1e4b94ca63f36796e2728293`  
		Last Modified: Tue, 12 May 2026 01:06:04 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1bbe498bd1293bc0a58bd8f7e67d316d404acd71525d7e8de44606a0151f1d`  
		Last Modified: Tue, 12 May 2026 01:06:05 GMT  
		Size: 40.9 MB (40901952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a488936a628dec4a0b8b09ba5cce2b2282275f003f30e521f65dc14f212065`  
		Last Modified: Tue, 12 May 2026 01:06:04 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:3180b6e6a3bd975a8829e4b43830b59c9e93c9024dcb3ca42c6471e8d7b40dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 KB (223033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9120c81d8f308e6ce3d9e0911c06f9fc7c46f354c68521927d990f2eabe00874`

```dockerfile
```

-	Layers:
	-	`sha256:045d1452c8e91d79dacf8809757eb7440cb49b75316fc49893edbedd15ec0e6e`  
		Last Modified: Tue, 12 May 2026 01:06:04 GMT  
		Size: 199.2 KB (199193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:321040fb8216116c8d88c9e82bc30b0e736aeca082a6ae32527f97b7714a7070`  
		Last Modified: Tue, 12 May 2026 01:06:04 GMT  
		Size: 23.8 KB (23840 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; riscv64

```console
$ docker pull ruby@sha256:3423080ba661b1cd39846293d97e9b10e0d8009b2e665109cc4a6afa4ef7fce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 MB (48013770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27206a14765c8ad047b1ba5084860073a3bf9b591a4673fe9c2a72230203a9f9`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:48:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 21 Apr 2026 23:57:46 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 23:57:46 GMT
ENV RUBY_VERSION=4.0.3
# Tue, 21 Apr 2026 23:57:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Tue, 21 Apr 2026 23:57:46 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Tue, 21 Apr 2026 23:57:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 21 Apr 2026 23:57:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 21 Apr 2026 23:57:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 21 Apr 2026 23:57:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 23:57:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 21 Apr 2026 23:57:46 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964fd66fb73a93026d2f560b41883a889f4fba9d610309f18f6a275a6e7c280a`  
		Last Modified: Fri, 17 Apr 2026 03:05:28 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9c704c37f9ed2dcc37af68a5a952c124cba3ccbb475796737d46302cee565c`  
		Last Modified: Tue, 21 Apr 2026 23:59:15 GMT  
		Size: 44.4 MB (44425780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6738e5eb2bf8d2e9aece90a7bdaedab9a38c114b68132d0fc67db1199126a2d2`  
		Last Modified: Tue, 21 Apr 2026 23:59:08 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:60318fa3b8d55b07f851dfb16c244f3fd7f59f2ba309b05205ba627c92dc7cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 KB (223025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7342128f73c1e2968ab976bc1f14f162d13271ce4550862e0d5a3e99d99c9ed`

```dockerfile
```

-	Layers:
	-	`sha256:7fa8dfa6c2dd97c2202ab782714d9ddd259ffd643adf4efd5f5df8e34d22e75f`  
		Last Modified: Tue, 21 Apr 2026 23:59:08 GMT  
		Size: 199.2 KB (199186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8898c98e9d0f2ad34b1112e4159b1518c802ab820262e3fb876b886c5dd225c7`  
		Last Modified: Tue, 21 Apr 2026 23:59:08 GMT  
		Size: 23.8 KB (23839 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; s390x

```console
$ docker pull ruby@sha256:e6409ebbd9dbfffbc4db6dbfe671b0354b9dd562a7895761dae3b0b2076193aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44245894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c92d2c7b17a94e9f055440142a43f184b3fc3cd3c0383d98e1a778cf4ee02`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 12 May 2026 00:09:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:11:51 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:11:51 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:11:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:11:51 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:11:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:11:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:11:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:11:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:11:51 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:11:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8d886a2c4066c78e7eb208bbc4ca2fe7fd475ec3c698338eae2b10937066ab`  
		Last Modified: Tue, 12 May 2026 00:12:03 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b901396c978ce9e52a758ec4c93f9a85b7c967c30be88e9546d6b2d205b8bf68`  
		Last Modified: Tue, 12 May 2026 00:12:04 GMT  
		Size: 40.5 MB (40519034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c3d3bb1e2cdc2bece24fe5a39cb1a0893723131398e3fb462af12ea47e7db`  
		Last Modified: Tue, 12 May 2026 00:12:03 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:2dd5130bb01258a95d85fbb093fe29debcbbb3f0743675b8e62362dca62e2f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.9 KB (222902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ac5c0c194b640178b31cbf2abd85737d9265140441c6f981b79004c05f7f8e`

```dockerfile
```

-	Layers:
	-	`sha256:3e34e2da19817b2cf710fe04941939e94a042123701563ad4c1c0f06c6079b19`  
		Last Modified: Tue, 12 May 2026 00:12:03 GMT  
		Size: 199.1 KB (199135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c8e7e76788068074932cd5c0687f5c2bcddd58deddbbb0e59d4d6c13a2be65`  
		Last Modified: Tue, 12 May 2026 00:12:03 GMT  
		Size: 23.8 KB (23767 bytes)  
		MIME: application/vnd.in-toto+json
