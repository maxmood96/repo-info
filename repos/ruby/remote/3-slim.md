## `ruby:3-slim`

```console
$ docker pull ruby@sha256:51d8b4d6f1cdfc45bc7764c3def28c8469ee8cf4ecd632d0efbb7e5a8175e3b7
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

### `ruby:3-slim` - linux; amd64

```console
$ docker pull ruby@sha256:f8995929e4eb94f187b6a29ae6bd7e6c87c45e5aa83251752eff7e07d0f10515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73170782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13bfeebcb69e0b4cce88e919186aed7fcddf359ca8dadd184fb386197601b200`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95c885d11163cea6141f2874f7609fd353fae57178c697f1a7d40224f7b00cc`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 1.3 MB (1279331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7f5fbc95c257016cbdb5dfe0a0139978a0a4a0d17362943647c993cd4bcb99`  
		Last Modified: Tue, 24 Feb 2026 19:49:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05f4e549e9c58aeab34c05f03badc598c63a0b59ae9c2fe69be781ab5544df`  
		Last Modified: Tue, 24 Feb 2026 19:49:39 GMT  
		Size: 42.1 MB (42112489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce46bb75e106e62f4498c163d02fd7018cc5ceaa37cf6b822414c2107df184`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:b28eb42d227085835dbc15ac4e49c86f00baa81072fa9f86ce858eb561f3ad7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9518e15ee443f276d8bd771da9ea88dd0f81f52478ce27593a9797ecc652d3b3`

```dockerfile
```

-	Layers:
	-	`sha256:5d501516e60fc10b96df8a6e6dc182e813db497a4abb3a9800968119e6a594a8`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 2.2 MB (2219393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1165cb1861afc3288fa509c3fd02e7f9060252fb48041b07c1e84b36494ddbe4`  
		Last Modified: Tue, 24 Feb 2026 19:49:37 GMT  
		Size: 23.6 KB (23612 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:b4dd47cf4d346adce16cb7678e6e20a728a67eddcff8667120983e7d30e7d482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67117180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b1740b5ff695fdcd934271b9d92de2f15c4bede63e704c230dbac84dd8259c`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc96269d7ff6661f7c783aa28ef266b6a3454b0b7270f35fd67c75efbb126325`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 1.3 MB (1262995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dde3052860b01def3c7729ab7e0b552cfc8471229c632727c524ba36ffa87c`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feb54b5087fc558951fafdb4a294dc5d0cfd9f91b23c76b4e5f03fb58403146`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 37.9 MB (37906244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd1652237e976a13ba3e6c119a312c9ef9b52d4d968f91702f2ed8dac11a6d`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:b2af01a66db1becbca4172d64b5b75a5ae07a888c3b3a047c860f38655f04dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2246119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63091311e60900eedadb0313364064040ac7b3de547eb05dd5c47f63e59bcf15`

```dockerfile
```

-	Layers:
	-	`sha256:dfa722ea8e2fe753b2414ac2c6a8bf8c7d68598ff50a23aa7d5ee3d0ccc314c2`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 2.2 MB (2222372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b9ec032e1c118282b515898503ec924c0700ab89159c7bf2eab30bd24e6d87`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 23.7 KB (23747 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:2348b385a79312d14056dc500206aadb969aa5e9619ad5737488c5b0184adb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65218044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eac7780c7f3d3186e754f906cadc64593d03ff0a9dcaf3901d60209199295c3`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 21:09:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:09:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14feba02466030de4233bb2b9b4ae7bb8d22598db9db35967cc9269952aa2190`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 1.2 MB (1236637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991f1e7bee0c079b1385009eded49ec5445b76573d3c6311e6d7a8472bbeebd`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f4b57fa9f91ef9277385833d43232d221aae42613777d8a1984c4d140abdf8`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 37.8 MB (37767330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865adf2d3ca7b76be7f98186142a67e87adc8e14da1a9c847d4838d387f91d2f`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:aba32152d528002d1aca68181f2ec92cef16c54b111a0e084b319f77ed0f8bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6be3beb05eaab67ec5e8272239046f9994c0f20fd42d4b12f10220ea0e0b38`

```dockerfile
```

-	Layers:
	-	`sha256:11f4e9c5302e44e48aae1c8c83b07b5aea56dd3ce50b4579c30631ec279b2cf4`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 2.2 MB (2220813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbea0ab1647050460091db69208766b5e1634106deb08b8f1295ab1d075201b6`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 23.7 KB (23748 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:5f6baf2a631d606ed3525bfa3ddc694277e08385e31bbfecac35de930305d4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73475858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873d8b406d9c001c7d4e76cfd1af56eb1a21a0a91a0f981d8fbb3ebcecb45a8d`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f75b690a5fd55169fbad21a29d8ed315a9d4042c310b1bf6f573673b222fc`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 1.3 MB (1261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c26ba3937fd2b59db15d9b6d2d658d4dd4063b544cfdc5543f937af1ae20ee`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af054951d688ba98eecceef225934514c1bce049b94d72213bb07dbde8fb87`  
		Last Modified: Tue, 24 Feb 2026 20:01:00 GMT  
		Size: 42.1 MB (42074135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639b1a194a41b5d55ce4d7d2ec84ba51375ae840f4a37543134a924795e35a07`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:7260f812f508d008311c945a1b09e2eb009aa3cc337d76a72580e56eac0d43fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577038e6c1f2fd5b16aaf6aece1c6fc7125ca924606fa629f28f008c8b7b8a8e`

```dockerfile
```

-	Layers:
	-	`sha256:c474edcbf3cebe779c0cbb526ca703bbba6b14645d03a7e966a35f28a8dfb175`  
		Last Modified: Tue, 24 Feb 2026 20:00:48 GMT  
		Size: 2.2 MB (2219677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be6e1d99f3771f044639dfe7358743e44a423770a86ba360edde2e87cec9ae09`  
		Last Modified: Tue, 24 Feb 2026 20:00:49 GMT  
		Size: 23.8 KB (23786 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; 386

```console
$ docker pull ruby@sha256:a1a23520e98bc1b8d6bc47d1ca58b686c2f00fa8f52bc18503fb02e1eda0df87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70243142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bc9bcdd54b5b982685b40d0d36cc864c7d42d59c29309fecba98834d92ff7d`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:51:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:45 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a892ff57419277a7fa8ad912b1813f1159602bd6d8068badf5bfb1d62a14993f`  
		Last Modified: Tue, 24 Feb 2026 19:51:53 GMT  
		Size: 1.3 MB (1287332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbea3e8ba0db554c2fac0167ff3e4daf51f3fbd5bc330d7217898dd5c65f7d2`  
		Last Modified: Tue, 24 Feb 2026 19:51:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2d9cc1d12b4edaca10bae974eeb96048293aec72576d8c3e8254d4431ce48c`  
		Last Modified: Tue, 24 Feb 2026 19:51:54 GMT  
		Size: 37.7 MB (37661562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee811540cac1162511fd45e13f42fe19541d1f73c7d8a45b816037c2d0668a`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:ae328c6c2623151902b4e67450c7163cce495ff33919f854182c948f1f5ca69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ade96de9415e535a4774b9041ce4ffdfda37cf2e0258d5b8194e7ebd3b17fc0`

```dockerfile
```

-	Layers:
	-	`sha256:603b4934a274f6c57bd1907895e3f62bda48a587ffb0698bd25075491cae4760`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 2.2 MB (2216576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af74c5b6fa35bada559c37083dc96e5f6731eec108a2f36e0fe4917db98acca9`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 23.6 KB (23564 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:2fb754a2556eca76d793d4256c7b9606939531efe87a5e2f63bb5869e501d1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74429376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fef2ec09a5586a8dcb516da1db16ddce6dfc665826abe304005cd1e6f985f7a`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:04:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 09:04:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6be1f9ad8d9708d6d1dd902519422f937c816172bb2279df8827177290ce2c7`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 1.3 MB (1309384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69016493cd4b81c51b0ebe7726a06117b8c667e58289628f10d4662f959eb918`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae5d6a287ac9deb00e76ee4f5bc8133dfa2ad449e09b28cbcef3715fe45f124`  
		Last Modified: Tue, 03 Feb 2026 09:09:01 GMT  
		Size: 39.5 MB (39519472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9277fefce554077ed90bf6814e28a9db303a96069b78e13ebbb958a92daa6d2d`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:76ada7d8cd9ec6eac64924bee661952be1cbe928bf17857526d76ae972311e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2246609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c0b224bdb43c95568c087707734350ccd1e4ea19daecaf7020ed0c0669e867`

```dockerfile
```

-	Layers:
	-	`sha256:1e2f635a6970e624dfbac554b5c3cf10d1e7c78f02e651f90f37d3677960d186`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 2.2 MB (2222934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f96939f09d3796fa0ff8126bfa5074c55a7ebf5f4438c972779aa088e8a943b`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 23.7 KB (23675 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; riscv64

```console
$ docker pull ruby@sha256:86426f8d8fb11cb89a731aee39cf44ea440c62b616ec97fe631882e60e533d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.5 MB (67484947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc5a132de32f8e603f2dd0c5735cafb8c0e07de9837567d6400b48877f36324f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 13:10:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 05 Feb 2026 13:10:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 05 Feb 2026 17:20:02 GMT
ENV LANG=C.UTF-8
# Thu, 05 Feb 2026 17:20:02 GMT
ENV RUBY_VERSION=3.4.8
# Thu, 05 Feb 2026 17:20:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Thu, 05 Feb 2026 17:20:02 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Thu, 05 Feb 2026 17:20:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 05 Feb 2026 17:20:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 05 Feb 2026 17:20:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 05 Feb 2026 17:20:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 17:20:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 05 Feb 2026 17:20:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf0e976c659ff3ac6c381f4cec5def67d95aa5aef846ea446ecbbd6e774248f`  
		Last Modified: Thu, 05 Feb 2026 15:10:50 GMT  
		Size: 1.2 MB (1247704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8eefa40daebcf4dcc863367436279b9ec1a07b4e3c3b2c23761474e0c24396`  
		Last Modified: Thu, 05 Feb 2026 15:10:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215659df42c822a410e9994afe9a4d05fa2e87855d0dc19ad0775f32f0e58e1b`  
		Last Modified: Thu, 05 Feb 2026 17:21:42 GMT  
		Size: 38.0 MB (37960521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b1d8d47b7c8271e2c230617da76b233be340dbb9a34fba3db007a0c3d0c823`  
		Last Modified: Thu, 05 Feb 2026 17:21:36 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:9e35742d9e47fb6ec2fc973add25b83d443a1d5d84f7b71211ffaaa76edb5a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2237004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e336669ae920676e4c4a98cdde74403c2f39a594b6c572eccb15951595508d`

```dockerfile
```

-	Layers:
	-	`sha256:a04ed1610e27d5291518327d7e2e142715a8ac7fc34c620a0a13ebf6c8e58a42`  
		Last Modified: Thu, 05 Feb 2026 17:21:37 GMT  
		Size: 2.2 MB (2213329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3c3d5ec1ccafd80eda456597c036b7e0770151b93f401a9e2dcc2bc2a0d7273`  
		Last Modified: Thu, 05 Feb 2026 17:21:36 GMT  
		Size: 23.7 KB (23675 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; s390x

```console
$ docker pull ruby@sha256:a67838f789de1e7f8fcc0691c224b2605d164007ca799efbeabe2574e2cc4154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70324474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8138df9402625708a09fc02bc9fed8a105099d58f9f730ebd455c18abc246972`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:53:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:53:52 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0ef58ef1eb78dd947e41fe50adfe7b4ab7ed59de6adb1cee9b213c29193b84`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 1.3 MB (1294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6191cacf2fcbd60736c6c6dd3a35edf5fb265ba19e0504896f4a96d590bdc0`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2e7a1acf75697b829c5674d2af59db59b82bd932f96d1c50df559112643e50`  
		Last Modified: Tue, 03 Feb 2026 04:54:07 GMT  
		Size: 39.2 MB (39191476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27dcf4be1994bc1f0cbe0b29edacbaeb7643532854664d63ed921b9823209fe`  
		Last Modified: Tue, 03 Feb 2026 04:54:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:e23d98216304496ceb84646ecad77e68c8380572a2216da162b956ebfb275b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21862cf5fa5b8fe9dfa9a33947fafd4b17bb19806036827230e46bc7d002f1d`

```dockerfile
```

-	Layers:
	-	`sha256:71dffb8568bdcc5261490b0bc3ba854bcc43cc31538114cdb67581face02f3d5`  
		Last Modified: Tue, 03 Feb 2026 04:54:06 GMT  
		Size: 2.2 MB (2220838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d1e83a521b28fff8ac1553781b86d29079031547455dae45ac5a63c9cfc43d`  
		Last Modified: Tue, 03 Feb 2026 04:54:06 GMT  
		Size: 23.6 KB (23613 bytes)  
		MIME: application/vnd.in-toto+json
