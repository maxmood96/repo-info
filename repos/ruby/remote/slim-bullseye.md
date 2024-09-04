## `ruby:slim-bullseye`

```console
$ docker pull ruby@sha256:7e9d982ad3dbd2840e32e24f728ac66815add651f352321e873af7befe76986a
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

### `ruby:slim-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:59ceaf28f1bfe4a52cc8d58798e5fbd107efc1890a7d6d201beebc627396511a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84096835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1104a96803e2e331fc8bd69d8f724084a39a6ffeef29d0a21d08139cb9d56a2`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:42 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 13 Aug 2024 00:20:42 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ba08c00d78a413c7746920088b3fa2fbf52c4a9679f878c2e0770003d4c464`  
		Last Modified: Wed, 04 Sep 2024 18:01:32 GMT  
		Size: 15.0 MB (14957868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bccadc064c50caa02d7bfead97066c735c994285e0ffe8ceee041b97b500e70`  
		Last Modified: Wed, 04 Sep 2024 18:01:31 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1cec74296c13f5c2226a33757ede2db4a3d88520cc3fae338434895869b106`  
		Last Modified: Wed, 04 Sep 2024 18:01:32 GMT  
		Size: 37.7 MB (37710337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47e9415219902d4a8ead1fa5a2c418721debd7fbdcc84405a6a04e54deaee27`  
		Last Modified: Wed, 04 Sep 2024 18:01:31 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:88d6af59ff7b4924e1d25c6313109b9569373d51c0b2385e4cee9f81aacdef2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c49d07c858d0d07998a26e1387fab45d7e3e1481606b01a993fb7e35676a39d`

```dockerfile
```

-	Layers:
	-	`sha256:96e9d0379ce021d8f584efac47dbd2124e4025ed7be96392806c36ba1be26c32`  
		Last Modified: Wed, 04 Sep 2024 18:01:31 GMT  
		Size: 4.1 MB (4095871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb56ab000ae244752451c783121c0b688db6334732e6f37cf9ac1353c55211e`  
		Last Modified: Wed, 04 Sep 2024 18:01:31 GMT  
		Size: 23.6 KB (23640 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:9229f18ae8cc2c94e869d463f8d27c0b91d6f1ee5041eb3fe49da3dfd81cb856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71240108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f898c532871624e08ed8ca1edbcba4d05e079f61ade80bfe78b00f90ebddc6b`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:46 GMT
ADD file:1f55c970615c481e4eb3e6e0183f67e0ec5ae170e52fb8b39dedb5f312049a45 in / 
# Tue, 13 Aug 2024 00:55:46 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:bc0f52e2f49aece451adc1699e9c837efc588cc5ad1995df66ae64a51b79ca6e`  
		Last Modified: Tue, 13 Aug 2024 00:59:09 GMT  
		Size: 28.9 MB (28930569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2ce6986ddddca72d0ba11915c1e7af06dc0551de4cd7203647137b01a3afef`  
		Last Modified: Tue, 13 Aug 2024 22:33:14 GMT  
		Size: 8.6 MB (8632365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52062f99af72b58fecd387282bd76c460ca58759f322ee7906cdbcde7bfe8979`  
		Last Modified: Tue, 13 Aug 2024 22:33:14 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cbc1c2787cfb263c192216dbbe73f35d466619b60e9e2f77dcb9177344b7cf`  
		Last Modified: Wed, 04 Sep 2024 18:15:15 GMT  
		Size: 33.7 MB (33676833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61300a84dce67d34e233493a77f5699249cd031d8810c61f024ef8e73c7fc894`  
		Last Modified: Wed, 04 Sep 2024 18:15:14 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:0ef748ab9f80310946ed8bace8515e3918ec4800c76c8c4230cccdd40b793412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7971ac0dd23af2f14740af6a4867e8aaae4f73311b595e429b3f7b648816f33a`

```dockerfile
```

-	Layers:
	-	`sha256:9999a24761c058cbd4a5a6f55de593d80d9edf32e58b1f96c9c1437a1852f933`  
		Last Modified: Wed, 04 Sep 2024 18:15:14 GMT  
		Size: 4.1 MB (4065880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85dac7a8ee6a1e538845bde666621e94b7b58f4cb219e3ab33bbf753f4d34cf2`  
		Last Modified: Wed, 04 Sep 2024 18:15:13 GMT  
		Size: 23.7 KB (23745 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:f87d4dece7a27450c1354f9ceb0736f389b56dd9ba9573d7ef6f9201ae5a4405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68315558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1b1dd45b25f45cdee00321194028322883de0f5b05ef1f890d8388cab19815`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:55 GMT
ADD file:9f6a2e97ea42608bfeab22c77e01d6614f64a00a2be04ed1cff9909375d517a8 in / 
# Tue, 13 Aug 2024 00:57:55 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:1a1ab1e12ebdbe1b5383067049fc746bcb9b882bd309b8befaa11c47eed5d4dd`  
		Last Modified: Tue, 13 Aug 2024 01:01:38 GMT  
		Size: 26.6 MB (26589215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802ffecf7de8fdd004205e2e2886b29ac8755b44608e0844d845504f9a91e3d3`  
		Last Modified: Tue, 13 Aug 2024 23:37:03 GMT  
		Size: 8.1 MB (8140587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf779df9ceb2d5914e7f0c04c49ad290ea81fdb989380544670bb80fff29f680`  
		Last Modified: Tue, 13 Aug 2024 23:37:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f7dd0d41d75ac626c52134645302f6c06c7816e95d86576227afbeb2cafab`  
		Last Modified: Wed, 04 Sep 2024 18:16:40 GMT  
		Size: 33.6 MB (33585417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6922070df8404e7470c8878d26f6ef63a6315c14131004972ca6de381f1213e`  
		Last Modified: Wed, 04 Sep 2024 18:16:39 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:0004f818a50861a99ba2d10fe3932d79070a6c78e109222c94612b66f5740ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e209e39efc549675ffacb4f06d8d0f9694de0d77cd96e350a94aa3869158bc2`

```dockerfile
```

-	Layers:
	-	`sha256:48402f1e539ec77a65a4e64d0ce272b17af760226649af8b90cff9e8fd4675f1`  
		Last Modified: Wed, 04 Sep 2024 18:16:40 GMT  
		Size: 4.1 MB (4068644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bab055ae47b1502e950b8d285a47e662732a0f43c96bab71699c52f2e8ab1d0`  
		Last Modified: Wed, 04 Sep 2024 18:16:39 GMT  
		Size: 23.7 KB (23745 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:f0931923fe8aa0722c90f40b92cc26b1d0d0207362afb1daf70131bd165bf43b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76949393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c5b9b6633772c2462803ccf70fc009deb1b91db07003a8ef9f5a24dd2210f4`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:06 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 13 Aug 2024 00:40:06 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65095a76595c098f51a1451e2c982d1c0e0750c252a19da132bddf26deac5c05`  
		Last Modified: Tue, 13 Aug 2024 11:29:39 GMT  
		Size: 9.2 MB (9240144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f0ebbc3a028235105c429f4aa2bcda6f56b873188cdb909f508271962e8b9d`  
		Last Modified: Wed, 04 Sep 2024 18:11:55 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c05f6917568909dc14d4e37e527474a35a87cea0fd83dbab67dba4c19edaea`  
		Last Modified: Wed, 04 Sep 2024 18:11:57 GMT  
		Size: 37.6 MB (37632817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34cb9083eb40e4e73ef1545c113cdfa5a2da4fec1f8b9971581420dc5d64bb8`  
		Last Modified: Wed, 04 Sep 2024 18:11:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:9f256b07a1fbc28eae720478cefb5a0d5aa97ed79e85c02f6fa13f5a18485eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ffcee2be59ca577c60692807e6a1c038582fe550210ab591590d86d9d764d0b`

```dockerfile
```

-	Layers:
	-	`sha256:5d4795916ffdbf6a5e02688c7dbed92b0bd60a8bd2e9e0f45267a196b3baa1ef`  
		Last Modified: Wed, 04 Sep 2024 18:11:56 GMT  
		Size: 4.1 MB (4069036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d35155e7e0e56ba16a181423e1868dd22c9919f479ab334a826fd580a6df7bb`  
		Last Modified: Wed, 04 Sep 2024 18:11:55 GMT  
		Size: 23.9 KB (23945 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:49a9507afaf7944dfa451233b43b5eb734bc4c6c93b77150efa2bfa753459878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.6 MB (82559294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5064a15241b5537760dbdf64a5a337df4376fd8062c5e050742eab02e64a7fd`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:18 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Tue, 13 Aug 2024 00:39:19 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1caed024edf4a6a8cf2773d4d4e7e10b3120cb5b0161660eb22213feff221d`  
		Last Modified: Wed, 04 Sep 2024 18:01:18 GMT  
		Size: 16.5 MB (16501675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26fd3092e49d76fc583877b57955579380d69fe26bd8101fb732775b79d5f984`  
		Last Modified: Wed, 04 Sep 2024 18:01:17 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bc5e86dd51422a7b7dfaa44088cfabf0032bcf67dd92298963507277d9d587`  
		Last Modified: Wed, 04 Sep 2024 18:01:18 GMT  
		Size: 33.6 MB (33643492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6557a4b92ec0cee1a5194eed8a7f79c1c48f1b8a691fa7cd9981b293fe6b5244`  
		Last Modified: Wed, 04 Sep 2024 18:01:17 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:e456be99c93a57c13ef9b92ea0fb9a1648eb65006e1fe54e5ddfaf367f034b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bf9481e75aac4ab8241e619072bcab4e06f670ae806a802315047ef57d5b07`

```dockerfile
```

-	Layers:
	-	`sha256:72d374204608354572a00f4dac8ce7b9aabba9a33a65041505ef48b3f0f8bb34`  
		Last Modified: Wed, 04 Sep 2024 18:01:17 GMT  
		Size: 4.1 MB (4100073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283acef8a105975051c7a914211713ae208899847fe9116bb61f14e508be0744`  
		Last Modified: Wed, 04 Sep 2024 18:01:17 GMT  
		Size: 23.6 KB (23605 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:25dc958819205798d0d24f49b9bfd0088ff4b213a9265e376927a331ec790a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74628311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e991a334023a3e0cf29bf703f2ac8c60c364ea4016da6fad583274694eb8c6`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:12:29 GMT
ADD file:d4b92daa2701c7af077c4c89b2b1f5a97cfc6389c09e049b3bdaa36454653bbd in / 
# Tue, 13 Aug 2024 00:12:34 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:15b8bd5d9ec350cbe23bbccddd5284b3cc9139e037500a63a02025354518d5c8`  
		Last Modified: Tue, 13 Aug 2024 00:23:52 GMT  
		Size: 29.6 MB (29646095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07033608e804547e67486b9091c336a7566d60f27ba5af107924484256b3c88`  
		Last Modified: Wed, 14 Aug 2024 18:56:31 GMT  
		Size: 9.8 MB (9833691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283b71c75074d7c9ab8ba7b96a17aefc4012a4cf1a5de51034d3c55d5c3f322b`  
		Last Modified: Wed, 14 Aug 2024 18:56:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ec1d363d6e985d89f5701e6419d9cc62d7b7f6a07f72679dbd1fcec46db3ea`  
		Last Modified: Wed, 04 Sep 2024 19:06:28 GMT  
		Size: 35.1 MB (35148184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740ef79585a022a24051563a2a0bcd5b701cc02656a0c7d054830b7923314833`  
		Last Modified: Wed, 04 Sep 2024 19:06:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:42eeea41f27aa732bd437b88b26720af02a421c15d9f36de54a1b746aa607550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 KB (23483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad890abbbbd068799f2811b75da2a941c531699cb81ecef5c32aaa8888deb6a`

```dockerfile
```

-	Layers:
	-	`sha256:876db02586f423fdfbe5229fb62955352012ffe7e0fcf24c88ef0289eab34df9`  
		Last Modified: Wed, 04 Sep 2024 19:06:24 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:a9d730cbc9626506824628c09b9c4c62a33b0166c32a05261f5558ab23bd608a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81256771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f4cf74cb13da05e712bb3e1bfc9b8d2311efdb6fc3692401331c2d67b268824`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:31 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Tue, 13 Aug 2024 00:22:33 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d057b2c883aa3a33aa2a62665c02cea10c37d6c57295e3d23da6d27c85ac024`  
		Last Modified: Tue, 13 Aug 2024 12:22:06 GMT  
		Size: 10.5 MB (10479764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4d66d147231a468cc1446004ad12f8e6300d1dbd8fbccf8d690b7105d949d0`  
		Last Modified: Wed, 04 Sep 2024 18:17:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c7d77b27dc13495a27b61ffb34ed57c9e39810690f231fd5841242b3eb278e`  
		Last Modified: Wed, 04 Sep 2024 18:18:01 GMT  
		Size: 35.5 MB (35471531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf521a6029ab9d2adcd3e264b5dd4092298ce36669c7135795f12cd82cf7220a`  
		Last Modified: Wed, 04 Sep 2024 18:17:59 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:d4c4e77698dd13354c49743cc576d7f85badba2679a82e5ee87e7fec7765c18c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f617ff2e66779073db76bdfa6474ec0b55f2df2a908fadb8ba55f044eeddb61`

```dockerfile
```

-	Layers:
	-	`sha256:c507f7d30b6502c726487252d12c481833f8e199cd49c04945a0821e474ab6dd`  
		Last Modified: Wed, 04 Sep 2024 18:18:00 GMT  
		Size: 4.1 MB (4083544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2115a62bc6cf4c384e07a2fcc55484a15d3431a9328fe8f956fd6b097e518368`  
		Last Modified: Wed, 04 Sep 2024 18:17:59 GMT  
		Size: 23.7 KB (23684 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:d08ee1d505eaeffe23d9d18e970f4693fc591308fbefdcbbf702a7af30645203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77809333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a731531f3cc6ca01351f5695818e8974ffcc980e0bb7a80ca6a7a3b1a1a983cf`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:43:12 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
# Tue, 13 Aug 2024 00:43:13 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fde3aae48926bef55b3a2a91cd3c13765b158530780ceeaea61e29f2b256617`  
		Last Modified: Wed, 04 Sep 2024 18:17:58 GMT  
		Size: 13.1 MB (13054149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f12737f4d28c54d267b7b42b40d3b578eb1890989e9a235dfd39121e3c15566`  
		Last Modified: Wed, 04 Sep 2024 18:17:58 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077d6ad4e98d2b1790d04e2b38ac7d1c1ad8d6e056daeb54dd3338eb370c511c`  
		Last Modified: Wed, 04 Sep 2024 18:17:59 GMT  
		Size: 35.1 MB (35085876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ddb0538b557799e6a496d0968f5a696c51b89386bd3b184748c953f713d02b`  
		Last Modified: Wed, 04 Sep 2024 18:17:58 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:7ca55ffcb769e2ab41beb1f83c0a4e330fff1ae7ff51da4e9567c133831f4a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4108190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6128c3f8ae8f003ff2429c22e0c7765a12f2339093a545825acfa0084668075`

```dockerfile
```

-	Layers:
	-	`sha256:5cf859a9c6583540f693b40f462d459919cb15e0ba63721c1d2d2402223e0f12`  
		Last Modified: Wed, 04 Sep 2024 18:17:58 GMT  
		Size: 4.1 MB (4084550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01327c8f82909ec109f36dec8cb42f4c8adacc9e36a4c692f4f25c8228342d6e`  
		Last Modified: Wed, 04 Sep 2024 18:17:58 GMT  
		Size: 23.6 KB (23640 bytes)  
		MIME: application/vnd.in-toto+json
