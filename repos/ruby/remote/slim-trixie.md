## `ruby:slim-trixie`

```console
$ docker pull ruby@sha256:d13278cf83bad7b0d01913e13f0efd46ffa049d976548d98b542d586e046b3e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `ruby:slim-trixie` - linux; amd64

```console
$ docker pull ruby@sha256:1fbc01ba38b664604059211f69fa5414301100e84468479a08225245cced1ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80646597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2584e1c034d71cf9267778171aeb5d489cdbfc90f703d4fc292697f7c8a0405c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:52:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 17:52:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 17:54:42 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 17:54:42 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 13 Jan 2026 17:54:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 13 Jan 2026 17:54:42 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 13 Jan 2026 17:54:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 17:54:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 17:54:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 17:54:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:54:42 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 17:54:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c761539f2c758469db5fe777555ae24b833cc2d98eb0f0d9c9605bb463bd0187`  
		Last Modified: Tue, 13 Jan 2026 17:54:51 GMT  
		Size: 1.3 MB (1279389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a82e927bddd76b2a9d6bc96d3e0bc311ac72f6defea5007641e745a47fda0d`  
		Last Modified: Tue, 13 Jan 2026 17:54:51 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a1ce9123ed3d8145cbecff04f8e8d3fc7b27e3b6bd1eb81f1aa464d3bce35e`  
		Last Modified: Tue, 13 Jan 2026 17:54:53 GMT  
		Size: 49.6 MB (49593191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a9cd433891210d259351ebb487ec26273b5e8309245a147445026ac37e3e83`  
		Last Modified: Tue, 13 Jan 2026 17:54:51 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:28629b757701ae4e680a483a3c647023fcf160c1db322e98ed29edd300dafbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bce2e943db2cb9d72995fa4aac6161703d7e12c989caa4128a74242d0a83ce`

```dockerfile
```

-	Layers:
	-	`sha256:1cf8a86e67ad7461fe861712f76315d90bf3753b5a456ca3c0123f99ab072b81`  
		Last Modified: Tue, 13 Jan 2026 22:02:29 GMT  
		Size: 2.2 MB (2215998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e7e39e193c4727a6ebee732a3782418d882c7367858c01474661813e4cacd0`  
		Last Modified: Tue, 13 Jan 2026 17:54:51 GMT  
		Size: 24.3 KB (24320 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; arm variant v5

```console
$ docker pull ruby@sha256:ac594621ee48ed97aa242381b1ab8e355a8e92ec0a1fd4db4398aa3c8e68623a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71840795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59052cd0c5f06d4dddc30d9a428c3c0665ed7953c08b23f9313f7836d31b76ed`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:55:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 17:55:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 17:58:27 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 17:58:27 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 13 Jan 2026 17:58:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 13 Jan 2026 17:58:27 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 13 Jan 2026 17:58:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 17:58:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 17:58:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 17:58:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:58:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 17:58:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e19b83481fb1dad1d7d98683324067c215c336ce3625be91a87952310d9c27`  
		Last Modified: Tue, 13 Jan 2026 17:58:44 GMT  
		Size: 1.3 MB (1263020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fb157595793db4afab228b771c9f7ecd625617408d50a6c945a7c7c9f60968`  
		Last Modified: Tue, 13 Jan 2026 17:58:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2561bf71b39573267b7c364f3270eab6d8bb9c01665ff4a40c6042a3a1ca274`  
		Last Modified: Tue, 13 Jan 2026 17:58:38 GMT  
		Size: 42.6 MB (42634719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c41cb7f702148dabfb36b3c82d76dc6c638445d2c4b3e08d0c765e99aa34ee`  
		Last Modified: Tue, 13 Jan 2026 17:58:37 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:e98f724173826b8c187a7cae74dab6aec7c16ba48b629a6e17475ba3feedbd2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c824bafa9fe50418eb3f9d98a539b62bc27831f44f1d7d443793550d194ce3a`

```dockerfile
```

-	Layers:
	-	`sha256:16f8e2e4fda0ab0b751959d758516050c784d05d274781fc9d540747353b0901`  
		Last Modified: Tue, 13 Jan 2026 22:02:34 GMT  
		Size: 2.2 MB (2218993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb47ad69c2df25c2621f57a34ae8912494ac79a0f26bc00847f44f49f6dc17e`  
		Last Modified: Tue, 13 Jan 2026 17:58:37 GMT  
		Size: 24.5 KB (24471 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; arm variant v7

```console
$ docker pull ruby@sha256:a8e0ab26018adbaf80ab978b9f9d7efc1ce30e00bc495a6478f1a1b712b888a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69916431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634ca14d40e60adbe9cbfab29b401509ecdc86decaa068fe717e3271ad09482b`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:57:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 17:57:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 18:00:37 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 18:00:37 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 13 Jan 2026 18:00:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 13 Jan 2026 18:00:37 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 13 Jan 2026 18:00:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 18:00:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 18:00:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 18:00:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 18:00:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 18:00:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaf0143e7e43141f7be9c33c221ed05fbcf60060d94c5fa283abcca1f331e9f`  
		Last Modified: Tue, 13 Jan 2026 18:00:47 GMT  
		Size: 1.2 MB (1236541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080cac65da09517ab67d2478e2f476b83498d051641e5e26f15e9993f3abd66d`  
		Last Modified: Tue, 13 Jan 2026 18:00:47 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fd19edc0c3ee51fd0470979dff7dd4dad419b65ba28bc1de60e7ebe9157d34`  
		Last Modified: Tue, 13 Jan 2026 18:01:01 GMT  
		Size: 42.5 MB (42470980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfab491e42850ce322982b2ff324a495d164779c5c1332fc16c84815586dca0`  
		Last Modified: Tue, 13 Jan 2026 18:00:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:cf44b5673bc838ff1d48b2b37c086d5a46f5983f8fa2100a0c7e68a885529741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21fe9e11f87423178075e0365285d9386042b949ced176a4c0f7bea50262ab4b`

```dockerfile
```

-	Layers:
	-	`sha256:93333b6d38964bbc309542320063865599c93cad682b3af5f4843b1f34d9dc66`  
		Last Modified: Tue, 13 Jan 2026 22:02:46 GMT  
		Size: 2.2 MB (2217434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33e88fb81def5828f8423d6ff702d7198c6ece2718837b6989230cc22a64193`  
		Last Modified: Tue, 13 Jan 2026 22:02:47 GMT  
		Size: 24.5 KB (24471 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:9c9fa249c42decb40c8ea030abf66d0dc99cb51579dffbcf419c06f1d03669b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80855299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ebac19d041d6e6a41a8e5500c3ffe516792a35bd3ac40386f63dc3c2d6939f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:52:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 17:52:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 17:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 17:54:55 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 13 Jan 2026 17:54:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 13 Jan 2026 17:54:55 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 13 Jan 2026 17:54:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 17:54:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 17:54:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 17:54:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:54:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 17:54:55 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ca7922754598b4e7b16f0cce5752cd24ce6048105f14bb6d9ff60fa7353550`  
		Last Modified: Tue, 13 Jan 2026 17:55:13 GMT  
		Size: 1.3 MB (1261707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68822db04c33c7c9a0be337a9e6e8710ce8db2e4b50b26cb1cd7a734f26ebb5`  
		Last Modified: Tue, 13 Jan 2026 17:55:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:966752dd42e57566699c86624d35d2f13c03863a849fdc4e35ad749cda4a2a7c`  
		Last Modified: Tue, 13 Jan 2026 17:55:16 GMT  
		Size: 49.5 MB (49459218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88427256f34890407deff875302196ab7b32d026f819a3e4c4208bd6ca6c9e2`  
		Last Modified: Tue, 13 Jan 2026 17:55:05 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:7298603be87aed073ed1d48d712260c2abf685a593a6b18a144ed03c2eb86d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed8bfccfed0d387c6b937987ba528ce8ae14722f3b7d63cc70432fbd5c09dee`

```dockerfile
```

-	Layers:
	-	`sha256:2c91ba34d1f7468cfb60abb7415d209160f61fed54c9b4b80b7441260bf7e3c2`  
		Last Modified: Tue, 13 Jan 2026 22:02:51 GMT  
		Size: 2.2 MB (2216306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0db630c50170234037623ab44f2254e1536f7da24fb8665c7fd4d4a6b4768af`  
		Last Modified: Tue, 13 Jan 2026 22:02:52 GMT  
		Size: 24.5 KB (24515 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; 386

```console
$ docker pull ruby@sha256:5827367ba3ef46c728a0493eb34b854743fd2dc0e5a708fe16f1c324f8633c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74942643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddc29c468384b494a6142975c77e9a6d5292bb9340777992c97d25ebedc8e7b`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 17:53:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 17:53:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 17:56:17 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 17:56:17 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 13 Jan 2026 17:56:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 13 Jan 2026 17:56:17 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 13 Jan 2026 17:56:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 17:56:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 17:56:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 17:56:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:56:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 17:56:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279d155c895805dc4f52ecbfb03137515c19585e0c9e4037af71c67120db82e9`  
		Last Modified: Tue, 13 Jan 2026 17:56:27 GMT  
		Size: 1.3 MB (1287245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f847be77b1db3242323f6d91cae8caabbf241844b5eef1281548e1671e5cd759`  
		Last Modified: Tue, 13 Jan 2026 17:56:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37708885362e6dd1f4056e4aebfdad92e6f6f18fc309611f75830e37801c847`  
		Last Modified: Tue, 13 Jan 2026 17:56:46 GMT  
		Size: 42.4 MB (42366590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f811bb7079745422d7c0ea0e4d2bcf4e94833a74512b2cafc56b075b03a761`  
		Last Modified: Tue, 13 Jan 2026 17:56:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:1a23397ec58507043259ee18a608f32f0537bf806ffecba642a352bc0d049b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c63f15615d37de8125e54c6bf486aa774b7c93c8adf1e6afd92dbd7a1fc016`

```dockerfile
```

-	Layers:
	-	`sha256:eac2008b3732fbecc7701e9a9e552a77a7fc78531c05514e4747dae60d2d8c52`  
		Last Modified: Tue, 13 Jan 2026 22:02:56 GMT  
		Size: 2.2 MB (2213171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:006ed94af966c316abc29f92f4ee5bb2e24844ab9d1c81dbbd56aa70cc3421b6`  
		Last Modified: Tue, 13 Jan 2026 17:56:27 GMT  
		Size: 24.3 KB (24262 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; ppc64le

```console
$ docker pull ruby@sha256:0b0a66713813cd382b1e69d901970a4fdc874ff022d1dbbd1d5410792941b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79353457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c02e813dc08d28e526e992762672123b273092e02b1660389c05cc5ae684f0`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:13:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 20:05:00 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 20:05:00 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 13 Jan 2026 20:05:00 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 13 Jan 2026 20:05:00 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 13 Jan 2026 20:05:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 20:05:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 20:05:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 20:05:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 20:05:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 20:05:01 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd359a7e5d3b012a0e1f773e5ca872b7185e1ae4c53f7a9a7d797ae3eaaf8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:33 GMT  
		Size: 1.3 MB (1309726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eeff64fa1ee2c5a20375771788d22ec3d5ad95481b75598a70ada63b47d8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f085ab932c13778f15a4f85e79b8cd40078ea31cafcaa0e8b6019f2498095c86`  
		Last Modified: Tue, 13 Jan 2026 20:05:42 GMT  
		Size: 44.4 MB (44447798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69e216831dbd646ef043c6f9f420b1aede55e153ec77136c0354a33dc1da6fa`  
		Last Modified: Tue, 13 Jan 2026 20:05:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:44083809d03b2746ed3df4beb03148aca1446c4c763ad16b32afb2614fcdd26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76496c4432d50b022ab49f335f986ff8dc15fcdf5ff6e3af33b561ed9a17b039`

```dockerfile
```

-	Layers:
	-	`sha256:42bdcef035c9c4de3b9cd33e6ad122fd256aaaa48e3a426dedb14e7bdba14e91`  
		Last Modified: Tue, 13 Jan 2026 20:05:29 GMT  
		Size: 2.2 MB (2219551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b7422281ef8a01a8b11601b878a41ee6552c9ba8d405a4607c1022126aa2aa9`  
		Last Modified: Tue, 13 Jan 2026 22:03:02 GMT  
		Size: 24.4 KB (24394 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; riscv64

```console
$ docker pull ruby@sha256:06b94004312bb13996c05e7ddc3a66555761cba0c244f7013fadd4cbae9249f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73653167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08da78589c758470d29b4f30b877ed2614f9dce7af297b63418be7af577d87b8`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Sat, 17 Jan 2026 04:09:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Sat, 17 Jan 2026 04:09:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Sat, 17 Jan 2026 06:06:19 GMT
ENV LANG=C.UTF-8
# Sat, 17 Jan 2026 06:06:19 GMT
ENV RUBY_VERSION=4.0.1
# Sat, 17 Jan 2026 06:06:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Sat, 17 Jan 2026 06:06:19 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Sat, 17 Jan 2026 06:06:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Sat, 17 Jan 2026 06:06:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Jan 2026 06:06:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Jan 2026 06:06:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Jan 2026 06:06:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Sat, 17 Jan 2026 06:06:20 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:07:54 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1c0798e9db9f70a770c007ce63e432772d80acd8395f5734b23ec63a5b2266`  
		Last Modified: Sat, 17 Jan 2026 06:08:20 GMT  
		Size: 1.2 MB (1248002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae37805c4126b550aa387e73fa7be996c3c367d48b0361e80a75c4533ddc6f85`  
		Last Modified: Sat, 17 Jan 2026 06:08:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d13864dd6aa3a5d6041081ba5fc194bab8440f678e7b93460b5052fa4f783c`  
		Last Modified: Sat, 17 Jan 2026 06:08:25 GMT  
		Size: 44.1 MB (44133144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fb45cd01b9e3b0bab59426a15f725a20b8d57cc26a5a0cc0562cdc0989584e`  
		Last Modified: Sat, 17 Jan 2026 06:08:20 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:bd703e034a7912d1fab1c62f82d932f4c934ad7ae93a1adf862b77997905bbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2234340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906660612836861850a43895c7671ff1e2e50949716f7151095b15b373d52855`

```dockerfile
```

-	Layers:
	-	`sha256:95b0ae7d346c761bb5398a0eee156d2d01e73e46bdb9d089a0eec9a7c118d8fe`  
		Last Modified: Sat, 17 Jan 2026 06:08:06 GMT  
		Size: 2.2 MB (2209946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6664d93ebbd130aaee5d58267c0a0b8556ec0ff661bf71e22c94cdada8debced`  
		Last Modified: Sat, 17 Jan 2026 06:08:05 GMT  
		Size: 24.4 KB (24394 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-trixie` - linux; s390x

```console
$ docker pull ruby@sha256:907fa7e199d02a725973649f977f9c2233e7e6cea45e7f06e1f97f76f6db5128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75402407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e3a0adbdb8267b9d0108cbf8cd9b68104c189fbe1e131edf17c972b9c5f936`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 15:34:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 15:34:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 17:55:10 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 17:55:10 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 13 Jan 2026 17:55:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 13 Jan 2026 17:55:10 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 13 Jan 2026 17:55:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 17:55:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 17:55:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 17:55:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 17:55:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 17:55:10 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ebe8df5ae9a3c192917df536e6e2799579bf1d2b6bbf9ca3bd704371588ae3`  
		Last Modified: Tue, 13 Jan 2026 15:36:42 GMT  
		Size: 1.3 MB (1294317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b53ed02e8d194058b777d39a7f36b45a9eb763c87d209d795bc869a283099c`  
		Last Modified: Tue, 13 Jan 2026 15:36:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7097dc464a940400d174643e3510103755a6cde7fa3ac3b63773f7cbfdd1c1`  
		Last Modified: Tue, 13 Jan 2026 17:55:47 GMT  
		Size: 44.3 MB (44274348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633ca22226250407f5f515bc6e46808751eb4dee30370a47756057df1c636add`  
		Last Modified: Tue, 13 Jan 2026 17:55:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-trixie` - unknown; unknown

```console
$ docker pull ruby@sha256:1305a716fdfde5f8efaf99070249fda7fcc0550bca5f20857b898745d58224af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e41ba3722c365b48058fcfecc7b986955ea7de51b1e6cda838e110676ae1b8`

```dockerfile
```

-	Layers:
	-	`sha256:66f43d0c4c2b1d5ac48a574472a17d0d70cd5079e21250e1c0a180aea954466c`  
		Last Modified: Tue, 13 Jan 2026 17:55:24 GMT  
		Size: 2.2 MB (2217443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78cb0c8adb21bd91985fece303445d8ade466a3907ca06266326b06c2d19559`  
		Last Modified: Tue, 13 Jan 2026 17:55:24 GMT  
		Size: 24.3 KB (24320 bytes)  
		MIME: application/vnd.in-toto+json
