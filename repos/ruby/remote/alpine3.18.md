## `ruby:alpine3.18`

```console
$ docker pull ruby@sha256:5d32a73b25aaef6f9a2862a58e8b27dd9d14f60e1d0664a3246ea55ca0903f83
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

### `ruby:alpine3.18` - linux; amd64

```console
$ docker pull ruby@sha256:16def2d10a7a033a52e2600678cea8632d37f9198cd18815ec7850f5110d5d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41207230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf01e802a663e6254f76f9e9048217088225bf299255ba2974d9c877015e565`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddfda8d2cb43acf60deb991085dea74bc61c37b4534a02bb79729e2d67da799`  
		Last Modified: Fri, 15 Mar 2024 23:58:38 GMT  
		Size: 4.1 MB (4131286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f432ef9c016345f1de08e1990841fd80a7de13639914ffe2b90cff0b1aaeef5`  
		Last Modified: Fri, 15 Mar 2024 23:58:16 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d540301983d71539d355fd68067e619078eb75a12e377637ce931b0afe7d7b2d`  
		Last Modified: Fri, 15 Mar 2024 23:58:38 GMT  
		Size: 33.7 MB (33673067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ae9f544ba5d5c3e099cd0c8f2a36fbb09b8f192e95620723c60c1d6dcac6f5`  
		Last Modified: Fri, 15 Mar 2024 23:58:37 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.18` - unknown; unknown

```console
$ docker pull ruby@sha256:2c23909bdac177f839392db1e61e10981cf51e7a60aa6d14da38f7136e92d068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.5 KB (987478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9baba39e66cdde1dd9d973e362e805aac36a7b9b351cb708bccb13bc0050764`

```dockerfile
```

-	Layers:
	-	`sha256:85f326b79d92d8d51861bc8206cc06950d0c5d7ca2041790c3f9c2cd0c056a9d`  
		Last Modified: Fri, 15 Mar 2024 23:58:38 GMT  
		Size: 960.9 KB (960872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc681b6227d232a93d7f169582ff74c42b691639d037889a511d12d77447fb54`  
		Last Modified: Fri, 15 Mar 2024 23:58:37 GMT  
		Size: 26.6 KB (26606 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.18` - linux; arm variant v6

```console
$ docker pull ruby@sha256:d1b82eefc8c09638a90c1180f48b4dc815d29a6fc7aaa594778e2759a121a5b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (38982096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0dfee923306ada1eef16bd687e764045b8beb2e5fdd6c381a235e504642c95`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.3.1
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0686941a3ec395a15ae2a852487b2a88e5fb8a5518e188df00d8d1bb71a6349b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f552652f091dfe0a928791eb6f50f81ec123ad9891af681575e3be4a2042d11c`  
		Last Modified: Tue, 23 Apr 2024 17:00:18 GMT  
		Size: 3.8 MB (3816403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fda9f81cf6aa6ffbc83f8a78a90e50b455b3969d586acd3584d36beee27a7b6`  
		Last Modified: Tue, 23 Apr 2024 17:00:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4598c7216255aa8b1fedc46d527661b2bb6831980ee70b669c7ced105d337d94`  
		Last Modified: Tue, 23 Apr 2024 17:00:19 GMT  
		Size: 32.0 MB (32018297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe6e18535dabbb61e22ebfcebed99fa48f536e11fe935c266af24c9867450dc`  
		Last Modified: Tue, 23 Apr 2024 17:00:18 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.18` - unknown; unknown

```console
$ docker pull ruby@sha256:34ec984acc59ff4aafde8ece89dbe059671f22233ea12f1256b4fe6347eee152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9bf625695ae18ce415a787f85765a6d020fdc8b8d4be986c25ca0a19ae7e4e`

```dockerfile
```

-	Layers:
	-	`sha256:5b178f1daf75c962f8537364b8000ea48f00d7f19e35c5b15c6e58f4d370ed08`  
		Last Modified: Tue, 23 Apr 2024 17:00:18 GMT  
		Size: 25.2 KB (25240 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.18` - linux; arm variant v7

```console
$ docker pull ruby@sha256:f1a82a98985c555c38f2a8e1c6633c16b4a68fad8d35c5ab72e437b4fca222a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 MB (36563863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb3204b226e162e7943d1bb22cfe7342726d8326d17facb927ed78382d282ef`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0024e184ce899205e2450f8f2b33be31d0264636f395ec416b756755089189d3`  
		Last Modified: Sat, 16 Mar 2024 18:03:00 GMT  
		Size: 3.7 MB (3717087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114d2ff0bc9c4fcf8807846cd7cdeeb2c3a3ed5d647d6e1e9c6b3afa13c0d033`  
		Last Modified: Sat, 16 Mar 2024 18:02:59 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c89cb6a9147d47cc69ac8c7c9be760e4d22361a3f057032a349d6785faff77c`  
		Last Modified: Sat, 16 Mar 2024 18:03:01 GMT  
		Size: 29.9 MB (29945049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879b76c97932420e381132a09fa5977fcc92f2889f0df7dc0845809ff64fa20b`  
		Last Modified: Sat, 16 Mar 2024 18:03:00 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.18` - unknown; unknown

```console
$ docker pull ruby@sha256:86695cd616bc4f43d4df9a53fcb9d4440ed4ebfa4495538e07394af7e48f97df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **969.1 KB (969095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a657694613376ccf42e85cbae54d8e7529c209bde762aabea4595af6ad1e8677`

```dockerfile
```

-	Layers:
	-	`sha256:514344743e832e07f0dd0b47801921603dbce8e67364d82ad0a95a6a463cf7d8`  
		Last Modified: Sat, 16 Mar 2024 18:03:00 GMT  
		Size: 942.5 KB (942547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fb1b7f1348f43be5d3a407b4efe020e7d8694bc475eaaf3ac5f768f5bed463f`  
		Last Modified: Sat, 16 Mar 2024 18:02:59 GMT  
		Size: 26.5 KB (26548 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:838650aabe75f737b99d9f50c9a858e3161a938251d472b39ea85ec03eecbed0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41053187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6daaf53808c134a506b6dd620279db968cfc7b440e7390b8b1bf38d84561d5c`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d002cb486864f216503b0e91a5fbfa1d4bff221bedad1208479f784d068c0ca6`  
		Last Modified: Sat, 16 Mar 2024 17:00:31 GMT  
		Size: 4.1 MB (4061386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73f9a3c5db2eccc0dbf307416289b5d4fa59b45ae3ae604086cb3c854fecba`  
		Last Modified: Sat, 16 Mar 2024 17:00:31 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1353a69975740ba3c54cb203df31664d440448328f6eb452bc4aedaf5d9a4945`  
		Last Modified: Sat, 16 Mar 2024 17:00:32 GMT  
		Size: 33.7 MB (33658108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9e90076e020845f768fe0611c15ae29a706d2c5aed589227ed7981c38c6513`  
		Last Modified: Sat, 16 Mar 2024 17:00:31 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.18` - unknown; unknown

```console
$ docker pull ruby@sha256:3ea7fa48636b7c49b1e071c365a2699a37296e23c02aa3829cf6f302c50bc081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **970.2 KB (970186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0f3b8399298f6ebe8e9a1e1842dff3b1e6b16918cb97cd2ddb8e12fce5bcec`

```dockerfile
```

-	Layers:
	-	`sha256:ed8b896f63a54e7af2e4566ae75d2aa125d602dcb8399fd06a9ca51b2c372d11`  
		Last Modified: Sat, 16 Mar 2024 17:00:31 GMT  
		Size: 943.7 KB (943737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d349e606cc75cdce275013629116e05b46324f75b5b58d45fa970e04d7bd2b`  
		Last Modified: Sat, 16 Mar 2024 17:00:31 GMT  
		Size: 26.4 KB (26449 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.18` - linux; 386

```console
$ docker pull ruby@sha256:fd580ce344493047d4559fa0309007be35fcc72d2755fee1216e272c39c12e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39363167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf3bf29265ccdd3703839162a1a451887799e0197313c565d350f27d5b78d8c`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.3.1
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0686941a3ec395a15ae2a852487b2a88e5fb8a5518e188df00d8d1bb71a6349b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f978c0f262134bfc99d0411c2a0dbcdf4b2d7f80a2d162979bd49e9a50ba375`  
		Last Modified: Tue, 23 Apr 2024 16:55:16 GMT  
		Size: 4.1 MB (4147028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f9f33fbd7a75219dd0f3ded69dd4c2989eb8829757385e2d74f7967d6f639c`  
		Last Modified: Tue, 23 Apr 2024 16:55:15 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17eb0ee80e06005e086a890deb12c2de5d05967b48477921ca2323e09744af6e`  
		Last Modified: Tue, 23 Apr 2024 16:55:17 GMT  
		Size: 32.0 MB (31976736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1caf1672c113c15175bb43c05e9f751d4bb091c63148406ea80de16d397f0f`  
		Last Modified: Tue, 23 Apr 2024 16:55:15 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.18` - unknown; unknown

```console
$ docker pull ruby@sha256:e744ecdd2c727cdba7e863009ce81cc60e251a8860572146cb9d24a40ce240c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **962.9 KB (962897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e46d89770c704103e5f5a5b13209a6ff612a47162daa0ac1bb464190f590ba`

```dockerfile
```

-	Layers:
	-	`sha256:c2bbec2bf8d138b47448f4fd0d6504dd30ccdf9f3c68ce1f8b40623345a20353`  
		Last Modified: Tue, 23 Apr 2024 16:55:16 GMT  
		Size: 937.6 KB (937583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3be2ee31549a4fdd4de7bcd82ab042df54c0b8aedf35888486ba0aba62887f5`  
		Last Modified: Tue, 23 Apr 2024 16:55:15 GMT  
		Size: 25.3 KB (25314 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.18` - linux; ppc64le

```console
$ docker pull ruby@sha256:1396966f64436e18a12afb8aca2f1886f945384fe07bf90fedbed7cc32cdba79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39017087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551f1ab2a8949b034dfd84d1d725c696c11a7c97e15fcf90ff095adde3c62b6b`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c6ec9fb504c07d1c16c1b449d00bcc19cc9559e9f63e741d265c315636bea`  
		Last Modified: Sat, 16 Mar 2024 11:45:41 GMT  
		Size: 4.3 MB (4279192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f03c40289ce1a749a54c1b09ca1e696aa84b538250c4fe7a36474bb3e3ea06`  
		Last Modified: Sat, 16 Mar 2024 11:45:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93123cd8b4793ab3e85728edce38c2b80c91f088b90d135baafec99ddbcdd474`  
		Last Modified: Sat, 16 Mar 2024 11:45:42 GMT  
		Size: 31.4 MB (31389070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed1aab6cbff6a384be7870976a0f7a0e87e7cfcd34fba14e108c9ad55505f32`  
		Last Modified: Sat, 16 Mar 2024 11:45:41 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.18` - unknown; unknown

```console
$ docker pull ruby@sha256:4f1057081bc5f9704b38ce865fe16d79563db2df691a83ede2b08e047cf5772f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **976.2 KB (976242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7dfae95053c823bd8cf88c61f27e9e2cd46d7e0237b2c98f7a9c93da17e9a2a`

```dockerfile
```

-	Layers:
	-	`sha256:fe54b84491673017592f67e80a9604e39d35898ab5d11726d542be55001056fc`  
		Last Modified: Sat, 16 Mar 2024 11:45:41 GMT  
		Size: 949.8 KB (949758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8585ed2b7e36643bd4acd59f8b58c4321b1ee03802e46eca724e1f37a64eeece`  
		Last Modified: Sat, 16 Mar 2024 11:45:41 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.18` - linux; s390x

```console
$ docker pull ruby@sha256:50b50cb996ca910a6f76f4fe62915515993ccbcdfc1afc3e6e2dbb94da3278ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38178558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07703cb0859c4ab5fc7c2acda279c2c1179777f7b9d321d70c08ccf03ae050c`
-	Default Command: `["irb"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	apk add --no-cache 		bzip2 		ca-certificates 		gmp-dev 		libffi-dev 		procps 		yaml-dev 		zlib-dev 	; # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV LANG=C.UTF-8
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_VERSION=3.3.0
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Thu, 29 Feb 2024 21:45:14 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Thu, 29 Feb 2024 21:45:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='7aa9e2a380a9958fc1fc426a3323209b2c86181c6816640979580f62ff7d48d4' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='b1962dfc18e1fd47d01341e6897cace67cddfabf547ef394e8883939bd6e002e' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		export ac_cv_func_isnan=yes ac_cv_func_isinf=yes; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-rundeps' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 29 Feb 2024 21:45:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Feb 2024 21:45:14 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 29 Feb 2024 21:45:14 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:905f468590b180ac946384c664e0231f84b310e2c181f704057a1a7e5773269e`  
		Last Modified: Sun, 17 Mar 2024 07:32:37 GMT  
		Size: 4.2 MB (4235217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8485725f7092ce368f351195ee735dbfc7e91f78899505986278d466a47ce5a1`  
		Last Modified: Sun, 17 Mar 2024 07:32:37 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606b69dabb89ebf400fd2752453ea53900194ca6931bd77972a5370db577393b`  
		Last Modified: Sun, 17 Mar 2024 07:32:38 GMT  
		Size: 30.7 MB (30725477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae118358c0cfd66340047230fb0f6d50f03b1af3a028f4ad9eaa6992618e9246`  
		Last Modified: Sun, 17 Mar 2024 07:32:38 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.18` - unknown; unknown

```console
$ docker pull ruby@sha256:61b5f50dfbcd58f6f2b3f05497cf5b215895e3ea98c3800eff32e27aad596272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.1 KB (984105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151954c6254dfd30695cabb184afd87a85ce5717b898dd087ddbda038b501a49`

```dockerfile
```

-	Layers:
	-	`sha256:ea84399e85096a9219780f02d47f387e7db271f675b8cda44a4f80af9016a6e6`  
		Last Modified: Sun, 17 Mar 2024 07:32:37 GMT  
		Size: 957.7 KB (957665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7af212d964c81fb459ad7057238a80dd80a6054bcb8d5bd4a075436d7dd34a5`  
		Last Modified: Sun, 17 Mar 2024 07:32:37 GMT  
		Size: 26.4 KB (26440 bytes)  
		MIME: application/vnd.in-toto+json
