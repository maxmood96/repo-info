## `ruby:alpine`

```console
$ docker pull ruby@sha256:b4c321a99b9f21b7bb24f22e558bf1477630fb55d692aba4e25b2fe5deb7eaf1
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
$ docker pull ruby@sha256:d1a1669b4cbef147088d1cd12463ece81586b3f53bcc1fa3f8a8b8d24e809cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47487281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfe36b50f2da9336056c356b327eec82f7abd9c1aefd578818c3d1630e3a7e9`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV LANG=C.UTF-8
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_VERSION=3.3.5
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5fb57ad4800f9b7aa213c24a541ebe0d817ee1c58b2c86a5824395e9f9dc4d`  
		Last Modified: Wed, 30 Oct 2024 18:06:32 GMT  
		Size: 6.7 MB (6684098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3ebbe33a58898f37c8b6a824df2c1563dc89e323fea2d68df62d5e3c0cdbf9`  
		Last Modified: Wed, 30 Oct 2024 18:06:32 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c29f70f107e5da88c01ebd08146a2f9c5d8f8b51324033cf92ba707db1794a0`  
		Last Modified: Wed, 30 Oct 2024 18:06:32 GMT  
		Size: 37.2 MB (37179040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7635daad87857a158991f8aad80f7abc486fefce4f9354016c00d15fab6a3b4`  
		Last Modified: Wed, 30 Oct 2024 18:06:32 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:11dbcf34f8c769b44ac2427454ac82bfaf6da155c9ad11295d346ceaeac509e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.1 KB (991147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4a9207f867232b8ec572ff155e86e90b9476bc33f5fa14e407be0d442a60f1`

```dockerfile
```

-	Layers:
	-	`sha256:a9be5bc4ab250ed13c41ab785a3721bda24daa9dfba2705b803505227a0303c7`  
		Last Modified: Wed, 30 Oct 2024 18:06:32 GMT  
		Size: 964.6 KB (964559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85cefd260623f4c49db8929e8a4bce47fd40e43466d1d857f40046047a7c3683`  
		Last Modified: Wed, 30 Oct 2024 18:06:32 GMT  
		Size: 26.6 KB (26588 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; arm variant v6

```console
$ docker pull ruby@sha256:7df1f1a092cdbf954816456a5c0f17b3fcb338218474b4f7d9caa47437e701d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43542391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa3e14317cf7f7bcff4a9a669efe429c1d3dd0888b0b1416021c6ec2cb69fab`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV LANG=C.UTF-8
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_VERSION=3.3.5
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7482308aeaf448ab510de66c0f7083c3f9f720a77f12ff2547be8a7fe4e277f0`  
		Last Modified: Sat, 07 Sep 2024 12:23:17 GMT  
		Size: 6.5 MB (6531246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac1582ea2b0d99bb913a6f07f9302b8130cf8a529fe6628b8ffd2cc37a19ee4`  
		Last Modified: Sat, 07 Sep 2024 12:23:16 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ad57d3a385823769fcef123dc881ed4bfb616381dd87818188ac5de262e97`  
		Last Modified: Wed, 30 Oct 2024 18:15:57 GMT  
		Size: 33.6 MB (33644302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4163d1e03fd11a2475b5712a9dfe61ce764b1df6098acd2fbbf4c5f147e20dbf`  
		Last Modified: Wed, 30 Oct 2024 18:15:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:51907b89b869de87c5e34a5021ce3efeb8b459cb46f100829867e6104f6ddff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc022e31cc936f6d8fc23c45698f60e4d6380c3d218e2e1c3452ffe5204124be`

```dockerfile
```

-	Layers:
	-	`sha256:bdae1be2214fdfe83a8befe69397fc1a89d87e9bb91d6c30b5ceccb0461b9f0f`  
		Last Modified: Wed, 30 Oct 2024 18:15:55 GMT  
		Size: 26.5 KB (26514 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; arm variant v7

```console
$ docker pull ruby@sha256:8adbe965b1a650e64f1e896a11f681227f0cb84ed5c936b7deef11bc12183972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42633861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706329867a8e583a0432339eeeb5ad0f7342f32106c0ac85a873b9ac1fa80d4d`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV LANG=C.UTF-8
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_VERSION=3.3.5
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d144a0b15b16a5460d2785d5992999e8460241448fbfbaab6e80402384bd6ddd`  
		Last Modified: Wed, 30 Oct 2024 18:43:37 GMT  
		Size: 6.4 MB (6375856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd32429e7ee45fcd9be91e5600c4298cb53c5c6e7e8896af54b2becf86bf65da`  
		Last Modified: Wed, 30 Oct 2024 18:43:36 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a302e3e6ec55deaf70005a67ed2f658cae5286aa0a50072e638ae441adf47dcd`  
		Last Modified: Wed, 30 Oct 2024 19:00:13 GMT  
		Size: 33.2 MB (33162168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627b4e9461f846ed99db70f7a86ac1809dd5e98e67cdd34fd4fa24e83998e886`  
		Last Modified: Wed, 30 Oct 2024 19:00:12 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:2860c9f77915263799f144003a1c87c8839426fdf4ff96830d17c6f4958479b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.0 KB (972995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369fd61e8ce00ad8ad72c27ae337e3bd0ab9b0d88b854582e53d4b812475b8b2`

```dockerfile
```

-	Layers:
	-	`sha256:857c188e63fd91adfe65108dd58fb5a2d362e13dd0e85f1f834765509fcf9bfc`  
		Last Modified: Wed, 30 Oct 2024 19:00:12 GMT  
		Size: 946.3 KB (946266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3747cc38f4bd2c59be98dbd7359de1157a42486279fd4982ac9187b5c3a2d3fd`  
		Last Modified: Wed, 30 Oct 2024 19:00:12 GMT  
		Size: 26.7 KB (26729 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:bfe01a002c7e07196fb77002764e242c7520f45452d86af6d589f87f88bcd6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45975222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78475f17faba3377d4e83e84fa5facfd213411e1398ce7e135fef7173f554f4`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79810d6b1dd426f9b344ea48580c130cffee420e2a54469effac9c8a83319af9`  
		Last Modified: Sat, 07 Sep 2024 11:38:07 GMT  
		Size: 6.8 MB (6750624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a01e81a3971e892954da181ff54aa648711d9c768bedf6741eab3e023df1c6`  
		Last Modified: Sat, 07 Sep 2024 11:38:07 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2e659c57c38b752dd8ffd7064672319fc3d6fe4ff7355cdfa66818f53c5ffe`  
		Last Modified: Sat, 07 Sep 2024 11:43:25 GMT  
		Size: 35.1 MB (35136620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ce8633db9027d32516f36e6a25b56b3e96bf9c610f1a799b8d7c80685e1d1`  
		Last Modified: Sat, 07 Sep 2024 11:43:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:05bef9abd5f6395da480a0d1d901a237f53232ff96bada53571dfe9efd25fac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **965.0 KB (964985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de04c95e68ff076581b31479733d668b62946c239dab387ebcbe412e2cb8b66`

```dockerfile
```

-	Layers:
	-	`sha256:61e3a08f13eb042c2bce6bfbf4a376c9f41ebf6039383be0b14d0898bd761f23`  
		Last Modified: Sat, 07 Sep 2024 11:43:23 GMT  
		Size: 938.1 KB (938083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b81062832c45fe06be6d2ea3765bfa3aca67675a9293aec7efde740db40c12`  
		Last Modified: Sat, 07 Sep 2024 11:43:23 GMT  
		Size: 26.9 KB (26902 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; 386

```console
$ docker pull ruby@sha256:486fc5999e94605b4f176c27109177c6da20e2437fa2b3077cb4b5e9eebf600e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43746566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da380ac12f97ad7b60244f50f33796e26bf7fc6483da66270c410ff8c0a8f379`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV LANG=C.UTF-8
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_VERSION=3.3.5
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d3afc1835d974f14dabf60e917109b43b9dbf0ecd2d2fb6c225b89e78344219`  
		Last Modified: Wed, 30 Oct 2024 18:10:06 GMT  
		Size: 6.7 MB (6749339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65826fd9e04761883d01465161972b6aa941cfd945aea9923687e9dd90236ddb`  
		Last Modified: Wed, 30 Oct 2024 18:10:05 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657a520738465262ad35b76da911f5ab41a8c2f76da9db830a560354a3e11c3`  
		Last Modified: Wed, 30 Oct 2024 18:10:06 GMT  
		Size: 33.5 MB (33527727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e249dffea7085b13b105543ec99147bbcb0682133025375d00159c7c323cf8b`  
		Last Modified: Wed, 30 Oct 2024 18:10:05 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:80d3aab26056c995f1716466f654fdfd5d32b2fce196452952d75c917c404642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.0 KB (991047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dd7e5e9945689a34c1fbfb29a454af8bac250bf95c384a88553e3dc2ef4f2f`

```dockerfile
```

-	Layers:
	-	`sha256:2fdc7f8ac5dd5fbc8552dd842f70dc353eb9b27e99c35632ed9bead36bb827f3`  
		Last Modified: Wed, 30 Oct 2024 18:10:06 GMT  
		Size: 964.5 KB (964514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d3a8f0c84078a60e2d8270d7c19c71d73934db5c06a7e6c1d6aa12961a019bb`  
		Last Modified: Wed, 30 Oct 2024 18:10:05 GMT  
		Size: 26.5 KB (26533 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; ppc64le

```console
$ docker pull ruby@sha256:f7751287976bf1397c5a127f1861f805ad45c0ae0d64160f619603d05a220e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45479560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb8b121a8d5132568bcd05cebd23fe681e25f9459e9368303394f6955aef76e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV LANG=C.UTF-8
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_VERSION=3.3.5
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32e4b3847e4b4db773ca759fee0fb64b5e18585fc43614f20d1a96ebe122c60`  
		Last Modified: Wed, 30 Oct 2024 18:32:55 GMT  
		Size: 6.9 MB (6911683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327d4fcf0c23e80b9c71ceaaff7941a53660d062094f3525284445b2a64efa9a`  
		Last Modified: Wed, 30 Oct 2024 18:32:54 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e82081b8d138639331456be5a08d6ff8089020e14a84e559a369eb8ad346df`  
		Last Modified: Wed, 30 Oct 2024 18:45:41 GMT  
		Size: 35.0 MB (34995121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070abd9c70ec09e3c3617eb64dbd4ab4bb3a81671c3c8c40489b00003f386b7e`  
		Last Modified: Wed, 30 Oct 2024 18:45:39 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:b0bfd2c984dab6173c6808cdb22e2da43a6d3bf60871eef6cd35a2c17a567668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.1 KB (980124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb9e72a61557d831b10a025f36c830b43318f667d7a93810c21f8ad2370b46f`

```dockerfile
```

-	Layers:
	-	`sha256:6c4dfee83d86297ef3efd269bd8c54edadfd2c5946e1706dc8e80b9ff3ca7f81`  
		Last Modified: Wed, 30 Oct 2024 18:45:39 GMT  
		Size: 953.5 KB (953469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32eb04a68dd35fe080240e22e535c0e9b4e61430379e3668224103d21005883`  
		Last Modified: Wed, 30 Oct 2024 18:45:39 GMT  
		Size: 26.7 KB (26655 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; riscv64

```console
$ docker pull ruby@sha256:5b35c0daa7eadd547de3d1e74066bcc1e1f90f3f0a6e7a8ecdefeb4663fb9e2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43747614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:960eead5ccd92bb92cf9f286b4a1e687ef8eae77e4db1bd26d3bf2c9ab3f16b6`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV LANG=C.UTF-8
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_VERSION=3.3.5
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f415934773bb3279d1e59447161213866d8d558ab1e46978460c059379f097da`  
		Last Modified: Sun, 08 Sep 2024 13:24:14 GMT  
		Size: 6.9 MB (6946838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d825ee7f9e2e2c32f71c97db0bf40f10edca4983062295c5bac56c1e34fbe2f2`  
		Last Modified: Sun, 08 Sep 2024 13:24:13 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc08704e7164b32089e9722d2f88fbcf616712bc8648028891220653c688d23`  
		Last Modified: Wed, 30 Oct 2024 21:32:19 GMT  
		Size: 33.4 MB (33428987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97b4ca0773bea5f9ceb772c8a8539712a223007cf8fbba93eaf3708fac2b748`  
		Last Modified: Wed, 30 Oct 2024 21:32:15 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:381a16b337e3ff57ae87e67de4cf698ac8fb13dc22d6f140b1029e1b85b5c00f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **971.5 KB (971545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9026c43fd974e209f047e237594d9562fb70c8e35a8972d281e944f6a6954f`

```dockerfile
```

-	Layers:
	-	`sha256:b3a11e1a9732cac0125aabfce9121d484be62edbd9094c2707ef06c144fa7f25`  
		Last Modified: Wed, 30 Oct 2024 21:32:15 GMT  
		Size: 944.9 KB (944889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:261ffcda777a00c2326a6904ff1efbf2b76843a84c0a66cada97e8161b6a1cb8`  
		Last Modified: Wed, 30 Oct 2024 21:32:14 GMT  
		Size: 26.7 KB (26656 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine` - linux; s390x

```console
$ docker pull ruby@sha256:6a0a636eabb569980dd7568dd0e7d70b7539d6bbf158488b081c7a090f55db1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45257000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fd4042beb7e0b3d3f217b149eab5b8d9008ee98f25d9529c690db64478f506`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV LANG=C.UTF-8
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_VERSION=3.3.5
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Mon, 28 Oct 2024 11:48:50 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='1455d1df3825c5f24ba06d9dd1c7052908272a2cae9aa749ea49d67acbe22b47' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='7087ada906cd27a00c8e0323401a46804a03a742bd07811da6dead016617cc64' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.82.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 28 Oct 2024 11:48:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Oct 2024 11:48:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 28 Oct 2024 11:48:50 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aace386700f7519dbe51639ba130b690fd2486da9b9222e5a560c73c7b6ee14`  
		Last Modified: Wed, 30 Oct 2024 18:40:54 GMT  
		Size: 7.1 MB (7061703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190d308936c031782fff1ed3f91769f04fd94a40dd3f441189355cabc7611a9a`  
		Last Modified: Wed, 30 Oct 2024 18:40:54 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7267b4ff66362d5d8cc446065c9d691e21887e0b14724fd3cd25f9daa4834715`  
		Last Modified: Wed, 30 Oct 2024 19:00:00 GMT  
		Size: 34.7 MB (34733365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c7b336b88f3af3174ae1a0c2f22b08e3263f34537ee684f31ab1a553f0c8e0`  
		Last Modified: Wed, 30 Oct 2024 19:00:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine` - unknown; unknown

```console
$ docker pull ruby@sha256:17b330789c8cba34e6814f3503bb8f518a1ba99dcb713a0804b2b739095601c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 KB (987939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae589d7bb5d11512b737175abfb6e9943461ca455a21f71e4f37f76fa2a0b33`

```dockerfile
```

-	Layers:
	-	`sha256:5bf90c92bb1fe00f967b463bcfc716732372d9d3492ee460606170c096728168`  
		Last Modified: Wed, 30 Oct 2024 18:59:59 GMT  
		Size: 961.4 KB (961352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c964c2d3a8b78fb471e9f52de96baed9e9ff59cb2566da3568d2fbfdd95f833`  
		Last Modified: Wed, 30 Oct 2024 18:59:59 GMT  
		Size: 26.6 KB (26587 bytes)  
		MIME: application/vnd.in-toto+json
