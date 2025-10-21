## `ruby:3-slim-bookworm`

```console
$ docker pull ruby@sha256:d6f651902589673f9652193bd39068be6ef05f1d808ab1ba24b45178e827c084
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ruby:3-slim-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:c2342e56b0d92e4bb8a7579fd28755bd9df43d4976df37067372c96dd5af953f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73227699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d60d48de34ef5946ac01cdae38d5d85bd41a55a586b730d45a49580d1b56ac`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df52d9df59fa0230c23a1ebdb3184d18844051ba557ed7a3f650a189d9a35e7f`  
		Last Modified: Wed, 08 Oct 2025 18:16:22 GMT  
		Size: 3.5 MB (3509662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd252c73c47da99bd18a694564b4832e6615384dee613b49873779da037f4f7f`  
		Last Modified: Wed, 08 Oct 2025 18:16:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe16e96e524a9fe6516f4a930fc2c9ec6c505ba61edbbc5d8a3324b4143d87f8`  
		Last Modified: Wed, 08 Oct 2025 18:16:29 GMT  
		Size: 41.5 MB (41489368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d2039cd1bd581b5f76bd7900e878aa3fc417f74f74597f79d972309f52083b`  
		Last Modified: Wed, 08 Oct 2025 18:16:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:2b5640102ae6bccf3ad3283326ffe1e0ba95a489e639508c8a48b9d5ea00ece8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3c4211c3b0876abe685c8299226243af522632b79dce8cd75d9d5d3479e327`

```dockerfile
```

-	Layers:
	-	`sha256:8cb71d6295b792290880aaa6d689c4fceccabee00ace49d79786efb76aedadc3`  
		Last Modified: Wed, 08 Oct 2025 20:59:50 GMT  
		Size: 2.6 MB (2601641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39f0e807c5d741e245fd057ffc48e46f8fd53cd46b2a69af45475e65494c004`  
		Last Modified: Wed, 08 Oct 2025 20:59:51 GMT  
		Size: 23.1 KB (23130 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:09bdb2904a25a7da842fabd98c52485d93b2295a01bb9e3873bd50f410654498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66114019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b79f43ebaf599c8b42060fb504f1d4b3f3e3ea3e9c22d531d8b98d5f470019`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 07 Oct 2025 23:03:17 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f982c9691d15a93fba0c1226ca85169d870439f0b6119d1ec61ec73d2a7dc8c3`  
		Last Modified: Tue, 21 Oct 2025 00:19:59 GMT  
		Size: 25.8 MB (25757495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e467a49a40cdef7c346202e88ef93b2d4900cd38bbc75f629de39330f1256da3`  
		Last Modified: Tue, 21 Oct 2025 03:19:27 GMT  
		Size: 3.1 MB (3079804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81843613d8a9cbd9cf4de8733459d539ca439055b854b33ef7e5bd98ebd868c7`  
		Last Modified: Tue, 21 Oct 2025 03:19:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9db9a2c57bd44f11b31dfe8f7e46e04af62bb7776f2cd261ebbf9547319afb`  
		Last Modified: Tue, 21 Oct 2025 03:19:31 GMT  
		Size: 37.3 MB (37276388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5ac7499810db4b1d9fb4d453264044279304bdd1709aa937f5a39f2a58a9eb`  
		Last Modified: Tue, 21 Oct 2025 03:19:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:dbf1744edc1294b4f1c919dacbecd96312d04247bfaa3e489f3ded76b5010229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb55b398f385d3c4282c84632ff1b164af0128cffcb81f01822b1dbfa24fe62b`

```dockerfile
```

-	Layers:
	-	`sha256:f02e62315952f768f296c4d9d45f343066bfaa22b5035023725bae95a7f4262f`  
		Last Modified: Tue, 21 Oct 2025 05:57:39 GMT  
		Size: 2.6 MB (2605446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd420530b08f83832824e0ea4095c7cc548525c3e999c773ed2213246d818b9`  
		Last Modified: Tue, 21 Oct 2025 05:57:40 GMT  
		Size: 23.2 KB (23249 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:8b7f75ccb7514818e129836feca434286f9c9fed0f4b3c61d59b6ff83fd74db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63960783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f911977304bb0c28f5360d8a8c84521c474ab46225a623358581227ed36ff55`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4c0d784fb90dddd991d201014e92ef1ebfe9a20d0f2ea56e2701fb9e8219be91`  
		Last Modified: Mon, 29 Sep 2025 23:34:19 GMT  
		Size: 23.9 MB (23933930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a45642dc3d89be0cf8df87b0c0f11a00b08bf70a0a6df38c0e55aba775d279e`  
		Last Modified: Wed, 08 Oct 2025 19:06:19 GMT  
		Size: 2.9 MB (2912734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02a8a24c2e90eff788ae72d18655ee782dccab7925d5db8018826b4546a5f1a`  
		Last Modified: Wed, 08 Oct 2025 19:06:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69217c66b9934386931e0162a9c214b485f4b6a2d2b18ce76be4c2d92363c22`  
		Last Modified: Thu, 09 Oct 2025 00:35:54 GMT  
		Size: 37.1 MB (37113786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d075baa1651da48db1832c174719dee45270ec7b2b2a50a3f8dfcf6ec8f7d661`  
		Last Modified: Wed, 08 Oct 2025 19:06:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:66d2c9335f275535d5202b4fa6d310d2644d3d6fd1557e2ce35e3ce9256253d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09bfb657bfd67bf14d0fd9cc2fe752a284ae76aa6f5cc5bbbe305fd7e4a59d9`

```dockerfile
```

-	Layers:
	-	`sha256:2b8f426130d6c4d7efc43e1899c762c807ad84f3cbe0fb96fb96598d1f43a877`  
		Last Modified: Wed, 08 Oct 2025 21:00:02 GMT  
		Size: 2.6 MB (2603865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62c31434dc009e3cbe5edbe17c284488668dc7b2807431445a108f7860797017`  
		Last Modified: Wed, 08 Oct 2025 21:00:04 GMT  
		Size: 23.2 KB (23249 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:836e64981960fad1681c13e9347ffc9939ad4130d46fcb5ed7a91421b6a85b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72846527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40c68254a84758a16b16fa995367831ed02f20e3928ae0461da3f4c47f99aed`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f899e85cfc230e8470b709b0d22f32511a4acdfe2669a7a182ff7efd5e67e9c`  
		Last Modified: Wed, 08 Oct 2025 18:16:08 GMT  
		Size: 3.3 MB (3340610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4169cd47869bb9313fee938e5715454a6912f2c7b9af927563834721e6995e32`  
		Last Modified: Wed, 08 Oct 2025 18:16:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9b682b0bcb54640d63a2c8afa481e5deb65cb0536c039306d815f667a14ffd`  
		Last Modified: Wed, 08 Oct 2025 18:16:12 GMT  
		Size: 41.4 MB (41403439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:517e2e82c299106e692b277d7786798161e481645c97e5a1bab1069209cbc074`  
		Last Modified: Wed, 08 Oct 2025 18:16:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:1f52640e94c71cfa6a663838dc9ea0ccabbaf790e1c3fffbe9bd56e7c3a510ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a5e6a49c6ab64d99475b3008fe39c9d717940bee9500aa4ecfea6cd1fa91e6`

```dockerfile
```

-	Layers:
	-	`sha256:dc0e769722327b322a4d4a2b0714fdbba25315606c4e8d62e6056edab846701f`  
		Last Modified: Wed, 08 Oct 2025 21:00:11 GMT  
		Size: 2.6 MB (2601899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ee2929f3c9c63bc8b9fc455d7786a7dc22be161b2ab61c3a556c676b6b7e75a`  
		Last Modified: Wed, 08 Oct 2025 21:00:13 GMT  
		Size: 23.3 KB (23279 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:404fa3c5c122190a3696eaa8876edfa778d43b47d251cae1f64bf34753cc05e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69795746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1b03ffcf222cd0ec618cd99c63e95c4642d6729a423d28fa210a2b99505f10`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942fe311490b89e76d3bac82ed5bc4df2c07d5c9f7593a87ad56405e8cfdf6e5`  
		Last Modified: Wed, 08 Oct 2025 18:14:07 GMT  
		Size: 3.5 MB (3511024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff2d459da1d402aca1355fd03af974eda7a5085de9a3b17bee156715b6332bf`  
		Last Modified: Wed, 08 Oct 2025 18:14:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909c63686b5140f19d47876eecbaecc9336c6d5ffc0526f5b835a489988b9ba8`  
		Last Modified: Thu, 09 Oct 2025 00:35:57 GMT  
		Size: 37.1 MB (37074758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6b0280bf90e8c855cc3e8e6991d1d5fc8b9567bb60596ea85a7d18cd6e52b8`  
		Last Modified: Wed, 08 Oct 2025 18:14:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:d423b547316b869c4c355df228cd35f7c11c9c978e92b5845e5fb2dd385e8eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f751a5a19bf23111be9b3aa5bc6cec84b6a4b7b72f7035f36961474e460293`

```dockerfile
```

-	Layers:
	-	`sha256:d5f66ab10f8e5f01e065dcd62081f0fde15b27172c10d7f3d1fc3883553ecd6c`  
		Last Modified: Wed, 08 Oct 2025 21:00:17 GMT  
		Size: 2.6 MB (2598822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10dbe58f5b69a379eb785436aa50161252d9da42efbffac109f0911cd4d85bce`  
		Last Modified: Wed, 08 Oct 2025 21:00:18 GMT  
		Size: 23.1 KB (23092 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:3e7db9bf9b8730d218b6caf9c8b7fc146a6a946c54a82fac5fb82aa3b887ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72041326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d5fbfb62198886b1e893db44c318c53521db44bee8769a0c46efe0cf3d206e`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:73d0a1261a90ced7c792643cb457a2c9f7bbeca1bcb84939b4029c5a1f01f26c`  
		Last Modified: Mon, 29 Sep 2025 23:34:06 GMT  
		Size: 28.5 MB (28513676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc185cd20a4d1332e5082d3212155eca1d67ff79aa1f54b8bda25e9b0231064a`  
		Last Modified: Tue, 30 Sep 2025 20:06:43 GMT  
		Size: 2.9 MB (2900465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3431ba64b343d7d70ab359ee84e84bf36fd1753a338cb9bff103e60d76d93449`  
		Last Modified: Tue, 30 Sep 2025 19:16:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9bc390f2a57e0184f3229fed71a83b76097fcf6d270b61e52bdd1726e027ab4`  
		Last Modified: Wed, 08 Oct 2025 18:41:44 GMT  
		Size: 40.6 MB (40626852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764cc71dbcea2dc70f4e513fdf289506b0c69fa0facd121229202a39d1242172`  
		Last Modified: Wed, 08 Oct 2025 18:41:39 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:e18b41652abea56caa5fd7f82677ba29659634d7ed4795122d3221b0e35e68dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 KB (22990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2abc060a8f0f2459f38b43ef06c2b345c159f4f5cff3813c675fad6a8f0ce1`

```dockerfile
```

-	Layers:
	-	`sha256:a6edb7c07535bdc3a498175e884b182ef67361b6c120ecf9bebfcb4b8622fd9e`  
		Last Modified: Wed, 08 Oct 2025 21:00:22 GMT  
		Size: 23.0 KB (22990 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:165dd26d8e24a5a5342ff02a8da22b542ceb8444a55d91f213b3f5906a368ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74723238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee22b24a6e3030cea0282bd7056bc2ad8f8d2107b2cee091df40d75761044974`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032c7f41aa3c2ac6d89b54272b44fe3f04b08e0e4eaab1f4fd0e4356ac29bea7`  
		Last Modified: Wed, 08 Oct 2025 18:47:17 GMT  
		Size: 3.7 MB (3709077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95c2f86ca7be5b394c6b9768dc9c9d7082013ece5806ce68e8fd626d62388ce`  
		Last Modified: Wed, 08 Oct 2025 18:47:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d8963f9dcd12d8c98579ec5386aed4c9774e20dd969cfd6712911fa3661e03`  
		Last Modified: Wed, 08 Oct 2025 18:47:20 GMT  
		Size: 38.9 MB (38945131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badca3e9e575b5a63097ab08f6a206b159e18b5484b5da8f8b6d357842457542`  
		Last Modified: Wed, 08 Oct 2025 18:47:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:1f66fb246db1a7cdbd4b54fc3c8c5dd7f5329caf958bb16dbf7c1a33b6055811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8e0fcfa071b1e59a00bc162cecfc3bf6a27942cef40b0dba350b1fa143dea57`

```dockerfile
```

-	Layers:
	-	`sha256:6bd59b1a6ddf775a913bb133bc04e5baf31a49664eee6c970429a6f115b2a32e`  
		Last Modified: Wed, 08 Oct 2025 21:00:26 GMT  
		Size: 2.6 MB (2606032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36c57b4f58be8617117eb09d8a5f8b8fcc9156c184bb61c442c1e9eb9e0f8505`  
		Last Modified: Wed, 08 Oct 2025 21:00:27 GMT  
		Size: 23.2 KB (23180 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:aff300bc5f6d4c83078c8af7c1abda2f61f56376d55931bac22851b6c3f92bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68186744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6962e086662ce28027b09859bcd4d73692eb921b60540738514b8b3d372aa1`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV LANG=C.UTF-8
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 07 Oct 2025 23:03:17 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Oct 2025 23:03:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 23:03:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Oct 2025 23:03:17 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e8e20085e9a53bda26d3ce9488db23293fd5b4e87bbc562f15dd908e389f6f`  
		Last Modified: Wed, 08 Oct 2025 18:24:33 GMT  
		Size: 3.2 MB (3170283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6d3c8193a156edaea6ec9b49418bc8d44deb71072118fdc3f4acdabdc40a27`  
		Last Modified: Wed, 08 Oct 2025 18:24:32 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df55b42defdd2e6e99aecf81231c6d32a526178d2d047cc7ae6c3759daeb7f7d`  
		Last Modified: Wed, 08 Oct 2025 18:24:36 GMT  
		Size: 38.1 MB (38131807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dd165be00bb42c1edc23fb693e0c629531f531042727f11c717ba2ec31ed67`  
		Last Modified: Wed, 08 Oct 2025 18:24:32 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:73036a7f510e2f7812d7e18f91ad5148d70631720b2751eeba6b71c176bd07a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4beaf469cbe5393c26a0e5b0e212306dd355c2bca34372014d9f3f61eb73d150`

```dockerfile
```

-	Layers:
	-	`sha256:a46af36e37fd0cfa1ab50b07c08797f1e03da2f85961dda5bd4b9489696f3a79`  
		Last Modified: Wed, 08 Oct 2025 21:00:34 GMT  
		Size: 2.6 MB (2598472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9254833af9ba5caafae8c10ff5eab84a86064c6f10daf5a7319347ae059f08b2`  
		Last Modified: Wed, 08 Oct 2025 21:00:35 GMT  
		Size: 23.1 KB (23130 bytes)  
		MIME: application/vnd.in-toto+json
