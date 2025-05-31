## `ruby:3-alpine3.22`

```console
$ docker pull ruby@sha256:7826580e93d5e08bf2d1b3397adc5e57e4fbc9fdc71ac11820aa7644e4687b15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `ruby:3-alpine3.22` - linux; amd64

```console
$ docker pull ruby@sha256:017bd0bf72da696261a11a1575ab04d65b3340def62ce39219e8862fc0aa13d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42976954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373cd78e1c3feee30ed4a1fd3dc7a2b8fa724911698ed830998b381887bca6cd`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.4.4
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Fri, 30 May 2025 18:04:24 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522ad4c993aae9f229d493707aa5e0af3140470619d0ec81a67637dbf6b1da46`  
		Last Modified: Sat, 31 May 2025 00:06:37 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aef85a1f86aebeab92f4ce01dcf9d988daf8e7ec77846d75f65945c8c7a5e60`  
		Last Modified: Sat, 31 May 2025 00:07:25 GMT  
		Size: 39.2 MB (39179780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c937d05c1c76f11cd764aa86bb4994353e8ead94f84340103ec52186bb330e`  
		Last Modified: Sat, 31 May 2025 00:07:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:0bb6eaf1a31ab42d05e185cd7ed37b589cd247f0774f7fcfb4a0f7a9d6937a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 KB (231729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeda3f9644375e462de5949dbe1c9d1cf49799ea41dbbf947289ce3328e8bb9c`

```dockerfile
```

-	Layers:
	-	`sha256:0e4da2725144b6fd9e9554196268aafd08a2226d31582f7b12edd91aa9223c15`  
		Last Modified: Sat, 31 May 2025 00:07:24 GMT  
		Size: 208.0 KB (208035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d8c7297608488612116dabb53352e4fcefd34f13f6949e96c16c65737a4acb3`  
		Last Modified: Sat, 31 May 2025 00:07:24 GMT  
		Size: 23.7 KB (23694 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.22` - linux; 386

```console
$ docker pull ruby@sha256:6e82d26eb64944e1e06c05077496687d6836450146b3442a5d1e390065ab5bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38369484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d2d280e59de0ce05423da3946621898c21070295b63734d0c89c07500c2122`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.4.4
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Fri, 30 May 2025 18:04:26 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e3569626c2ab7487719d058923c0720169139ce5b370a9fe7bdc9e01d72230`  
		Last Modified: Sat, 31 May 2025 00:07:22 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e888cc5eba9dc77a030e4e80ec59d97910ebbd3ee03f2a0c92f6e505c4286f2a`  
		Last Modified: Sat, 31 May 2025 00:07:24 GMT  
		Size: 34.8 MB (34753128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f5bbd707e62cc276fae30002b672b37925af6c471284e5e3e1b24658ae5f5d`  
		Last Modified: Sat, 31 May 2025 00:07:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:dd016e19d7bf7180bb490239ff42c2d7e1e9d6678dadd17601df168e96223432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 KB (228638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf920c0724c4097ce2881e7ecb65ec57e9770b47fb518c9524c47ed9add48f8`

```dockerfile
```

-	Layers:
	-	`sha256:6a6020fba6b9c08b4559d151d3d0b408fd576baa228be83a8027c1398e5f0e29`  
		Last Modified: Sat, 31 May 2025 00:07:22 GMT  
		Size: 205.0 KB (205000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ad1f443dd0b89ab54c62ef65b0c1d39f82494067d2ada00995c2ded4262b76`  
		Last Modified: Sat, 31 May 2025 00:07:22 GMT  
		Size: 23.6 KB (23638 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.22` - linux; ppc64le

```console
$ docker pull ruby@sha256:1be9fa08250946788e6bb39b8ded8457c9dcd0a95ff3a2b5d86f012aca702c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40151531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adffbc0ff36b5b21e088020475a9796162e140a0155653a240cf27b7a399bfab`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV LANG=C.UTF-8
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_VERSION=3.4.4
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.4.tar.xz
# Fri, 30 May 2025 21:16:58 GMT
ENV RUBY_DOWNLOAD_SHA256=f76d63efe9499dedd8526b74365c0c811af00dc9feb0bed7f5356488476e28f4
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 30 May 2025 21:16:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 30 May 2025 21:16:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 21:16:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 30 May 2025 21:16:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Fri, 30 May 2025 18:14:22 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc492aa09ba6ba094b03567606500b7aa632647756572ee386cf287352e6e8c6`  
		Last Modified: Sat, 31 May 2025 01:03:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e9a106abee74bc81090093dd6d3bedb3ba300d485fa280649741c225e05713`  
		Last Modified: Sat, 31 May 2025 01:06:18 GMT  
		Size: 36.4 MB (36421017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d5acebf6966af835354fc20e5fb95555435f94fed42411bdfd0499c42f8c87`  
		Last Modified: Sat, 31 May 2025 01:06:17 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:613b11f42f079812f188fd2361e40ef56227f6a597edb635d90f261b36ba56d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 KB (226918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0730cf461b991f14915de66b17a2bf9a9850061e86e179b08c2337e7e6bfc6`

```dockerfile
```

-	Layers:
	-	`sha256:b042a4b8bfca1f1a7db13be88291a10215dbe72f88e1365f3fb806a9be5091ce`  
		Last Modified: Sat, 31 May 2025 01:06:17 GMT  
		Size: 203.2 KB (203152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5969fcc2c3a599488dae7c40c25ab76cb0172f1e409ee82dc2597a9224c7091a`  
		Last Modified: Sat, 31 May 2025 01:06:17 GMT  
		Size: 23.8 KB (23766 bytes)  
		MIME: application/vnd.in-toto+json
