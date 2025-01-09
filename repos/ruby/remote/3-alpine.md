## `ruby:3-alpine`

```console
$ docker pull ruby@sha256:6c2d534dc79e4fd4c36bbcb8a9b7e2b7f8fcf5bf5af7deeed94bb216d9c5aad2
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

### `ruby:3-alpine` - linux; amd64

```console
$ docker pull ruby@sha256:85bea6ca8a1d9583dec5831fd4d18d486402ff455fd3827fa1f052ba903ad2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49391680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e861606e687682a35ad5275466ab4505280ff24330849123958c8ffbe547529c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c786f76e374fc91fb623f07cd2aa47899e9a2d0e468d9543832593cc11ee7e5d`  
		Last Modified: Wed, 08 Jan 2025 18:16:29 GMT  
		Size: 6.7 MB (6738188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe95a7e27e29a4ac22512cc3f737a3001efab7bbd2df6c0b7ee5ad4e782a9c9`  
		Last Modified: Wed, 08 Jan 2025 18:16:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02b6fd5b71340ecfc7f8b26c79598a8e064dc36707f8b4b70368ed69fe2e3f9`  
		Last Modified: Wed, 08 Jan 2025 18:16:30 GMT  
		Size: 39.0 MB (39011452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7be61ea53639a35b64876d1934cdff4e895f7f4f54c4d9bbd71de1d41fe0e9`  
		Last Modified: Wed, 08 Jan 2025 18:16:29 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:3e713b4b04d39779db99f3c31e90765ba7b9e4a4f80a6d865fdc16fc9f75f67c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.6 KB (997626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6eb2d09cec096709339f14615544fd77f7107478389d281d8c9cc820344505`

```dockerfile
```

-	Layers:
	-	`sha256:4737b0229aa487b8ee17e535dfd418486f38a11d25611115df918f785c1ed5a8`  
		Last Modified: Wed, 08 Jan 2025 18:16:29 GMT  
		Size: 971.4 KB (971372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8729021973452c760db2c47e0bcd6e418ec177647ddf283a7ec0de6894000d86`  
		Last Modified: Wed, 08 Jan 2025 18:16:29 GMT  
		Size: 26.3 KB (26254 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; arm variant v6

```console
$ docker pull ruby@sha256:182ff7cd9c62bfb3f406f88004c4b82eabf80ad10e6140ea3699a5973538ec01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44374210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27020d96710713b414f4714b484ba469d2d8e060e8777cb892a7788b7b2bd16d`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
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
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af466a850274c5cfc460ffaec5dc34aa83ce770328c0692bb6db6211cb9504b6`  
		Last Modified: Thu, 09 Jan 2025 08:32:34 GMT  
		Size: 6.6 MB (6562228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c457e26642d0738844c2ccdcdab4f06ed5846e0b9963f30c667d237d95f74e3a`  
		Last Modified: Thu, 09 Jan 2025 08:32:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87888fafe1d52ff12e7dcb8a3920584631f6b33e5102765f3ec73a0aa2758767`  
		Last Modified: Thu, 09 Jan 2025 08:32:35 GMT  
		Size: 34.4 MB (34447778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663bd19bbc112a0a19ce7d90bc9cf84034f67ae1ee809623a6bdd026d20f3a7c`  
		Last Modified: Thu, 09 Jan 2025 08:32:33 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:31dc7d31fcd1cb9ad236eca514935cfc71e0215ce02032771bde1b9f1e56e9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc7e01b77ab698f8bf4d4d79190b677e24ba27ee2fa486b856ecdbb6387a85c`

```dockerfile
```

-	Layers:
	-	`sha256:53d44c5da7d968285da2caa908b6a60325d5fd69dbab62a8aeb982d008adf3a9`  
		Last Modified: Thu, 09 Jan 2025 08:32:33 GMT  
		Size: 26.2 KB (26186 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; arm variant v7

```console
$ docker pull ruby@sha256:fc2a377ad24d4d62c97a2786062909b052ca4a9e42e846ad450713ec0831f5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.8 MB (43814468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3c19cf1d0132841166d165cd3492611a0f602bb60775fa9f0ac5d056456c0c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
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
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06b963bedc19582f09d28a1c302370df2114505862ef2a5ee797e6f95c2ce4`  
		Last Modified: Thu, 09 Jan 2025 09:06:53 GMT  
		Size: 6.4 MB (6404600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6829b8e64350e12f38023dc192f421050f0bf2638b3b406cee27d9c3b681911`  
		Last Modified: Thu, 09 Jan 2025 09:06:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99dd12479864d9fb2545155b9a1f7a2d1d2000bafb6f55b144189cfe4720a1a`  
		Last Modified: Thu, 09 Jan 2025 09:06:53 GMT  
		Size: 34.3 MB (34312431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30df1c09459cd3a7d0cf026537a58b2f1c124035635c1b903ad2c8d6abdb9e3c`  
		Last Modified: Thu, 09 Jan 2025 09:06:52 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:94b696833011cf95b195a44587ca4cb34f68633a532d2bf3020408b044bf91d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.5 KB (979510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69bdb3db275a86b0ae41ebb9c2f1f5c0786a1225507dd323455edd0c47bdc2b`

```dockerfile
```

-	Layers:
	-	`sha256:b436e148761552f829681855abef32caba5307e5481c3cb129fd9d2487499554`  
		Last Modified: Thu, 09 Jan 2025 09:06:52 GMT  
		Size: 953.1 KB (953109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74ac6f6363e14eb922250d4628ee71e22604de4bc464884df4ca967bfc9b485d`  
		Last Modified: Thu, 09 Jan 2025 09:06:52 GMT  
		Size: 26.4 KB (26401 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:b386ee545ca9c159f4bae64e03b725af68d112e68914c740b1515322b710ed0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49759051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189faf94b322f4c99e9402860a1f467ffbcdf0a2d72c8dae1d48f562706b7f98`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96696564a66275d9a8befd8604f11e7f341379fd0685f5e2c002f42527b75a67`  
		Last Modified: Thu, 09 Jan 2025 05:39:25 GMT  
		Size: 6.8 MB (6771547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6747a89512ba90600968fdc2aa00ac683aafa9b86b5071c57dda5496065487`  
		Last Modified: Thu, 09 Jan 2025 05:39:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c292aeb3212c09a1f3a8377863414335e7395905af3147bbe19ec0e64c6564b5`  
		Last Modified: Thu, 09 Jan 2025 05:39:26 GMT  
		Size: 39.0 MB (38994820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa5dc8904c73e079371a6183d9b30c96e809ce700be9cd61260083ebefad52e`  
		Last Modified: Thu, 09 Jan 2025 05:39:24 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:9f71c081a196427474af94ad01dbdb437a56de956660df22af374756345e0c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.8 KB (980809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83c8f773d94ced1de2229894460dae346be99e372244778e41aafa03796de4c`

```dockerfile
```

-	Layers:
	-	`sha256:e91e231c9d1f8f7c1f3c08d6cd02c3a8f2438e0f8c98f702c3be265871a48c6b`  
		Last Modified: Thu, 09 Jan 2025 05:39:24 GMT  
		Size: 954.4 KB (954358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e8c8853cea9d8bbab1a401f84def2b588efebb83b35eb2141d58af93a5323b`  
		Last Modified: Thu, 09 Jan 2025 05:39:24 GMT  
		Size: 26.5 KB (26451 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; 386

```console
$ docker pull ruby@sha256:dceb073507d709d3175c7582d663bd3ca47e009d3966ef77547a3dbb62cf73bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44594994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573b95e8e2f93743136937ad7d7f5329d085e1cbc68acddddf1dec41c8b4d68f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
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
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eba38edb91c15dd34a8c53aa0a64eb8b53b9748ab3528e388efd596bd0ceef9`  
		Last Modified: Wed, 08 Jan 2025 18:13:57 GMT  
		Size: 6.8 MB (6808886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f703871f810a5663b1710c83ad631644432d9cbfb113a81482fe9a5e8117a8`  
		Last Modified: Wed, 08 Jan 2025 18:13:56 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e1fce3281bcd6b760193904c16f9f9a28611ae618f1aa6fb894609e6456c3f`  
		Last Modified: Wed, 08 Jan 2025 18:13:58 GMT  
		Size: 34.3 MB (34322659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90ae527a21f5f483a721f1a6d83c3e90f3b27682d2929dbcfb81fad63d7aae2`  
		Last Modified: Wed, 08 Jan 2025 18:13:56 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:429147e250c2c11a0254812ccd036d99ff75669e2722a2cea9e98bce57f79200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **997.5 KB (997523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb12d57e4f2fe94edf012389aed5bfefbb2568d2e93fe8d800a73c11b552250c`

```dockerfile
```

-	Layers:
	-	`sha256:0a550ab58384b57db6dc24e2500d7dd3b3c56e34c0cb1c2383984605fd24208a`  
		Last Modified: Wed, 08 Jan 2025 18:13:57 GMT  
		Size: 971.3 KB (971327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bfe47000cb83cf7c80ac1bd446c93cd6dfbf01a583e7626c45300c37be26d2f`  
		Last Modified: Wed, 08 Jan 2025 18:13:56 GMT  
		Size: 26.2 KB (26196 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; ppc64le

```console
$ docker pull ruby@sha256:764fc429a95589337301d8ecf74048f791c76d751ebcd8a9e6c896fab99d7f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46468295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b13e335fa62c415d04dbd19a8d263d3da7849c1d6e669fe115eb7195d30ef4`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
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
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9e2f6b3581b52bff77bf2c10aa7b9708f87de5e097130ee9f026657c08aa6`  
		Last Modified: Thu, 09 Jan 2025 00:33:22 GMT  
		Size: 6.9 MB (6947855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524db264acb9a23ad8e3467ae4eeca651c7911840ea0ec56950a479b77d619ca`  
		Last Modified: Thu, 09 Jan 2025 00:33:22 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa07ed52c6cc9de640b8d6ebd7d7ba7bdc5b7a7902790e4f0cc2a1a2e2897b`  
		Last Modified: Thu, 09 Jan 2025 00:33:23 GMT  
		Size: 35.9 MB (35946513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569e45beb7c39b164d9e1f9a5aba043b90f461822ab0bfa04bb2e89c9c987d7c`  
		Last Modified: Thu, 09 Jan 2025 00:33:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:5c093dc3cb959bece2a4f01eff7fd0d57eea27e0a5aae3039ec50f75afa97936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.6 KB (986628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be67454b655592ab72cd3f239e156ca2634874da4b3ef262b361fbbb04f1450e`

```dockerfile
```

-	Layers:
	-	`sha256:260c454369aecbfcec80364bbd1a5f947965ee2ecf906f051420b40773621aca`  
		Last Modified: Thu, 09 Jan 2025 00:33:22 GMT  
		Size: 960.3 KB (960300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e79cb4790b7509d6cc6a4e3d55f1a2e70036075e8744e67ccc473c703304089`  
		Last Modified: Thu, 09 Jan 2025 00:33:22 GMT  
		Size: 26.3 KB (26328 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine` - linux; riscv64

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

### `ruby:3-alpine` - unknown; unknown

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

### `ruby:3-alpine` - linux; s390x

```console
$ docker pull ruby@sha256:5ab32d2b0b0cb965bbf61e4ad5de4b981000210ae391a42daeb8587a178ae91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46300137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5790fd230ddc7027401ea51601f05d5435803f774fda6a2f1535ed5ff24a0104`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 25 Dec 2024 12:03:23 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
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
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc63c3fee81c318f448a556f5432cdc819fb476a80d6f1ac75f71d7e8707a555`  
		Last Modified: Thu, 09 Jan 2025 06:48:02 GMT  
		Size: 7.1 MB (7112968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29bb53d4b30761d50dcfaa0d23ab2332960f3ad75638ed2b05867955601501e`  
		Last Modified: Thu, 09 Jan 2025 06:48:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0da5c373c598b2a2758cf6c89edc0fda2374a8e09d420c719fd7b3db6613eb`  
		Last Modified: Thu, 09 Jan 2025 06:48:04 GMT  
		Size: 35.7 MB (35719979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2eedf63f37543d1de36125faad07443b3bed3554413ff94ca49c7d0a8c78bd`  
		Last Modified: Thu, 09 Jan 2025 06:48:02 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:3645877343457db0a5c8fec63b73de57e510a683fd2e761b31ebb0dcc79415ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.4 KB (994424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6635a02aefb2517ae998c50c63e83e9acff7e3360d8be34f697376a52433a31e`

```dockerfile
```

-	Layers:
	-	`sha256:78f27d3c3826d5ebcaad20c373fdab88ead693db3e957ffe248646afefba0562`  
		Last Modified: Thu, 09 Jan 2025 06:48:02 GMT  
		Size: 968.2 KB (968170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90277b5640b3546ecb9dbb1434871460602363e802fc6bd72259b3bc221018d3`  
		Last Modified: Thu, 09 Jan 2025 06:48:02 GMT  
		Size: 26.3 KB (26254 bytes)  
		MIME: application/vnd.in-toto+json
