## `ruby:slim`

```console
$ docker pull ruby@sha256:b423de1def93f6bb6d18681e04ec2ca17725ec2d632893e2f4b14c133ddbf6e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `ruby:slim` - linux; amd64

```console
$ docker pull ruby@sha256:c85f17b4fbcaaa6abdd1eeaa7002c18619ebf2f8775524487ed2406eb8f53cca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (75989177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230459e7cf72b323eb84aaadba1c281cdc3bdd705dafca05740b602d949f328c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 19:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 19:08:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 03 May 2023 19:08:49 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 19:08:49 GMT
ENV RUBY_MAJOR=3.2
# Wed, 03 May 2023 19:08:50 GMT
ENV RUBY_VERSION=3.2.2
# Wed, 03 May 2023 19:08:50 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Wed, 03 May 2023 19:11:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 03 May 2023 19:11:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 03 May 2023 19:11:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 03 May 2023 19:11:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 19:11:33 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 03 May 2023 19:11:33 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201ffa30101754210c7fbca23d2147904756a96e7f8d9754f6db4bc31580083c`  
		Last Modified: Wed, 03 May 2023 19:42:49 GMT  
		Size: 10.0 MB (10023164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaf5502212fbe68d4ac640762fb12d59af0868a4cd48fb88fd3e7612d79c165`  
		Last Modified: Wed, 03 May 2023 19:42:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fac5d79fd01fd7c79f3738270733b402ad10bdbc9b39486e7780b00d4a28275`  
		Last Modified: Wed, 03 May 2023 19:42:50 GMT  
		Size: 34.6 MB (34562122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6f20d4cfe8f5cef5e4125ea488b8a3ec54e158795fc95957828ae237167cef`  
		Last Modified: Wed, 03 May 2023 19:42:47 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:6796e95a59181c87bcc017ba3f521b3da95004a79de7e097996066e03e3d9007
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68025267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f8fdb1552540470150845918630e1b390582cf906bebf3b1c9baf84e6b287c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 May 2023 22:48:53 GMT
ADD file:ca82c0d9094c1022a00b5f2157a02e1a9032aafc357a41c76c6b60bd74d25395 in / 
# Tue, 02 May 2023 22:48:53 GMT
CMD ["bash"]
# Wed, 03 May 2023 11:47:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 11:47:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 03 May 2023 11:47:12 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 11:47:12 GMT
ENV RUBY_MAJOR=3.2
# Wed, 03 May 2023 11:47:12 GMT
ENV RUBY_VERSION=3.2.2
# Wed, 03 May 2023 11:47:12 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Wed, 03 May 2023 11:49:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 03 May 2023 11:49:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 03 May 2023 11:49:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 03 May 2023 11:49:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 11:49:30 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 03 May 2023 11:49:31 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:eb6ee5d3f82142e70aca665cea92048b1a46ff1aa5c5be47a04c27a471470c07`  
		Last Modified: Tue, 02 May 2023 22:51:25 GMT  
		Size: 28.9 MB (28903418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2520c96d75b8bbb8ca7b74094ff4ee8c41cf536df6bac998b01db4bd0935efe6`  
		Last Modified: Wed, 03 May 2023 12:03:22 GMT  
		Size: 8.6 MB (8634343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cb808d1e8f9d1f674dfe2463dc61ac8964cca0d926c771ef50a5b0d9a35ecb`  
		Last Modified: Wed, 03 May 2023 12:03:20 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df8fa599426003e9a31b88bd3b1931a7f0a314c5e4f09449a9d3f78a707f2277`  
		Last Modified: Wed, 03 May 2023 12:03:24 GMT  
		Size: 30.5 MB (30487133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338a4830c86e9cad46b32e03f3e475f043d1ceb1b8a1e94c0cc54146db627d32`  
		Last Modified: Wed, 03 May 2023 12:03:20 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:6c83cef5a91168e3a7acf685cc42f7dd40ae9e7f01aef4abb68acf1b5a61b495
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65087458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c2b4dfeea5828e961dcb68e9a7af6a97d35fb62cff8879eeacade64966c38ef`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 May 2023 23:47:57 GMT
ADD file:69d82e947b50a0f0ec610822ffe7c23ec1f6eb41bc17068502380f827cbcce40 in / 
# Tue, 02 May 2023 23:47:57 GMT
CMD ["bash"]
# Wed, 03 May 2023 15:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 15:04:30 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 03 May 2023 15:04:30 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 15:04:30 GMT
ENV RUBY_MAJOR=3.2
# Wed, 03 May 2023 15:04:30 GMT
ENV RUBY_VERSION=3.2.2
# Wed, 03 May 2023 15:04:30 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Wed, 03 May 2023 15:06:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 03 May 2023 15:06:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 03 May 2023 15:06:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 03 May 2023 15:06:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 15:06:37 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 03 May 2023 15:06:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9c7c4e67baad3ce38491ce8c1ffaa9ca9ce37409270ce53ab3472054f35d097e`  
		Last Modified: Tue, 02 May 2023 23:51:30 GMT  
		Size: 26.6 MB (26564648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b4d9291c9933451d8b76290c3e6931085c6d07e8b924df3ca7adff5bf6c57e`  
		Last Modified: Wed, 03 May 2023 15:34:16 GMT  
		Size: 8.1 MB (8143782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0fc957833ebe20d5c94e0eb971e265ab56116e4317427dea0623899524f1503`  
		Last Modified: Wed, 03 May 2023 15:34:15 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76d87367d0780b28bbaf540fef45409cce8721b3932353b07798cb08ebf7e27`  
		Last Modified: Wed, 03 May 2023 15:34:18 GMT  
		Size: 30.4 MB (30378655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e423fc8ce3d3aa9aa33dc666d1e23215c0ceee6d70545906f03d1dbaf0fabe4`  
		Last Modified: Wed, 03 May 2023 15:34:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:ac9cabe390be6f64baba0a0cb436c0d0b4fc73d2aaa1fb2a44f9bff0e27e1bff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73743764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb511b54db1b1dfcf3654b6358984930bc84a5fa9011e4d61a4f3ca9f5b030df`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 11:33:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 11:33:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 03 May 2023 11:33:36 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 11:33:36 GMT
ENV RUBY_MAJOR=3.2
# Wed, 03 May 2023 11:33:36 GMT
ENV RUBY_VERSION=3.2.2
# Wed, 03 May 2023 11:33:36 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Wed, 03 May 2023 11:35:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 03 May 2023 11:35:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 03 May 2023 11:35:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 03 May 2023 11:35:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 11:35:40 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 03 May 2023 11:35:40 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c1531f71db6b0a18949b875d88c4e89771d1f342242ace07be465eaf823657`  
		Last Modified: Wed, 03 May 2023 12:00:18 GMT  
		Size: 9.2 MB (9243388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09062a3cd32c5e4b240a84c6d1b7286f252e13dd31c44688b8ef1fc66feb47ed`  
		Last Modified: Wed, 03 May 2023 12:00:15 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5cd9a9e48cb2019bf1d8cff9ffbac5150e26acb0cccbe1b7860ebe927cfeec2`  
		Last Modified: Wed, 03 May 2023 12:00:18 GMT  
		Size: 34.4 MB (34447268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8492d62e395409e95b38143f3f472a5c1efb722f9eada4d5e816a217cbde21c`  
		Last Modified: Wed, 03 May 2023 12:00:15 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim` - linux; 386

```console
$ docker pull ruby@sha256:33feef5e7d3fa2adee6acec11ab4986205756a8c1ed3dd371bf460e6398a9c99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74839631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c1d46fadbb3a48dd59738e524c3681048a5b7084ac1634db81ae32dae51776`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 23 May 2023 00:39:30 GMT
ADD file:8319fc1c1a3c0f2a6bb03636fe1fd0eb7fa52c58505d279e4366627452ea2104 in / 
# Tue, 23 May 2023 00:39:30 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:12:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 23 May 2023 01:12:04 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 01:20:43 GMT
ENV RUBY_MAJOR=3.2
# Tue, 23 May 2023 01:20:43 GMT
ENV RUBY_VERSION=3.2.2
# Tue, 23 May 2023 01:20:43 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Tue, 23 May 2023 01:24:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 23 May 2023 01:24:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 May 2023 01:24:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 May 2023 01:24:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 01:24:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Tue, 23 May 2023 01:24:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0f5d158483bd0ffef0c106b68514aece2ca0500d2990c830844277cbca7fe0bc`  
		Last Modified: Tue, 23 May 2023 00:44:28 GMT  
		Size: 32.4 MB (32388165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f5e573e66fa2cd19b7052169187d24733be9d6d250dc8898046d0fea6cd049d`  
		Last Modified: Tue, 23 May 2023 01:43:19 GMT  
		Size: 12.0 MB (11997370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35afa18cbcba46f8516124b77bcc5ade8c55162dc60d023b4302c72e9cb40e08`  
		Last Modified: Tue, 23 May 2023 01:43:15 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b0c57b6292ed23675a7061e3f31c7817b16ccea26842bbd5daebedb54573a`  
		Last Modified: Tue, 23 May 2023 01:43:53 GMT  
		Size: 30.5 MB (30453719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ffce46134166cc892cf9d1461231da89357c03ec22d8ac9cdb975f94beae9a`  
		Last Modified: Tue, 23 May 2023 01:43:49 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim` - linux; mips64le

```console
$ docker pull ruby@sha256:2f3e99d095d879ae2ee2e00e1139cf8d7c3c13eb92fe133c9d2e47acd9de30d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70879316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e452c684c5260baa1492cf757ada64381349527310cd2a23903f240a6444dd`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 02 May 2023 23:49:45 GMT
ADD file:c3427ec4e3a2c988fdd372b529660d45ee105e317d6a964ce96f8f9009a3c21e in / 
# Tue, 02 May 2023 23:49:49 GMT
CMD ["bash"]
# Wed, 03 May 2023 22:56:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 22:56:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Wed, 03 May 2023 22:56:58 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 22:57:01 GMT
ENV RUBY_MAJOR=3.2
# Wed, 03 May 2023 22:57:04 GMT
ENV RUBY_VERSION=3.2.2
# Wed, 03 May 2023 22:57:07 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Wed, 03 May 2023 23:10:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Wed, 03 May 2023 23:10:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 03 May 2023 23:10:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 03 May 2023 23:10:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 23:10:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Wed, 03 May 2023 23:10:22 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:498edd615f8781385e0d5246e189d80b5caceb207fe26608a12605d0a823d4df`  
		Last Modified: Tue, 02 May 2023 23:58:10 GMT  
		Size: 29.6 MB (29623482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3810d4d0e884eadfc61a26d977e016037851a041463e04b1e28f0bbb1311d0`  
		Last Modified: Thu, 04 May 2023 00:20:10 GMT  
		Size: 9.8 MB (9836646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95cccb497ad41cb6df018855db1850c2079aaf59040b230d2da8fe19ce09a126`  
		Last Modified: Thu, 04 May 2023 00:20:01 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e4d6a2064ac7b96cef3b2ec5dd55ad2f597ade5935633d195ae0d929ae15b3`  
		Last Modified: Thu, 04 May 2023 00:20:14 GMT  
		Size: 31.4 MB (31418847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9b693e3b7b1b27061275fbcdb30f226604b7dce1deeb0e2404fee9f0956222`  
		Last Modified: Thu, 04 May 2023 00:20:02 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:94007bfaf48fe7068bd29bbb659af0d6574227b6d631e19ed55312957f92744c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77802694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495f93fab3e5cbeccd9a3e5103147559dffbcb4d6a013a126e8e084de1f0e0f6`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 23 May 2023 01:17:35 GMT
ADD file:719aea085739ec41c255f35070ca652d4e356c5ee62c8237f8ebc7389feb8e38 in / 
# Tue, 23 May 2023 01:17:37 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:23:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:23:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 23 May 2023 02:23:32 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:31:38 GMT
ENV RUBY_MAJOR=3.2
# Tue, 23 May 2023 02:31:39 GMT
ENV RUBY_VERSION=3.2.2
# Tue, 23 May 2023 02:31:39 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Tue, 23 May 2023 02:36:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 23 May 2023 02:36:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 May 2023 02:36:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 May 2023 02:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:36:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Tue, 23 May 2023 02:36:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b6c83d2f160e7e38990586d26caa105ff577368a887fd754ae4634cdbfec83ff`  
		Last Modified: Tue, 23 May 2023 01:22:03 GMT  
		Size: 35.3 MB (35280911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d38ba339ef6043fdfe3ddd5359c69fcf0314d3e805835066f25f5bdec81cbaa`  
		Last Modified: Tue, 23 May 2023 02:52:45 GMT  
		Size: 10.5 MB (10481258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6686de7ce20c5bf6829105ad713ada3bd60313789b594e248ffe5250dc1b159f`  
		Last Modified: Tue, 23 May 2023 02:52:42 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9cf57585ce8987532ff175e0041c781bcc4db1c4520adf09d7257c7ebcf369`  
		Last Modified: Tue, 23 May 2023 02:53:33 GMT  
		Size: 32.0 MB (32040149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acdc99335d351094af5ea73b713f30145d8a6b0c5d0694b9017e0f4aa6a488d1`  
		Last Modified: Tue, 23 May 2023 02:53:28 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ruby:slim` - linux; s390x

```console
$ docker pull ruby@sha256:250e8d7f720ece654f006ae470fe4654d4b8452c8feabc19463ea7ae0edb031b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70160515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af6768d36e014c45042f07a3c6018e1838dac66769e295404ce768f3e6f6e53`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 23 May 2023 00:42:52 GMT
ADD file:23b1e12559302529556a94a1d4098dbdb454e263265258b940c2b2d23a97c121 in / 
# Tue, 23 May 2023 00:42:54 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:16:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:16:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 23 May 2023 02:16:13 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 02:18:37 GMT
ENV RUBY_MAJOR=3.2
# Tue, 23 May 2023 02:18:37 GMT
ENV RUBY_VERSION=3.2.2
# Tue, 23 May 2023 02:18:37 GMT
ENV RUBY_DOWNLOAD_SHA256=4b352d0f7ec384e332e3e44cdbfdcd5ff2d594af3c8296b5636c710975149e23
# Tue, 23 May 2023 02:20:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='5cc9ffd1026e82e7fb2eec2121ad71f4b0f044e88bca39207b3f6b769aaa799c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.25.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e189948e396d47254103a49c987e7fb0e5dd8e34b200aa4481ecc4b8e41fb929' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.66.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| grep -vE '^/usr/local/lib/' 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version
# Tue, 23 May 2023 02:20:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 May 2023 02:20:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 May 2023 02:20:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 02:20:35 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME"
# Tue, 23 May 2023 02:20:35 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9c24ec455bdb6a9ad0d033c7cce8e71dd5bdbbe53a86d5feeb8d4cb7804fb8e5`  
		Last Modified: Tue, 23 May 2023 00:45:47 GMT  
		Size: 29.6 MB (29642170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389e5acb5f585dd7876222f795a0f8adb45bbb36dfee1707ad06ef3c32abe06a`  
		Last Modified: Tue, 23 May 2023 02:25:49 GMT  
		Size: 8.9 MB (8864321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f41881192359d6eae65c1dea80a1676401b472e6565797e2c8a05658dbfc19`  
		Last Modified: Tue, 23 May 2023 02:25:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765174b826e55c241900aed7c3d62d20bf3979483266eec0f3af8ce364b21bb9`  
		Last Modified: Tue, 23 May 2023 02:26:02 GMT  
		Size: 31.7 MB (31653649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402962b852504de53b8adf865046a540563f7441a146d157270660e649483687`  
		Last Modified: Tue, 23 May 2023 02:26:00 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
