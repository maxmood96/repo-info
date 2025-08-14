## `ruby:3-alpine3.21`

```console
$ docker pull ruby@sha256:161e52ab2f11b1ffbb803ce9f2a086f82bab8566b565ba8fd68a55510466d948
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

### `ruby:3-alpine3.21` - linux; amd64

```console
$ docker pull ruby@sha256:c81c7391650b202117cd09a23311db44be0d2b8e4585232ed47c6746277c74ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42801084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ebf5f61dbbd47cf0ae76e438635d6e92854c9c36caf0fc1c594f81f124371a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV LANG=C.UTF-8
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_VERSION=3.4.5
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f69142b9a37e5683109dcf786620030d953f0c658519c99a87c34a963b8215`  
		Last Modified: Tue, 15 Jul 2025 20:25:26 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915da332df2276612c38ca451f1373ffa3d7531f724e36f6c4e01e7b767920ce`  
		Last Modified: Tue, 15 Jul 2025 20:25:33 GMT  
		Size: 39.2 MB (39163187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0d3ad2634a366b570a2036575e9aa4fe8eebcfb572b4399d6efa5c5712f658`  
		Last Modified: Tue, 15 Jul 2025 20:25:28 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.21` - unknown; unknown

```console
$ docker pull ruby@sha256:47e325b4bdfb3d21bbfdce82fe5b44e61acb3b08c3c33cb4aa8dd949a5feb020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 KB (228552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7f11109f4234d9340bc39779051aecd5ab63106e62d0a5db068f0964aa2b92`

```dockerfile
```

-	Layers:
	-	`sha256:71412b91309c6de1315edc7bea4c84bab8749d8f34525e91dc900d081b7cbdbe`  
		Last Modified: Tue, 15 Jul 2025 23:57:29 GMT  
		Size: 206.1 KB (206058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecaea46c7d9b07cbe833b9ef0b6cb5b59b36a851d445021839bdb3e5bc0d93d3`  
		Last Modified: Tue, 15 Jul 2025 23:57:30 GMT  
		Size: 22.5 KB (22494 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.21` - linux; arm variant v6

```console
$ docker pull ruby@sha256:36e91000cb18ac466ebc7a7791a71303f20101f0f729bcbcccc16e59da0a58ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38239407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f52283f18403b9afd6b1c9dd977d48b26ec74f7c7c846e759126733848ae22`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV LANG=C.UTF-8
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_VERSION=3.4.5
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ca0c331561564c536ffa9246944bb50ac21d3fb11fe66c38baad97fdd1f05719`  
		Last Modified: Tue, 15 Jul 2025 18:59:41 GMT  
		Size: 3.4 MB (3363814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffd2aade873422152cd38c54790f33c3043c235216377097742a4ec943cea10`  
		Last Modified: Wed, 16 Jul 2025 03:14:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c940bc61c375730635fe7d29ed75d3a2876c8c9136df26b4e3a56d129116e947`  
		Last Modified: Wed, 16 Jul 2025 06:24:43 GMT  
		Size: 34.9 MB (34875265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1a49178b8d874b9c58f9c2e074a9f339940a93e857828c4c4e4539c46de744`  
		Last Modified: Wed, 16 Jul 2025 06:24:40 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.21` - unknown; unknown

```console
$ docker pull ruby@sha256:dc383978fd8a2fe9493500a79f45fa444d84dd07d453f6470863c7412e4c2bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 KB (22381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2ba9814ed4d817ccd6af172b95a5ce72526878cdbb5e505187c9bf9da22c8d`

```dockerfile
```

-	Layers:
	-	`sha256:8936a28f43a5b3d7b80c25ae29eb6b027c4b75794b05e12290a6e98a80b5bd02`  
		Last Modified: Wed, 16 Jul 2025 08:57:44 GMT  
		Size: 22.4 KB (22381 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.21` - linux; arm variant v7

```console
$ docker pull ruby@sha256:6e9558c885d45976f001f440bac33cc7eec113b1fb54292a6faae2d5b7db17ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37803368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034a77ead72e7959206f1b42ed9dd900f450fa950cb3e57af12dbb81c1731b8c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV LANG=C.UTF-8
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_VERSION=3.4.5
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a96f521d793eec1dcb2b825985eb01c309edb500ebd753a2f84cb9430f05802f`  
		Last Modified: Tue, 15 Jul 2025 18:59:46 GMT  
		Size: 3.1 MB (3096871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770f1267e885ebdd245469ced631a975128a2c04584309a18a73b137ebc67293`  
		Last Modified: Wed, 16 Jul 2025 03:21:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff73924c8850802027da4ff19222101270e6674e78c2c8a49c670a680883d60b`  
		Last Modified: Wed, 16 Jul 2025 06:56:48 GMT  
		Size: 34.7 MB (34706169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e7062b476c093598e3452d168011c07c92723f19e9bf4b34c5284daeb5ec01`  
		Last Modified: Wed, 16 Jul 2025 06:56:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.21` - unknown; unknown

```console
$ docker pull ruby@sha256:f036601bb05d772a5a00835b082899ad07c33465a76bef4111f588fff82427d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 KB (228690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1854074f3fd03e3ae6151df0bacb51a766f95c5388fada5f847e26d2f03c1677`

```dockerfile
```

-	Layers:
	-	`sha256:730c948c1c9a2b890e08f917ac3473360e7d3c73f9d8f955d5af38f153e18281`  
		Last Modified: Wed, 16 Jul 2025 08:57:47 GMT  
		Size: 206.1 KB (206094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86c8afbf9a5955fcd31c73e7f15a2c0d7bc2b897e0e0c94ab59e99095b02b4c`  
		Last Modified: Wed, 16 Jul 2025 08:57:47 GMT  
		Size: 22.6 KB (22596 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:f62ec177caae17818fed27a783d7c7b238f8c9de90638940d0b5d3ae84d169ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43048784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a6b80fab394e25d91e42b80b7c94f83f1ca1b34daa22b4a91e70fcbe1295fa`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV LANG=C.UTF-8
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_VERSION=3.4.5
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10d4dac5f9ebd2c1c068878484d17a40ef8f76f0e093e40d9f6146bae31701f`  
		Last Modified: Wed, 16 Jul 2025 05:34:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b78294880d4853bed967087fb20b7c8e35f86ca0598b26c3e4c8e5ace2b650`  
		Last Modified: Wed, 16 Jul 2025 08:56:04 GMT  
		Size: 39.1 MB (39061519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1c338e8928b1d3bdf7dbce68b748bcd63e9ba895615879aa2ce719ac234962`  
		Last Modified: Wed, 16 Jul 2025 08:56:00 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.21` - unknown; unknown

```console
$ docker pull ruby@sha256:3e9e3ee80c14fb72fd7dfad832e34999308b003143a1ebba6c95dbdf933f8183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 KB (228741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede769f63662e184ddf861ecaa9fd255845d3814a7bd7d7503a717e0a6afbd01`

```dockerfile
```

-	Layers:
	-	`sha256:d862bdbd359393478639d18f9db2143035170cc07cf4386ec0554e9bd4181362`  
		Last Modified: Wed, 16 Jul 2025 11:57:38 GMT  
		Size: 206.1 KB (206114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c55877448496c3ad9423db417ca2c525171ec152a9e6b7de91806ce88e031314`  
		Last Modified: Wed, 16 Jul 2025 11:57:38 GMT  
		Size: 22.6 KB (22627 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.21` - linux; 386

```console
$ docker pull ruby@sha256:b396345d706ea7fe68ca3baa666c09561e9a0b999a078fc89dfca3b079d80598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38204014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd0c13820a0d0ac78d19082b87cf2af898fe21f0742dccadf365a309112b3b3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV LANG=C.UTF-8
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_VERSION=3.4.5
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:47ad0adcb4aa253584437783c542bfbd2276c07a7a0b7487bb26f9b2e80cba73`  
		Last Modified: Tue, 15 Jul 2025 19:04:30 GMT  
		Size: 3.5 MB (3460726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d17085fbcdd4ac9aa47859b3dd72e02b4f1954bf4866818192e62eeb8d8672`  
		Last Modified: Tue, 15 Jul 2025 20:25:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7152d614b175db138eb92f236216af2372eb961ae304a03683b1585d8397c73`  
		Last Modified: Tue, 15 Jul 2025 20:25:21 GMT  
		Size: 34.7 MB (34742960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f267648557b0f73552bfce1fd4565fa0987f32abffc013e4a021a04973057dc3`  
		Last Modified: Tue, 15 Jul 2025 20:25:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.21` - unknown; unknown

```console
$ docker pull ruby@sha256:89ffa583fdca8246b682b00be58079cbfdd603f8a5b1ac829db60e5a4eafeab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 KB (225501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e437c569ba9b55be5c103e2414f3b6ae56f99c44891e2d163553367b10670495`

```dockerfile
```

-	Layers:
	-	`sha256:011b0634df07a43d65af059c3351a822313f39c3b14bdc1ec382b0e593af1ffc`  
		Last Modified: Tue, 15 Jul 2025 20:57:54 GMT  
		Size: 203.0 KB (203043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41516e3fd563781da28becf9e5720dd84a8bffe3a7ce9ef5d09ba7bd12d7e2a8`  
		Last Modified: Tue, 15 Jul 2025 20:57:55 GMT  
		Size: 22.5 KB (22458 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.21` - linux; ppc64le

```console
$ docker pull ruby@sha256:6f07478bfb32b744f5988ff80e478ddff224ba06cd2e6f77ae1105abce0cbe79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.0 MB (39965545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41d672166a882fbc9c2d57ee7fcfb32a3fdafce65cfe121c3172f9992073ec5`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV LANG=C.UTF-8
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_VERSION=3.4.5
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:bf93837577694839723892fa29fd11013552ac59944071e2341ac6d6d9876d29`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.6 MB (3569125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f46416c566ecc9d89cb5bee95fc09aa21f865554af8f4134eb062779a2f237`  
		Last Modified: Wed, 16 Jul 2025 00:59:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e86a0c452e33ef7d1e4e8e308105d2eb68720f4dc0328c5a85f6b4eb201e6d6`  
		Last Modified: Wed, 16 Jul 2025 10:06:17 GMT  
		Size: 36.4 MB (36396092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a91771e741135f43378020e30d497b1edf0fd63bd293ea950454217a8d8414`  
		Last Modified: Wed, 16 Jul 2025 06:10:15 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.21` - unknown; unknown

```console
$ docker pull ruby@sha256:baa262ee608ed9d459c452a7c7d487b3733465165992835a4913332e0ae2b443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 KB (223692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df732099808ddb7271b5ae3155f59a1917972a13c5124fc459f5079424f8cee`

```dockerfile
```

-	Layers:
	-	`sha256:62d5510f702aa4ecc593ba8d2c1df0d4dfba5a4da7829fe49cda779078a9d3e4`  
		Last Modified: Wed, 16 Jul 2025 05:57:41 GMT  
		Size: 201.2 KB (201151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea0982c387b773a3a5882451847dd21e2fcb730609cfa3a020e5ad33d0a40dc2`  
		Last Modified: Wed, 16 Jul 2025 05:57:42 GMT  
		Size: 22.5 KB (22541 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.21` - linux; riscv64

```console
$ docker pull ruby@sha256:5ff333cc6d83b57bdc87b0f727d0aa2e3e1216a0c88d9406964dd6bea601fe5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38175670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a8b2bbfa0a6f50ad43ab004341f5f186b44be6482f9be179b43a81e6e52e630`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV LANG=C.UTF-8
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_VERSION=3.4.5
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c4be3fb7c48ca84ee50be475d7d4a527212bb75b64469ee7eb6e6f0a98941f`  
		Last Modified: Fri, 18 Jul 2025 03:36:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87f2f72b85f4b1f84f401ec1eb73b412a9b35e8e40978f4ad024f26454ef23a`  
		Last Modified: Sat, 19 Jul 2025 04:44:18 GMT  
		Size: 34.8 MB (34826252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521e7aa8aaa73f8c8864ad24345a546d06bb5b0efa09850c3edf85aa658095f2`  
		Last Modified: Sat, 19 Jul 2025 04:44:14 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.21` - unknown; unknown

```console
$ docker pull ruby@sha256:35c1a101bfc0efae17aa4f17d72c3fd4f0b529d7849b9f2182aba452b43eacc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 KB (223689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24631793e090925de7f4f31c98575ef1510abaa00cc2d058b9ca51c5a48e0b2c`

```dockerfile
```

-	Layers:
	-	`sha256:4e0c902f5e8f1b9287b0b5b63bbf30dab51aa24a1144752eca72f680d3441329`  
		Last Modified: Sat, 19 Jul 2025 05:57:49 GMT  
		Size: 201.1 KB (201147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:478c998db7930b37f3eea8ea2b48f54aef2dc3f0163de6353e58430967608c66`  
		Last Modified: Sat, 19 Jul 2025 05:57:50 GMT  
		Size: 22.5 KB (22542 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-alpine3.21` - linux; s390x

```console
$ docker pull ruby@sha256:b8c6ef3f7900cc53eede3c04ee2e32215f34cf5f121ead1068ac73408309d070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39636579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833cfd377e090ac29b098c89d5c93b35aafb8930d60626fc89287f6a58277862`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV LANG=C.UTF-8
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_VERSION=3.4.5
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Tue, 15 Jul 2025 17:53:49 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 15 Jul 2025 17:53:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Jul 2025 17:53:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 15 Jul 2025 17:53:49 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:40ef870b733fb35d27e79770e3e1133cc7c54e14d8c251e61ecccdec69c20e32`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.5 MB (3462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f70e23950b298583307250026bf211e6e69f1f04bf424c27ce5cf1cd1fad65`  
		Last Modified: Wed, 16 Jul 2025 04:44:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb6e17e601f031cafa9a97074f0982bda522a7bcf90f7eedc98b7649a0000eb`  
		Last Modified: Wed, 16 Jul 2025 08:08:33 GMT  
		Size: 36.2 MB (36174151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09d4dfa9e67e818dabfea755252c393384801c677b992948474fc50587344bd`  
		Last Modified: Wed, 16 Jul 2025 08:08:28 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-alpine3.21` - unknown; unknown

```console
$ docker pull ruby@sha256:69f7c84893b6b4e706ea016a91e1006f276e284069270ed1d7e0601f1f5a752a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 KB (223611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9e2918e046930a6fa972ad80e128924e46b4c6bfc5199b1a3d0f23fb5c3385`

```dockerfile
```

-	Layers:
	-	`sha256:84d6716bb9a5a601fe04f6dac3207cc478e216178eb7b44ef88b9697b9a250ef`  
		Last Modified: Wed, 16 Jul 2025 11:57:48 GMT  
		Size: 201.1 KB (201117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7991aee9b37e2772804d2016f8659b5e47e82b32b678c550c9c1ac3eb151049`  
		Last Modified: Wed, 16 Jul 2025 11:57:48 GMT  
		Size: 22.5 KB (22494 bytes)  
		MIME: application/vnd.in-toto+json
