## `ruby:3-slim`

```console
$ docker pull ruby@sha256:4d611590cb3dc3211dc2e42c87347970c0ae9f7ad9c3db17a121d5996296f8ff
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

### `ruby:3-slim` - linux; amd64

```console
$ docker pull ruby@sha256:30316d9643f743da6ecc0f5dba53b38a95f00bc11bdc13dd8cc1d52c280ec211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79087398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a86bd551d4670b80418f8e355ee2429185d3ab430a0182cc25550dcad9a6dea`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e1e64c0260323cc3d99a8927d5ecf7bff2f32154352f1822ff9990ee9c0b98`  
		Last Modified: Thu, 30 May 2024 23:59:50 GMT  
		Size: 13.7 MB (13657856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5eb91e4185f23c6e7b0ec5f31a6784a64d736cf0805370cdde3d2e50f12294`  
		Last Modified: Thu, 30 May 2024 23:59:49 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2c80134e4474ebe0bc3797dda3197f0eff056d00b523590c66733109c794ed`  
		Last Modified: Thu, 30 May 2024 23:59:51 GMT  
		Size: 36.3 MB (36278790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4645d3b7b2fcfef3562129e10a283e0f951a4b1d8b403f497305a877f0015f0`  
		Last Modified: Thu, 30 May 2024 23:59:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:e8cd2ea0779548783481793f6ef4cfc4cc792cc890d0126ec38a0ddb56dd0f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3887527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079a4d0b1c6aa8beebd582e45ecf19163a919ea5a6376c555561ecf651ae2f4f`

```dockerfile
```

-	Layers:
	-	`sha256:81c16a1fef79fd30c0fb1bf13600d33aa0caf922f7e1b0e73bd7ec0028d22f52`  
		Last Modified: Thu, 30 May 2024 23:59:50 GMT  
		Size: 3.9 MB (3862873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cad80b4479e4f40ce6199f28d8820bd9abe081149dfd05b7b9d98f2f11b44d`  
		Last Modified: Thu, 30 May 2024 23:59:49 GMT  
		Size: 24.7 KB (24654 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:4980e1555a2128a48eb3a072305d74d4ee589f90084dd819a7ced81877bd1946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71038789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15019a28f910988fed3486853ff54c2aa940758f151b98f67b144a7db60fbbe1`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:48:34 GMT
ADD file:ee9f1914c7fc370bdb089c9e2fcfa15477f7091fc5437cb780232afdf6297586 in / 
# Tue, 14 May 2024 00:48:34 GMT
CMD ["bash"]
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:169fcae2368e5a601c42972560f091e123648fa0e741975d1b35900c61b9ff71`  
		Last Modified: Tue, 14 May 2024 00:51:36 GMT  
		Size: 26.9 MB (26909921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc0d863e1cea9a17dc904ca5a6d61bfea1a1e2223fcb1515dd50bf17c949f59`  
		Last Modified: Wed, 29 May 2024 23:17:12 GMT  
		Size: 11.4 MB (11414771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce3639de2ba35b8eecc033252bda9a1ada8db3da13a1c04a7d129bfc778a5b7`  
		Last Modified: Wed, 29 May 2024 23:17:11 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee4c0dbe58ae6145dda0d8b2c61ae1036212ab19ab8c2b122d9ba5a23abee7c`  
		Last Modified: Fri, 31 May 2024 00:07:41 GMT  
		Size: 32.7 MB (32713755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef11c23692d961d506d746eebcfe7e63499be265d16aa8c289aa57b4a46a68f`  
		Last Modified: Fri, 31 May 2024 00:07:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:08a6812773cb7f7974fd93e76d4e1c937129f635cc732d2b26f85b60d3119566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3857966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff8faa5209ef9aebd84463293a14fb6eb12e236d680ec24a5f95e37211862bd`

```dockerfile
```

-	Layers:
	-	`sha256:639655a2624380831a78123a7c0acaf113a0c4046eff6c19a64941e4be9d5870`  
		Last Modified: Fri, 31 May 2024 00:07:40 GMT  
		Size: 3.8 MB (3833171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c78f588580feed04efb8407c73d73725f2d7e29a39c92402479c1ec14bf22952`  
		Last Modified: Fri, 31 May 2024 00:07:40 GMT  
		Size: 24.8 KB (24795 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:32090737ecf3ab4ffdab60f0b75ab5bd7e4f4809da8312cf24459aa14b30e14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68082611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0706755243260e5dd7c97095cf5483a29a7f6987c5af3c76a4745df90d2b17da`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:08:45 GMT
ADD file:e170e8e24c36eb1a1a24d68a97cd2a7784d689387d804630dc7b596551d91090 in / 
# Tue, 14 May 2024 01:08:45 GMT
CMD ["bash"]
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3b9aff019fd47145a0f08828c4c912b901596e71f6dbe2367a7a098e8882ef55`  
		Last Modified: Tue, 14 May 2024 01:12:45 GMT  
		Size: 24.7 MB (24740205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c8065f009e859df72992de63fcb275d3c91a7eaeff8f66368e22b4acce59dd`  
		Last Modified: Thu, 30 May 2024 03:40:25 GMT  
		Size: 10.8 MB (10753078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f7e398abf78de4e05a9cd12d3a58ab932d390ce40cf407d06ac8ff814f4883`  
		Last Modified: Thu, 30 May 2024 03:40:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe34fb1911e09ebf9001488dbb78c58dd2277f5d950fe4746baecfcea30ed80`  
		Last Modified: Fri, 31 May 2024 00:44:39 GMT  
		Size: 32.6 MB (32588988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78bfdd244ed7efa480b377dabfffc9c20118daccd5b8504ba85c7f9885f2a45`  
		Last Modified: Fri, 31 May 2024 00:44:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:4be69c41da5ae36d4da1b3f137919d9b9e2f657374e353262e9767d7a6b83b35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3857761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b276eea70367e902439b960da25465b8714eb9030b029d5ecfe7eef410f07bb1`

```dockerfile
```

-	Layers:
	-	`sha256:9699a00b17fec1e25f159575c4c442e055423062c959c2793996a9de8c8b7960`  
		Last Modified: Fri, 31 May 2024 00:44:38 GMT  
		Size: 3.8 MB (3832966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8ac689df9ebd5d5bf708225c0f6d5efa0c393d59228a8347732bcdcf42fd2e7`  
		Last Modified: Fri, 31 May 2024 00:44:38 GMT  
		Size: 24.8 KB (24795 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:9e20d87fc90b12696b53c4df65ce801abbe4967fcd2b1667caa7e2f6ecca1ad3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78003092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7faa7b9a720c6edc373fd8a6aab3ebaf6c52b44e6b1bb2a0c9ec6dbfcdd92c53`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bdf007984198d16122b3af870a2fb93855d99d52d93747046405f9c0a88bb1`  
		Last Modified: Fri, 31 May 2024 16:37:22 GMT  
		Size: 12.5 MB (12500254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a06b777816135b7ba317c55b9783d6b383e08fd1181bff331e54f501a204002`  
		Last Modified: Fri, 31 May 2024 16:37:21 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aad556af4455c1d2043028bcdb8b9028028446031ed22eafa0efebf4612ccaf`  
		Last Modified: Fri, 31 May 2024 16:37:22 GMT  
		Size: 36.3 MB (36322994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23fa971999c8ea03a7d0d5bdcc415d9dad9de9361430c6b55bd010a9397a86b`  
		Last Modified: Fri, 31 May 2024 16:37:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:1bc2822b01c190c5259c584d51f86cc11454fdc4d8c03184b33506f4a03200fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3859149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bea9e0a4d016509b5d7b920c811574171f7c37fe9e723ab90d2d54c45f251d`

```dockerfile
```

-	Layers:
	-	`sha256:6b2278fba8847d77b0280751446ce02d692b0e1636cee807f103d04a8d574ca3`  
		Last Modified: Fri, 31 May 2024 16:37:22 GMT  
		Size: 3.8 MB (3834138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de33fee159430d1ff2e5317dba7f11998f03f0e1c56f78bcd99c3c423c8f3f0`  
		Last Modified: Fri, 31 May 2024 16:37:21 GMT  
		Size: 25.0 KB (25011 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; 386

```console
$ docker pull ruby@sha256:38ed562d095d6af26562d0eea17a44c8477550e986fd1c2bec401da32d19281f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75882266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc217c038cfa98a5fb7e9442317eaad4ea8633c6f99e4ba860929cbc12526b34`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:47:12 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Tue, 14 May 2024 00:47:12 GMT
CMD ["bash"]
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f568491bfffc7e6075102a469d9695d859eeb099391e34dbc51b1c0390c6a86`  
		Last Modified: Thu, 30 May 2024 23:59:35 GMT  
		Size: 13.2 MB (13207799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a435cadc4669f8c4b13b8d1cedcf7b0971343b3d89f21f7d1b77dd1a0f82dc95`  
		Last Modified: Thu, 30 May 2024 23:59:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1da2ba4574b0a8fe82201b4a65d8f7f1bf38bab6251bdb79d2dff088ac50d3c`  
		Last Modified: Thu, 30 May 2024 23:59:36 GMT  
		Size: 32.5 MB (32511489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa696053400d802f63d6c9d9d98f67f52894df7872c1d1a060952e73028a64f2`  
		Last Modified: Thu, 30 May 2024 23:59:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:9a59adb6f50b8be3fd48af59192461ad2bdea9b832c9ee166c56e5284b6b4dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3881310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b837eb42917634b0e67343111adf628206909213de8ba82778faede6271f6548`

```dockerfile
```

-	Layers:
	-	`sha256:76398280b3bd604552a2ef49c411407a66001c3f65f631643543dba285636bac`  
		Last Modified: Thu, 30 May 2024 23:59:35 GMT  
		Size: 3.9 MB (3856711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9aaf34a7e2f2af9f650a80cf5d0889f7639aae55641e9e71ace3edfacf64c3f0`  
		Last Modified: Thu, 30 May 2024 23:59:35 GMT  
		Size: 24.6 KB (24599 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; mips64le

```console
$ docker pull ruby@sha256:d6f11fab1e2dbc048bf259605bf55e9b0c3c580434d1d86e751ddad9a6f0526e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75555563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de85643ccbf064f3719280c4309f0d9f1cca313ea2556251339a9dd8e66ba27a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:11:07 GMT
ADD file:a92da94a28279478b2eae11dcdcd2913fc06af02498a5515cc3f288668d74e43 in / 
# Tue, 14 May 2024 01:11:12 GMT
CMD ["bash"]
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6ccc6628d3cdcda935b3b60cb54fa578d669965454d9cf39de3df9c1276132b7`  
		Last Modified: Tue, 14 May 2024 01:22:19 GMT  
		Size: 29.1 MB (29143688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fca084acbdf23d646962c97074f6292846770337152770afcf9f2f474776110`  
		Last Modified: Fri, 31 May 2024 02:28:46 GMT  
		Size: 12.7 MB (12680079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cf74322e0c6d344c6626808ed1c2ad920739dc6b22d82fa13f05439432d0dc`  
		Last Modified: Fri, 31 May 2024 02:28:43 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10082c0b384145c04e4a935af44c72f75f77e49ee32d1cbc65dfb3d841bc53d7`  
		Last Modified: Fri, 31 May 2024 02:28:47 GMT  
		Size: 33.7 MB (33731455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b75a414cc6d88a7f0f71cb62e4673653f9d0965cd712319dddd8a78974069c0`  
		Last Modified: Fri, 31 May 2024 02:28:43 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:0cafaa6c5c1e7333554b160e4717e996e249b7b0150063f7c684e90692cdd042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 KB (24537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1895d7f19d08a71d5114e13fe0bfed7665a28c69d5f6f38bbd148018c55b798`

```dockerfile
```

-	Layers:
	-	`sha256:c1d2583fa77219314494486a51e25ce29525c21177cf913f5c66b0376860cc67`  
		Last Modified: Fri, 31 May 2024 02:28:43 GMT  
		Size: 24.5 KB (24537 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:016e7b58295f98d5e8a59631a80f1667abff4b987d26602ce6c02b608e12560a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81627942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5b9c5d70a11870aa01a444f7e69d42f09600f3c1bd89f785511990813fb03c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:20:02 GMT
ADD file:1622c3287b5a5c8a6e0b0b0180489212aab2c9bc7b43390b17a5cc8b153e542a in / 
# Tue, 14 May 2024 01:20:04 GMT
CMD ["bash"]
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:11ee2a6dbc4a6a6b182097f6023f775e595488a6bcc424e9b58001659deb7fa1`  
		Last Modified: Tue, 14 May 2024 01:24:06 GMT  
		Size: 33.1 MB (33141160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8df8f7a7ab53bd12e50659cfa5485e9ad01378bfe00268020c22fb0c1c573c5`  
		Last Modified: Thu, 30 May 2024 03:24:20 GMT  
		Size: 14.4 MB (14379694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ced3e50fbb60a005c54e48064e67785e58584efc4fb8ac34fc587e0f21566ac`  
		Last Modified: Thu, 30 May 2024 03:24:19 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60202256a661016ee30a583717fa650ff50c9339097156512c57f1cbe0e5a18f`  
		Last Modified: Fri, 31 May 2024 01:45:30 GMT  
		Size: 34.1 MB (34106747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3728131a29302a3bafc5c671f8552f0e874e699fc2088d389cf11420f1d4e6`  
		Last Modified: Fri, 31 May 2024 01:45:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:f90bf5eeda6b21c10479d173b7bbac2ca8d52aa68b31ea558611c6c94e55121e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3873418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f297b454948916de56642df632274ac501aba85ff4746e1bf425b8e9062a4162`

```dockerfile
```

-	Layers:
	-	`sha256:f2c290c3247baf72d0a98accff764cb73ca8977bece981b7d398b8d0cbfa626a`  
		Last Modified: Fri, 31 May 2024 01:45:28 GMT  
		Size: 3.8 MB (3848696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30e867a5fee3d91d86cf2aeb81935f18053e11b921cb1e2002fcf1b2d89dd551`  
		Last Modified: Fri, 31 May 2024 01:45:28 GMT  
		Size: 24.7 KB (24722 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; s390x

```console
$ docker pull ruby@sha256:ba7cfc8dcf082eaed3e85b897f34999240fa60c503f05b9d34ac2faa0dfcb793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72702791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628170b557e949358850de789e416f39298dc9a65cff944265867db0706b94a6`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:42:38 GMT
ADD file:55fef93bbad6701fe968a070a0c72b3a0bd3df408dd79c9a616a43dea0de11d0 in / 
# Tue, 14 May 2024 00:42:40 GMT
CMD ["bash"]
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_VERSION=3.3.2
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.2.tar.xz
# Thu, 30 May 2024 05:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=b5e8a8ed4a47cdd9a3358b5bdd998c37bd9e971ca63766a37d5ae5933fdb69f1
# Thu, 30 May 2024 05:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 30 May 2024 05:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 30 May 2024 05:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 05:03:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Thu, 30 May 2024 05:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d7365433874e83ccc92aa5d768989641a64e23c3247409161401a09b4895c406`  
		Last Modified: Tue, 14 May 2024 00:47:35 GMT  
		Size: 27.5 MB (27512398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32912cba28e8556ac93ba58ce8912b77f9999bb1cd901683ec344723c3d6b2a1`  
		Last Modified: Thu, 30 May 2024 01:38:58 GMT  
		Size: 11.8 MB (11832531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a9ca50dc30f1c056991d42b8025be4a5e5c94171957ca0d19ff13ba52b20ca`  
		Last Modified: Thu, 30 May 2024 01:38:57 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c88851876b030d68b2e324f0fa50d71142f7d6f2479da3cb4ed1276f27bf21`  
		Last Modified: Fri, 31 May 2024 00:52:30 GMT  
		Size: 33.4 MB (33357520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa80909eea866d75fc3a6a8e76ebc9e87dc8c24d9e81fa98c731e9656beb1911`  
		Last Modified: Fri, 31 May 2024 00:52:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:14259e08a255df685a7eaf7a932a1e2f61216594dc7c0c81c163e34a2b4d9cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3875777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c32095731c6fa3a03c5fedbc161c4c1f325f881e375e74665c7200cbb3328bb`

```dockerfile
```

-	Layers:
	-	`sha256:effbf25aca3520b3d90665c7cf140199c249a1bc10cae89492ed18e6249a96f5`  
		Last Modified: Fri, 31 May 2024 00:52:30 GMT  
		Size: 3.9 MB (3851123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:479d508b5d4972a718b9df386d905465c8580f339ff01bf33943138db2149e26`  
		Last Modified: Fri, 31 May 2024 00:52:29 GMT  
		Size: 24.7 KB (24654 bytes)  
		MIME: application/vnd.in-toto+json
