## `ruby:alpine3.22`

```console
$ docker pull ruby@sha256:0d58abc079b0a41cfd426e82620f3c2d5f907fc46fab1815802cb79cdfb94095
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

### `ruby:alpine3.22` - linux; amd64

```console
$ docker pull ruby@sha256:92a022098cf2846be4f6deea583a18ebe548c203a0b0458a8211ca94ac230aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50106417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0384c35bed644fc74347dcfa36e0e6e5c0e65d2b5247987294ecca43078f361`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 17:34:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 21 Apr 2026 17:36:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 17:36:19 GMT
ENV RUBY_VERSION=4.0.3
# Tue, 21 Apr 2026 17:36:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Tue, 21 Apr 2026 17:36:19 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Tue, 21 Apr 2026 17:36:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 21 Apr 2026 17:36:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 21 Apr 2026 17:36:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 21 Apr 2026 17:36:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:36:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 21 Apr 2026 17:36:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bdae6396d1f0dc96d44ad382f5d27cecf2c49fb867972c723f90ff8b484890`  
		Last Modified: Tue, 21 Apr 2026 17:36:28 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bbe1a1a0144224cd9d11151f66213a86495e2e3e611aefa9b6fc9e51afe9c0`  
		Last Modified: Tue, 21 Apr 2026 17:36:29 GMT  
		Size: 46.3 MB (46297897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6434d9115f9efa14ee4e3324b46e74e0874ca1b78a31186667acd4a2510077b`  
		Last Modified: Tue, 21 Apr 2026 17:36:28 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:d46a32cef5c07f7854f9e99e83d8b7bc5bb018bf4c3b00589246bc2dac9be4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 KB (225420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9b98083538b578a8530c29c612610c2d24d50095bf286fb053b1c211d39d89`

```dockerfile
```

-	Layers:
	-	`sha256:6e8c5a0fd9f8aba4944d3cfa0858156b015183606e486c0cb6139040cc2c0282`  
		Last Modified: Tue, 21 Apr 2026 17:36:28 GMT  
		Size: 202.9 KB (202852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9404a6722bde1ae74df14808f1d1f8fd7c81a4b20e6a47cded3d9c20a2840e`  
		Last Modified: Tue, 21 Apr 2026 17:36:28 GMT  
		Size: 22.6 KB (22568 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.22` - linux; arm variant v6

```console
$ docker pull ruby@sha256:c6e356d2a9bb90a165fbcdaed8ade674b2673168a5678a93fb47afd131e0dd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42722768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2987057db206523882788cbdd69f14efa40b820730255527ff71c80a4b2a9dd8`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 17:29:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 21 Apr 2026 17:31:48 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 17:31:48 GMT
ENV RUBY_VERSION=4.0.3
# Tue, 21 Apr 2026 17:31:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Tue, 21 Apr 2026 17:31:48 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Tue, 21 Apr 2026 17:31:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 21 Apr 2026 17:31:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 21 Apr 2026 17:31:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 21 Apr 2026 17:31:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:31:48 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 21 Apr 2026 17:31:48 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a1b7e70841c1627617ebae7429734b2b5149046042c7f9de09fd19fd7083a5`  
		Last Modified: Tue, 21 Apr 2026 17:31:55 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a3d9f4bcf3275138a26ff1655c55cf2c3962f80bcf165eae389a3db7833227`  
		Last Modified: Tue, 21 Apr 2026 17:31:56 GMT  
		Size: 39.2 MB (39215054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc9c0187d42e239ddf9f17aa3ef23929290d133581dd851635ebd59e879e698`  
		Last Modified: Tue, 21 Apr 2026 17:31:55 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:abe7e824393d13f63070d1ce9054d9e931265eb24e17cb4dab44dfe7202073c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 KB (22459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3368917a66b1816fab84b5e400c035c8c9250b051218ac9e03f767a08e1ecf`

```dockerfile
```

-	Layers:
	-	`sha256:638da65bc030fadde1cd3ea31f5ea57579c7eb75323a5e366348fad40f463193`  
		Last Modified: Tue, 21 Apr 2026 17:31:54 GMT  
		Size: 22.5 KB (22459 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.22` - linux; arm variant v7

```console
$ docker pull ruby@sha256:f00e3152a146fc29923116cd1d6c8518afe3f294646efd298b84c37123d79b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42279095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b625780965b5c45adf9a5e6eee1205e47632b7081e56f9773352f044f84fd4c`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 17:31:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 21 Apr 2026 17:33:47 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 17:33:47 GMT
ENV RUBY_VERSION=4.0.3
# Tue, 21 Apr 2026 17:33:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Tue, 21 Apr 2026 17:33:47 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Tue, 21 Apr 2026 17:33:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 21 Apr 2026 17:33:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 21 Apr 2026 17:33:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 21 Apr 2026 17:33:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:33:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 21 Apr 2026 17:33:47 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc34ec86dd71f3e966bebef5bd7c6928a2167a3119bcd2cb72201c7f459c77b0`  
		Last Modified: Tue, 21 Apr 2026 17:33:54 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3c3f08a4441dc61cec67400221d062b90369f7e7da324a8645273446021cf`  
		Last Modified: Tue, 21 Apr 2026 17:33:56 GMT  
		Size: 39.1 MB (39052935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1860a14513804a0db0bb774311c8801c6ae381ecb40b97d2e24af69daa8f49`  
		Last Modified: Tue, 21 Apr 2026 17:33:55 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:8acce97d48b0323c291e70e1433896da0ad24f9a8fd7650825dda83d13f54a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 KB (225562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f835223af50e2206c25377e0367b12e51a531f620bfa6d89c91d2ce8d107cea`

```dockerfile
```

-	Layers:
	-	`sha256:66b7452bc3ba0e2a380a271ac7237715b6e399a38ecc755043513717ba6ae7a7`  
		Last Modified: Tue, 21 Apr 2026 17:33:54 GMT  
		Size: 202.9 KB (202888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:767023b012222d3dff4b05ae39e031de1858751a82c79b6467446d6b0a94ab31`  
		Last Modified: Tue, 21 Apr 2026 17:33:55 GMT  
		Size: 22.7 KB (22674 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:552fb84722c6831408677b07cdae35f4e37d20e3a3d57893e11749a798af9902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50251803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1e3db7fdf3a41bf8d6196a61ab6be12c163d25d0a891dcca155f8d37d482cc`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 17:35:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 21 Apr 2026 17:37:57 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 17:37:57 GMT
ENV RUBY_VERSION=4.0.3
# Tue, 21 Apr 2026 17:37:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Tue, 21 Apr 2026 17:37:57 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Tue, 21 Apr 2026 17:37:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 21 Apr 2026 17:37:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 21 Apr 2026 17:37:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 21 Apr 2026 17:37:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:37:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 21 Apr 2026 17:37:57 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cfb3f321c4263e5c879d4036439e9088e4dba444fbf74a0979290ffb37f885`  
		Last Modified: Tue, 21 Apr 2026 17:38:06 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd67026a1857d71f163ca99d27a101c3dd72873126635b38460c0dbc7b5d967a`  
		Last Modified: Tue, 21 Apr 2026 17:38:07 GMT  
		Size: 46.1 MB (46109578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eebacc7c22ad02b34a6c6b08172c384a6dd39783cea0ed16a281f226fb1876`  
		Last Modified: Tue, 21 Apr 2026 17:38:06 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:f7d494eb76c7dbdb7b835851ccb26ac5b87d8aa0826fa789e75fc5674bc0356b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 KB (225610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a36c16d32c30a44704fec03a016cc3380457b95524e727c97d29a14ca85231`

```dockerfile
```

-	Layers:
	-	`sha256:1a58fe122a2b0b682e45669d99346d665fd8640ad0a9bb55dc52809e0fe65c88`  
		Last Modified: Tue, 21 Apr 2026 17:38:06 GMT  
		Size: 202.9 KB (202908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d96bb1bb60cde6b35b621d350883826c6710b6732ae769cf16575fbf31acb82`  
		Last Modified: Tue, 21 Apr 2026 17:38:06 GMT  
		Size: 22.7 KB (22702 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.22` - linux; 386

```console
$ docker pull ruby@sha256:bc1a9e3e725f9a4f3ea281aec5878ba93a44ec37db7959afc81e0eef24f310cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42700780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3395a9bb959157baf7860f3ac93af59a84f104ee7c8ab0e79d563da63ec2f1`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 19:37:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 21 Apr 2026 19:39:38 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 19:39:38 GMT
ENV RUBY_VERSION=4.0.3
# Tue, 21 Apr 2026 19:39:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Tue, 21 Apr 2026 19:39:38 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Tue, 21 Apr 2026 19:39:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 21 Apr 2026 19:39:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 21 Apr 2026 19:39:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 21 Apr 2026 19:39:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 19:39:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 21 Apr 2026 19:39:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efed09ae68c0c151d3f3c564613496cf15ad386d531268312e0a3ed11e8e236`  
		Last Modified: Tue, 21 Apr 2026 19:39:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bdd09eb6f8618cb9f074e24713ddc395b3ed3bc3980587866e66c49383e87b`  
		Last Modified: Tue, 21 Apr 2026 19:39:47 GMT  
		Size: 39.1 MB (39075732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dcf0247b01af6ce3cc0e3602c2e374568378deda2a745208ed8f8058f0e9d6`  
		Last Modified: Tue, 21 Apr 2026 19:39:46 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:70afeda9ae30265ee036649867ad436da291978c7bdbd0dfab1350356a232c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.4 KB (222369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf346554a45cf63a8e471e740e834c96d43d7f7bba83d9e3436992d089d1721`

```dockerfile
```

-	Layers:
	-	`sha256:bb1f9b66ba250a2751da5c95b19252f01356ddf68728d589a7e905f5f8612cc1`  
		Last Modified: Tue, 21 Apr 2026 19:39:46 GMT  
		Size: 199.8 KB (199837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd93c31b0895ff042ae8d6cf7fde647bf5c9aecf8ec912b95618201ec44143e`  
		Last Modified: Tue, 21 Apr 2026 19:39:46 GMT  
		Size: 22.5 KB (22532 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.22` - linux; ppc64le

```console
$ docker pull ruby@sha256:2645dba5c027b18ee5b7737e69a206da8d26fd35373f3a631f8afdc4c906a97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44596704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c88e95e47ea1c650be548c8e95919724b26c6ab403cb15ff1b984239f382f0c`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:58:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 21 Apr 2026 17:47:24 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 17:47:24 GMT
ENV RUBY_VERSION=4.0.3
# Tue, 21 Apr 2026 17:47:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Tue, 21 Apr 2026 17:47:24 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Tue, 21 Apr 2026 17:47:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 21 Apr 2026 17:47:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 21 Apr 2026 17:47:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 21 Apr 2026 17:47:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:47:25 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 21 Apr 2026 17:47:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2a4eb80f9e51dff402e569adc4e1084a404f43137fdd0acf96a3cde37a485b`  
		Last Modified: Fri, 17 Apr 2026 02:02:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d494333072c58debb540c0aaebf2e657ae4492d71d9c598e5ea30443a9c320`  
		Last Modified: Tue, 21 Apr 2026 17:47:45 GMT  
		Size: 40.9 MB (40859720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5108a34fcb00087e026b2797dd949226b3e2df762b6c514367da1178d8e689df`  
		Last Modified: Tue, 21 Apr 2026 17:47:44 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:de9d89277496ad8b22274ac8bca031ee3dda75b0a1e651e04ac8334bd2da9d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f815d9e90ae16fea44d2194affb0af682f22b7a4575fd1a8943aca637cc232a`

```dockerfile
```

-	Layers:
	-	`sha256:912886cb5b1c6a9a8a994c979ef93aef1597e864f82f578aeb7ba362c242c551`  
		Last Modified: Tue, 21 Apr 2026 17:47:44 GMT  
		Size: 197.9 KB (197945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aae54b47bb3c5571ca6cd44d2f41111583c92276a4f4ccaf7d3be90126bf012`  
		Last Modified: Tue, 21 Apr 2026 17:47:44 GMT  
		Size: 22.6 KB (22616 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.22` - linux; riscv64

```console
$ docker pull ruby@sha256:6e8d15d64fbd22df28452839a4602e6c13c86ba873203624463be30aa3e441b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43906466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48397afa2c30b117bdc735774d05e403617ec18085f693b992ede57e1cc808ba`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 10:34:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 22 Apr 2026 01:56:04 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:56:04 GMT
ENV RUBY_VERSION=4.0.3
# Wed, 22 Apr 2026 01:56:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Wed, 22 Apr 2026 01:56:04 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Wed, 22 Apr 2026 01:56:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 22 Apr 2026 01:56:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 22 Apr 2026 01:56:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 22 Apr 2026 01:56:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:56:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 22 Apr 2026 01:56:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb21a08d5839b637b9824ed6b3ef7431390966a49ebc9fdf0e39feb214392411`  
		Last Modified: Sun, 19 Apr 2026 12:30:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5403d5f715747c2bdce4f98d396478c7420967547be7f9796968b5705d30e00`  
		Last Modified: Wed, 22 Apr 2026 01:57:29 GMT  
		Size: 40.4 MB (40385258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc439473b33e5421fbd0fc978385e7cb75fd024bc491f9fa60a3d52abaea7326`  
		Last Modified: Wed, 22 Apr 2026 01:57:23 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:75e240ff47994a3ee5f8604b5160f5b53b990a86fc8a8aea8235d483f84fbe19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 KB (220555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968a7f0578fb147f927ed49db9dea3a61c753ae1806ac5ac7795b41dcae294c1`

```dockerfile
```

-	Layers:
	-	`sha256:4e044c45b711c4a57309256f3811acce14f469d61041397283b06763441e347b`  
		Last Modified: Wed, 22 Apr 2026 01:57:24 GMT  
		Size: 197.9 KB (197941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:536bad65394bc59c85990a58ec27b8cd6749484f8011d065e54170f7c69907a0`  
		Last Modified: Wed, 22 Apr 2026 01:57:24 GMT  
		Size: 22.6 KB (22614 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:alpine3.22` - linux; s390x

```console
$ docker pull ruby@sha256:ab465833b04a2fe7391d1861f067c5da4fb3ec0ce5eb8d36e44a4b56a36039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44460546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb0b53be11357f3248f6048ecbbf4247da4a7bf81e1561bb1bee7da4fb428967`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 17:32:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 21 Apr 2026 17:34:58 GMT
ENV LANG=C.UTF-8
# Tue, 21 Apr 2026 17:34:58 GMT
ENV RUBY_VERSION=4.0.3
# Tue, 21 Apr 2026 17:34:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.3.tar.xz
# Tue, 21 Apr 2026 17:34:58 GMT
ENV RUBY_DOWNLOAD_SHA256=22cf6005d25bbe496b5ebe9224d63a1aaabfbfe02591bb5d612517c5a7836f29
# Tue, 21 Apr 2026 17:34:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .ruby-builddeps 		autoconf 		bzip2 		bzip2-dev 		ca-certificates 		coreutils 		dpkg-dev dpkg 		g++ 		gcc 		gdbm-dev 		glib-dev 		gmp-dev 		libc-dev 		libffi-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		ncurses-dev 		openssl 		openssl-dev 		patch 		procps 		yaml-dev 		zlib-dev 		ruby 		tar 		xz 		yaml-dev 		zlib-dev 	; 		rustArch=; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') rustArch='x86_64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-musl/rustup-init'; rustupSha256='e6599a1c7be58a2d8eaca66a80e0dc006d87bbcf780a58b7343d6e14c1605cb2' ;; 		'aarch64') rustArch='aarch64-unknown-linux-musl'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-musl/rustup-init'; rustupSha256='a97c8f56d7462908695348dd8c71ea6740c138ce303715793a690503a94fc9a9' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		wget -O 'thread-stack-fix.patch' 'https://bugs.ruby-lang.org/attachments/download/7081/0001-thread_pthread.c-make-get_main_stack-portable-on-lin.patch'; 	echo '3ab628a51d92fdf0d2b5835e93564857aea73e0c1de00313864a94a6255cb645 *thread-stack-fix.patch' | sha256sum --check --strict; 	patch -p1 -i thread-stack-fix.patch; 	rm thread-stack-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .ruby-rundeps $runDeps; 	apk del --no-network .ruby-builddeps; 		cd /; 	rm -r /usr/src/ruby; 	if 		apk --no-network list --installed 			| grep -v '^[.]ruby-' 			| grep -i ruby 	; then 		exit 1; 	fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 21 Apr 2026 17:34:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 21 Apr 2026 17:34:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 21 Apr 2026 17:34:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Apr 2026 17:34:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 21 Apr 2026 17:34:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5767f367d10a89d950d7ec3f5c51a2e46baf459292728a337db97395cd011020`  
		Last Modified: Tue, 21 Apr 2026 17:35:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c548ca3437a6927f25f485d76cf0e7d9b97daf0678a67eb987ce973e963257c`  
		Last Modified: Tue, 21 Apr 2026 17:35:13 GMT  
		Size: 40.8 MB (40806345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a74e8673e62152b8f8f94149bbcef7a7b099ab5ec3c3bbcca379daf4c96fda`  
		Last Modified: Tue, 21 Apr 2026 17:35:13 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:alpine3.22` - unknown; unknown

```console
$ docker pull ruby@sha256:af51ac5936428c1e2da1f5f88bf85416543199481d2491bca6294314356cc3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 KB (220479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690559a5b5b91c652c49cb830f9909c8fc56b69da0f102c3b30f5cb24d58b790`

```dockerfile
```

-	Layers:
	-	`sha256:43a5d74c05ed884b49d7c2648b4f487f5dbb6d1d1c2d5dda09461d77e410dcff`  
		Last Modified: Tue, 21 Apr 2026 17:35:13 GMT  
		Size: 197.9 KB (197911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:480b0cba7870be8abaff7f49b83606f60abe3f5d200dae4dfbb80dad2a172322`  
		Last Modified: Tue, 21 Apr 2026 17:35:13 GMT  
		Size: 22.6 KB (22568 bytes)  
		MIME: application/vnd.in-toto+json
