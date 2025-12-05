## `ruby:3-alpine3.23`

```console
$ docker pull ruby@sha256:0fa90fb5c08fb0a2d345d57967641085a6f6636781465e1eb0287c02e96971f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `ruby:3-alpine3.23` - linux; amd64

```console
$ docker pull ruby@sha256:99079ca339c8183ce343c4d6b7c23c3d9b81fa44c55adbf9f48f4ba3d059f32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43103410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abd6f21bd9cf195020f5f28d22d79154b041d49e93f8ceb085c744b34288b1f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:25:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 04 Dec 2025 22:27:51 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 22:27:51 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 04 Dec 2025 22:27:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 04 Dec 2025 22:27:51 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 04 Dec 2025 22:27:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 04 Dec 2025 22:27:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 04 Dec 2025 22:27:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 04 Dec 2025 22:27:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 22:27:51 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 04 Dec 2025 22:27:51 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ebd804a65b5c2347887ba739623b58b4490d3ced04ebbd63ed9fc0beeb649`  
		Last Modified: Thu, 04 Dec 2025 22:28:05 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfd254d68b4c8b9450e2afe0da8227f01a094a39b1a6a5ca3b19fe2d310320e`  
		Last Modified: Thu, 04 Dec 2025 22:28:11 GMT  
		Size: 39.2 MB (39243769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcff6b396a3966b1f9a46fca3fb054761f5fb9489903f09ff56cf7120deb893b`  
		Last Modified: Thu, 04 Dec 2025 22:28:05 GMT  
		Size: 137.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.23` - unknown; unknown

```console
$ docker pull ruby@sha256:718191d6da4930a964f6fbc9cf77b632d37f55d48f55133a9429b09aaef58130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 KB (230379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a9045b58d752b3179ee7102d2366d8467e6de9650c94c74c820fbb41fefe7c`

```dockerfile
```

-	Layers:
	-	`sha256:64aa1224fbe7c19917c64a7b10ea2a5a095909b598b88b7da0c6708b33ccc391`  
		Last Modified: Thu, 04 Dec 2025 22:44:55 GMT  
		Size: 206.7 KB (206728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0177cccc74a316790f5c90c51ab92a490169285c97501c48ab2f3cb5c20e542c`  
		Last Modified: Thu, 04 Dec 2025 22:44:56 GMT  
		Size: 23.7 KB (23651 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.23` - linux; arm variant v6

```console
$ docker pull ruby@sha256:1edcf92acbdcd109edb54617085a958bcadac374a70f8c935f1041a170f6b31e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38504550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd46f71fbcd2032b305f5792e13018aa6373a38cb9303d1406a7347ac814b5b7`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:24:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 04 Dec 2025 22:26:38 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 22:26:38 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 04 Dec 2025 22:26:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 04 Dec 2025 22:26:38 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 04 Dec 2025 22:26:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 04 Dec 2025 22:26:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 04 Dec 2025 22:26:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 04 Dec 2025 22:26:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 22:26:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 04 Dec 2025 22:26:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41242a068b489384d8b3dee2527b951c8eadb4c2e56f85b4f14968f78b3a4ebb`  
		Last Modified: Thu, 04 Dec 2025 22:26:51 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c524cf24c6c3b0d58634ad8822d56b4b310a5c2b83da200a1bbb7e773d56cec`  
		Last Modified: Thu, 04 Dec 2025 22:27:00 GMT  
		Size: 34.9 MB (34936328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74abe26ff67c446a034411a732afd239d306f5157efafb8a12556dd4ec2ef08d`  
		Last Modified: Thu, 04 Dec 2025 22:26:51 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.23` - unknown; unknown

```console
$ docker pull ruby@sha256:02a12ef3f1482dc6d07e1fff052d82f56fe5ef2923e4bf8ba41b68ff3b98c974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 KB (23574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ed214bfe150f6a2f639b7b23a40b0a2da6821d9789fb6c27e9f4d30daa8e14`

```dockerfile
```

-	Layers:
	-	`sha256:5de6e7be0c214927a8296a7f07f10dda8b99e1292509a97b5b04b42bcf18f7aa`  
		Last Modified: Thu, 04 Dec 2025 22:45:01 GMT  
		Size: 23.6 KB (23574 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.23` - linux; arm variant v7

```console
$ docker pull ruby@sha256:8af4cd21ded3d49717993a47c4f61a4cea7aa844ff765940ee95236a0483f3de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 MB (38076020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e696f82a7c559fca4e0fb844c813ac5ebb15fbbdcb43d07c87703e8c176fc75`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:20:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 04 Dec 2025 22:23:06 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 22:23:06 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 04 Dec 2025 22:23:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 04 Dec 2025 22:23:06 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 04 Dec 2025 22:23:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 04 Dec 2025 22:23:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 04 Dec 2025 22:23:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 04 Dec 2025 22:23:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 22:23:06 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 04 Dec 2025 22:23:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d698b9161d3393ecd0f0cdf0a4b897b05d854a9ced2ea4418cd2652e773554b2`  
		Last Modified: Thu, 04 Dec 2025 22:23:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59978706bcecd4ac587b51cf46a6dab3390a41819aa72a20b3ffc35c2eb4b7cb`  
		Last Modified: Thu, 04 Dec 2025 22:23:24 GMT  
		Size: 34.8 MB (34797226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b8a0612d336b2300a85db6c2e150b32ea4f6a36eb90ea915da926b986c8db6`  
		Last Modified: Thu, 04 Dec 2025 22:23:20 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.23` - unknown; unknown

```console
$ docker pull ruby@sha256:1fffd92ade09a36190f242bcc8fc2a051b6d14d44868a8a464dbb2a8c78fdf43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 KB (229935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7bf2c6d62c56980adc143ccae18d5d4a9e6b6e930794d2771e8e8ae883daeb`

```dockerfile
```

-	Layers:
	-	`sha256:3cb4b24c95ec3bfc43c704798210c187b0f8352bc834c23b1d1a1b266857489b`  
		Last Modified: Thu, 04 Dec 2025 22:45:04 GMT  
		Size: 206.1 KB (206146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2894ac3159d50e3a12532765422f5944903c33172bc3a41791ae5ee0ab3133b8`  
		Last Modified: Thu, 04 Dec 2025 22:45:04 GMT  
		Size: 23.8 KB (23789 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:c2e8b5110c1efb63735dab30c5b8fac03ee2fd258aefb8ea2f58e285561d891d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43439435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bb0c81042af8f385f64102a2e19add8dabbf016938025e9a3461490faa39ed`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:22:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 04 Dec 2025 22:24:55 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 22:24:55 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 04 Dec 2025 22:24:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 04 Dec 2025 22:24:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 04 Dec 2025 22:24:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 04 Dec 2025 22:24:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 04 Dec 2025 22:24:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 04 Dec 2025 22:24:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 22:24:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 04 Dec 2025 22:24:55 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1875b3917a159a0ed3be15b47970081b619218abdb1c81e17125c692b3c1a7`  
		Last Modified: Thu, 04 Dec 2025 22:24:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c59676c18074e48f056fbc400ae3c85198fd75b89bb46338a265ee9aca898f`  
		Last Modified: Thu, 04 Dec 2025 22:25:13 GMT  
		Size: 39.2 MB (39243908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729370e7c113850789fdeb79c583fb572fd87c9c37be1f00b70944939a3e3caa`  
		Last Modified: Thu, 04 Dec 2025 22:25:08 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.23` - unknown; unknown

```console
$ docker pull ruby@sha256:c8b4b64ff6f4f24849c3cf44fbacabb00c04ae5a59bf9b456bf72ecd6187e189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 KB (230015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63481bbcc8f5f65b79cd3f22446ea68acf359993e0eba188ceb79aa54929bd49`

```dockerfile
```

-	Layers:
	-	`sha256:57d8590f74ac9c4b613120db906c29c342bff67f8e3c4017f33a34fdd0b386b7`  
		Last Modified: Thu, 04 Dec 2025 22:45:08 GMT  
		Size: 206.2 KB (206182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c82ca99921b30a537914349c671a2037d7d33cc1196dd702b05979dccedc9d2a`  
		Last Modified: Thu, 04 Dec 2025 22:45:13 GMT  
		Size: 23.8 KB (23833 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.23` - linux; 386

```console
$ docker pull ruby@sha256:57b9f1b40e79770c72e0cd58ec2de838ee5a27a2e660ce50a8ae4fc316f3d0e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.5 MB (38453548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f052ff43b3d98fd54df2b396d7685f8a1b225b9f4c093b78fd55bb09056211c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:22:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 04 Dec 2025 22:24:18 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 22:24:18 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 04 Dec 2025 22:24:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 04 Dec 2025 22:24:18 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 04 Dec 2025 22:24:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 04 Dec 2025 22:24:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 04 Dec 2025 22:24:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 04 Dec 2025 22:24:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 22:24:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 04 Dec 2025 22:24:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a458cb82612278ae784c1f0cc247458da12766aff7e1a38bfc698f2ec7a649c`  
		Last Modified: Thu, 04 Dec 2025 22:24:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca2e80b397c2d3ec0c15cae4eb88b7b854a589cdaad39ae72c64daeac137410`  
		Last Modified: Thu, 04 Dec 2025 22:24:48 GMT  
		Size: 34.8 MB (34767365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4a6ffd40188b1da883ba59d3162237213b16e90ca4b6cef958b0601534ad14`  
		Last Modified: Thu, 04 Dec 2025 22:24:34 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.23` - unknown; unknown

```console
$ docker pull ruby@sha256:204da95c70092bc199a93ad2fd8c29dee68024d6e2f3095e7ba1ca531107e98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 KB (227287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793583c83c9eea71734c0fe190d0fcbca685645059546116f75d8b58f92adc88`

```dockerfile
```

-	Layers:
	-	`sha256:7cfe38875daad6d57d2937eddc330e293dbdf832f754dd4150b9db7b56dab8ad`  
		Last Modified: Thu, 04 Dec 2025 22:45:17 GMT  
		Size: 203.7 KB (203693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0d9830ac1c9d4fb9cbe8ec2390c7b9d9bf639f272b37d6eb5dc80357cbd495`  
		Last Modified: Thu, 04 Dec 2025 22:45:18 GMT  
		Size: 23.6 KB (23594 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.23` - linux; ppc64le

```console
$ docker pull ruby@sha256:e6ac229c709cd57194ec29d93e94dfa0e0f921b16b65159d0662e8792c824924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40490706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba120157107a41fe1cac415281d1a3c1b28d2427441182d47103d91e44db925`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 22:31:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 04 Dec 2025 22:35:00 GMT
ENV LANG=C.UTF-8
# Thu, 04 Dec 2025 22:35:00 GMT
ENV RUBY_VERSION=3.4.7
# Thu, 04 Dec 2025 22:35:00 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Thu, 04 Dec 2025 22:35:00 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Thu, 04 Dec 2025 22:35:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 04 Dec 2025 22:35:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 04 Dec 2025 22:35:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 04 Dec 2025 22:35:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 22:35:00 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 04 Dec 2025 22:35:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac41d9c710e429b12352e49659d95e1a878d6156b0e7be442eb5728421b6be0c`  
		Last Modified: Thu, 04 Dec 2025 22:35:19 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d0740874032b21b52d3413bd7d26c21f3dbd095d4160ee4c76fe382b6dabb7`  
		Last Modified: Thu, 04 Dec 2025 22:35:35 GMT  
		Size: 36.7 MB (36663363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6caf29f5b2b80eec9c02e7551d84e86b0afddc96e2e1fba21ba350f090ba5a2a`  
		Last Modified: Thu, 04 Dec 2025 22:35:23 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.23` - unknown; unknown

```console
$ docker pull ruby@sha256:a6873cec73cbc830b77c180d85a879c0388a38b0a398edd46bbc143996c4a288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 KB (226867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55297424803e01d14f300a5c743785cb1728c1420290cf7ba6e358d09d16455f`

```dockerfile
```

-	Layers:
	-	`sha256:e8c0f0e441316e63a8c9d7ddca3e0801132e6f4477fc948c6ff1ba79b786732e`  
		Last Modified: Fri, 05 Dec 2025 00:57:43 GMT  
		Size: 203.1 KB (203145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67a2d2c90e75acdd65eb04298b4546ac8e0161cb0734d0706279ee6dbdf0f03f`  
		Last Modified: Fri, 05 Dec 2025 00:57:44 GMT  
		Size: 23.7 KB (23722 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.23` - linux; s390x

```console
$ docker pull ruby@sha256:097aa9243caab3e7e8e38851b2a3d37596ef4963684905291987fbaa0810cc7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39880737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09add15979b77cfdc8ce9e9969653edd506df50655e441df9daab97d1ad7c817`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 23:59:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Dec 2025 00:03:58 GMT
ENV LANG=C.UTF-8
# Fri, 05 Dec 2025 00:03:58 GMT
ENV RUBY_VERSION=3.4.7
# Fri, 05 Dec 2025 00:03:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Fri, 05 Dec 2025 00:03:58 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Fri, 05 Dec 2025 00:03:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Dec 2025 00:03:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Dec 2025 00:03:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Dec 2025 00:03:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Dec 2025 00:04:00 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Dec 2025 00:04:00 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f419b1ba133e200c5637aa89448c06ec846634b6aaafec356fdcfed7a8d054f`  
		Last Modified: Fri, 05 Dec 2025 00:04:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a79417665441c68b4910db78ec4a7010872c062c36d7a2746da83fa33f1efbb`  
		Last Modified: Fri, 05 Dec 2025 00:04:35 GMT  
		Size: 36.2 MB (36156598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508e1609b5b0b37e4b97fb4ae8e0d878a1693d77843c40fe320e3d6c3f6762bd`  
		Last Modified: Fri, 05 Dec 2025 00:04:31 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.23` - unknown; unknown

```console
$ docker pull ruby@sha256:eef2f076002e5da57f1ad9c337df01957d3ba2155f7e4935065c03b97ad9a494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.7 KB (226738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daa5a994bce2744dbe79807c89afac401e465feceeec30faeb7e000347fd7e4`

```dockerfile
```

-	Layers:
	-	`sha256:7615138bd03b71b73dde8772c34e18fd29f1af394027a5bf880e679f2891373e`  
		Last Modified: Fri, 05 Dec 2025 00:57:46 GMT  
		Size: 203.1 KB (203087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9607504efbfc8ea343eacabb28577d9c145b5085973d18fa02d535ceb5a1a7c1`  
		Last Modified: Fri, 05 Dec 2025 00:57:47 GMT  
		Size: 23.7 KB (23651 bytes)  
		MIME: application/vnd.in-toto+json
