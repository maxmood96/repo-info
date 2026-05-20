## `ruby:4-slim-bookworm`

```console
$ docker pull ruby@sha256:2e3a51b8de80ca4ef72cedf690067fa7e378b1d613483adab7a389771fcd63f6
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

### `ruby:4-slim-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:5604d680c84f9df369eede4d52cd4df3ebeccfde22bef11ebe16c12d2f22afda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80731186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afd22b47164786212cc18b8664519fde507b1471e6390be36d194e7891b88d4`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:51:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:51:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:18 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:18 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 19 May 2026 23:53:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 19 May 2026 23:53:18 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 19 May 2026 23:53:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7437a5ff046c98886c928136937685f8c99736ee136a50b2d2116fb268f1f4`  
		Last Modified: Tue, 19 May 2026 23:53:27 GMT  
		Size: 3.5 MB (3511473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015e71c3a96b53db3281decbc805c8ada79e2bbd14064fb3ea0ca970ff96178b`  
		Last Modified: Tue, 19 May 2026 23:53:27 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810cd90dd8e8b5719289a804a15d3699120dfa7c36dbd1975fba26b995943b55`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 49.0 MB (48985834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28806927f6ae51a5cd3417d1e2e53e4a6ad7b851a8a48738425b54d2799fc9e`  
		Last Modified: Tue, 19 May 2026 23:53:27 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:cc0745181b9172601b85626f5c6fbda8a32d83b3d113594237ce357be38e6409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:944bc1f8c04ff0bf5028959cf19d858c1899ea238f47398196e32cbaa046de6f`

```dockerfile
```

-	Layers:
	-	`sha256:093dd4e1c30006456a61951644b351fc66ba2fd3ef3f43861080db0e748f8575`  
		Last Modified: Tue, 19 May 2026 23:53:27 GMT  
		Size: 2.6 MB (2597689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2007c0368edcbac325d06389dca6e74f7d542609bf564cb21c11259579cc61b`  
		Last Modified: Tue, 19 May 2026 23:53:27 GMT  
		Size: 23.2 KB (23203 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:d8a600e368af79619a5f059e769d562962752502163df3c4befc96d7e14404d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70817149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c043608c0d3758e30567d7f6bb1df0591d7d3e9229f50dc97dff8e9860fe91d`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:35:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:35:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:38:15 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:38:15 GMT
ENV RUBY_VERSION=4.0.4
# Wed, 20 May 2026 00:38:15 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Wed, 20 May 2026 00:38:15 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Wed, 20 May 2026 00:38:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:38:15 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:38:15 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:38:15 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:38:15 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:38:15 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913a9d7ce9c4374c9eb4b016f1b27a19afaa13be2937c493b8807aefe597b178`  
		Last Modified: Wed, 20 May 2026 00:38:24 GMT  
		Size: 3.1 MB (3082782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b386275daf739d7fc886a3e68eaa8cc966d233250482fce0fe9f3c5e8dceb5`  
		Last Modified: Wed, 20 May 2026 00:38:24 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09f031991ce996e3f12772a3281891377d2c47ad1d79b37111f0d34e72c2765`  
		Last Modified: Wed, 20 May 2026 00:38:25 GMT  
		Size: 42.0 MB (41965743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b49eb5d462e5a5e8f431076d5c3fcb298ba01caff941ddb0b7405de39c9f6c7`  
		Last Modified: Wed, 20 May 2026 00:38:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:23eaf78fa11b833bb57e3ff6dd64389aa0be48487df9ac42cac4c26afdeef05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37defb850e68356b2d62d507fb86f37e5261993afb3c16a739257a08e7090ab5`

```dockerfile
```

-	Layers:
	-	`sha256:7d8501293b502721aafad31f6347dc75a3ca820c7d4f960957c77bf7abbbd6d7`  
		Last Modified: Wed, 20 May 2026 00:38:24 GMT  
		Size: 2.6 MB (2601494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6426e27b2bc15fdd03ccb0d979369f2c3609df39ffb6b5424ff91052b9f54cf`  
		Last Modified: Wed, 20 May 2026 00:38:24 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:114b8439812b44c9338eed3b70928af6d879aae99db15b041d369f133139646e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68635902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36aaf737fb8be6edd4398f7ec27194330a1275f7def4f7a458d8f878c803b713`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:09:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:09:08 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:11:36 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:11:36 GMT
ENV RUBY_VERSION=4.0.4
# Wed, 20 May 2026 01:11:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Wed, 20 May 2026 01:11:36 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Wed, 20 May 2026 01:11:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:11:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:11:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:11:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:11:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:11:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a84fa2312e4e5911c8291125e783588e17de4cf5fb8fbdddaa41a4241a4dd1f`  
		Last Modified: Wed, 20 May 2026 01:11:45 GMT  
		Size: 2.9 MB (2915731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9403426a598adc1670ed095e0b56fce7e7523e596541af3009fc9fda818b61`  
		Last Modified: Wed, 20 May 2026 01:11:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f77d4a5cc8bce98cab85694e275f1be821ada8e9a270060f7c2aedec75535a69`  
		Last Modified: Wed, 20 May 2026 01:11:46 GMT  
		Size: 41.8 MB (41778195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a41a42e7372e372a95e1cf7d52dac18d36e4f50467113b9e4c89934a222cb1`  
		Last Modified: Wed, 20 May 2026 01:11:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:19bf9b323420e0e27b915e98803a2e66023cd1e567eeccf9a08cfa473bee133e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2623236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6d6dd31b5fb90354ac61b088d11d5329cca1e948b73c7b14e5e88541086423`

```dockerfile
```

-	Layers:
	-	`sha256:b1136e7c981744d2afc73ad1fc5b91cde7c9ad58809119ae0864223c896e8f06`  
		Last Modified: Wed, 20 May 2026 01:11:45 GMT  
		Size: 2.6 MB (2599913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fab935b711aeb97f78e127429295bd5f912b45aa40438bca11cdd64346158b0e`  
		Last Modified: Wed, 20 May 2026 01:11:45 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:bfe65a31ddffdcd42d89a92ffa621c986e24c3c8e56c259fdcc1bd737405a52c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80179063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6424201ad005978280efaf299a930d08b9310fd7bcdcc5345f5b29c4f9966049`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:58:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:58:54 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:01:28 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:01:28 GMT
ENV RUBY_VERSION=4.0.4
# Wed, 20 May 2026 00:01:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Wed, 20 May 2026 00:01:28 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Wed, 20 May 2026 00:01:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:01:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:01:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:01:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:01:28 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76aef3aaec90e5d550268137b900c45a18a4c6ab71c88a3bb7e2b4fac719700`  
		Last Modified: Wed, 20 May 2026 00:01:39 GMT  
		Size: 3.3 MB (3344300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0e131d9a3ea7c939cae9d352023fef9c3c1e5e7077b9e5939e501dd7cb3972`  
		Last Modified: Wed, 20 May 2026 00:01:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161f16678054abbfdfa7878d93213de6ac8951bca353d03b5f2a61545e3110e5`  
		Last Modified: Wed, 20 May 2026 00:01:40 GMT  
		Size: 48.7 MB (48719387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f64ac93f86b5ad8cbb194710fa7165dbc1feb1651c0c51d86784fb3537b6d4d`  
		Last Modified: Wed, 20 May 2026 00:01:39 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:541a582a78579d5840b3e145f0feaf6186f34c11793c713a7fdd4124af4f1732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5c4c9e5b425d6cfebc5337545adcd49a467821318c245aae3baec987fa3e68b`

```dockerfile
```

-	Layers:
	-	`sha256:f853f9fb2a45cc1d900de45cccb80d908ed7e1d682610d29ad12508961a2c698`  
		Last Modified: Wed, 20 May 2026 00:01:39 GMT  
		Size: 2.6 MB (2597947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f698f43b487548fa6186bd78bb60ec266b12f84b67eeb5cdeb9eade6a7ba9e1`  
		Last Modified: Wed, 20 May 2026 00:01:39 GMT  
		Size: 23.4 KB (23353 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:a79d4378831a1e04f7b302333b4e485375d0d189be28a19daf8673e985096ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74496816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2972177591f0d0af74c61d5ec3711a58a502757c90dd6ee6cbf43569c00744e1`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:50:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:50:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:12 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:12 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 19 May 2026 23:53:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 19 May 2026 23:53:12 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 19 May 2026 23:53:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:12 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:408fe432485bb366e9a4871b553de2e6347ca580fe8a5d45c84c87fa58d5e5c7`  
		Last Modified: Tue, 19 May 2026 22:37:12 GMT  
		Size: 29.2 MB (29218601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c46dec71db45765e49d2d5b525d101c52e66f22bbc7328de3d5a8ea13a296c24`  
		Last Modified: Tue, 19 May 2026 23:53:21 GMT  
		Size: 3.5 MB (3515430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50baf35f8de41f4a6aeb893930a27e62ef465f3c791cb70b052bb3433d73a89`  
		Last Modified: Tue, 19 May 2026 23:53:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc9199ed246f108799439bf5fa53f00f0c28be0e602247e8668152832d036ef`  
		Last Modified: Tue, 19 May 2026 23:53:22 GMT  
		Size: 41.8 MB (41762452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ba0d50ccc7a89bfabd1ec53175b9d968b27fbde40afcff0529fb370ba940ce`  
		Last Modified: Tue, 19 May 2026 23:53:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:86b0af2957a7ad508639d60804a31799583fded37cbff1110234fad8d35ea358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f768784f52968ff5f4c3a0f0dad431e5f714b638ed273d0386ac0a4f7201744b`

```dockerfile
```

-	Layers:
	-	`sha256:c03dbf402ec76b569f85ce31c6a01ec227675ea992634982b925cf53744fe188`  
		Last Modified: Tue, 19 May 2026 23:53:21 GMT  
		Size: 2.6 MB (2594870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b9388ab7f635120fe1399d7bd2d78583882593af48c2194079e56a5e97e432`  
		Last Modified: Tue, 19 May 2026 23:53:21 GMT  
		Size: 23.2 KB (23166 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:2ed8974dd6ebc9c8c7d8078e702ee6cbc8a9d82bd245e6981ad590843496bcbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74767702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d46608cd1111ae27c900ef466404902369256a9121f56fad772a1fc5bb59bf2`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 10:47:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 10:47:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:32:16 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:32:16 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:32:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:32:16 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:32:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:32:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:32:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:32:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:32:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:32:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8e1a6f4f5a9e9628f902e3c8df639d1691d7f1000dc904f820155d1b9b2fa2ff`  
		Last Modified: Fri, 08 May 2026 18:20:04 GMT  
		Size: 28.5 MB (28526280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03245296ed4c53e7e3243a0fa73f65d2e35b8668cc7e9f3cc6607d0c1eca2a42`  
		Last Modified: Sat, 09 May 2026 11:03:47 GMT  
		Size: 2.9 MB (2902318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b375eb3b507d8c82f2f4acafad10d11d011df27cb70fb48ede1ed2a1978be7c`  
		Last Modified: Sat, 09 May 2026 11:03:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334493b3024a678cb8c061e5c2e72e9b2b5ffb0ad9d37919a1e1f406a6ab3233`  
		Last Modified: Tue, 12 May 2026 00:33:03 GMT  
		Size: 43.3 MB (43338769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975919265243e4b1c023bf3acb6770264882d99bd4bbaef25bc76516083137ef`  
		Last Modified: Tue, 12 May 2026 00:32:58 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:b9c5384b7240ecd07544183c68aa7ecad4e5dc1cf63610e6b8181863b9d692e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ab87297e109380de9d80ffea9c517e6ae70f6f8f8549d6f6f5d61534d5bd7a`

```dockerfile
```

-	Layers:
	-	`sha256:bc9a42c03d7a005922d2c56f200b2d65ed6340e79b8b76c22cc2f7f162f74b5b`  
		Last Modified: Tue, 12 May 2026 00:32:58 GMT  
		Size: 23.1 KB (23064 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:717eff69159fc8c93ff8abcfe7c8db27c5da9e8c7394e4167189c0e743b5f1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79652207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974d61b7734088e5fef4f888070565127a51abaa7452ce961393f9890237229f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 02:02:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 01:03:26 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 01:03:26 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 01:03:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 01:03:26 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 01:03:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 01:03:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 01:03:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 01:03:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 01:03:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 01:03:26 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffde109a7f36d8787d6dc2b8602d11b1d3e583896da3f19273d1024e6840ab62`  
		Last Modified: Sat, 09 May 2026 02:06:26 GMT  
		Size: 3.7 MB (3711891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a386e5a54e6ba22141a4bf874e54c80ebac21f8ea950f613ca335c685399549`  
		Last Modified: Sat, 09 May 2026 02:06:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d3ab85fd5a808d410bd6157e010c1ea9d4a37f08168217155a1b18b4d36b5b`  
		Last Modified: Tue, 12 May 2026 01:03:47 GMT  
		Size: 43.9 MB (43861528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb78a04aa8c06cd29aa16bce95f70f86acf22b3e902d7ea27b82dce4d434e4ef`  
		Last Modified: Tue, 12 May 2026 01:03:46 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:a50a5d66836d5cd700edb8a05e1105fe6b142af2633ffbd07017ee40edab72d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44988628f5cf96fea800dee0db62df55ab9d91a760df7d272e69c6aa81d1a0cd`

```dockerfile
```

-	Layers:
	-	`sha256:2e7263441ec85411e8bbc819a95b01ced78cf353fcb9b7b9841b3956c45400ea`  
		Last Modified: Tue, 12 May 2026 01:03:46 GMT  
		Size: 2.6 MB (2602062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6816a034060f1a5d067899bec985a8f1f870a1d3de7195feedf90c89c8850db`  
		Last Modified: Tue, 12 May 2026 01:03:46 GMT  
		Size: 23.3 KB (23254 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:4-slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:9df217b5f85830296171df84846c9ff06cf3ee80c9605a33beb81c4685bb966a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73155626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921854be436a8666dc665a253334515f1cb926aeb5699df6529ccc3427793f4c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 00:06:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 00:06:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 12 May 2026 00:09:36 GMT
ENV LANG=C.UTF-8
# Tue, 12 May 2026 00:09:36 GMT
ENV RUBY_VERSION=4.0.4
# Tue, 12 May 2026 00:09:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.4.tar.xz
# Tue, 12 May 2026 00:09:36 GMT
ENV RUBY_DOWNLOAD_SHA256=6ff9d2d6e75f5a6f997222ecc45f79209d663737eceb3689d1f42ab952673fb7
# Tue, 12 May 2026 00:09:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 12 May 2026 00:09:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 12 May 2026 00:09:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 12 May 2026 00:09:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:09:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 12 May 2026 00:09:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bbb386086a73fa6455b55838bf67c1540c2367a10d30cb1479d8575fc9b174`  
		Last Modified: Tue, 12 May 2026 00:09:50 GMT  
		Size: 3.2 MB (3172030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287415afbb6267a1c9a4d289acb50ec8d8df22151b6d80d1040d7295923f44`  
		Last Modified: Tue, 12 May 2026 00:09:50 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e81293b4e55c48aaa49e3ec75230b118738bd034ee61e91dcdc24925456fb5`  
		Last Modified: Tue, 12 May 2026 00:09:50 GMT  
		Size: 43.1 MB (43091659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8a10fafd95be6c269080968b5e86c49acecac9299927b2801f44bfc4852a3a`  
		Last Modified: Tue, 12 May 2026 00:09:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:4-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:3db51425518a3a2262825f1dac1a1aafd30cc17049a79fa8ec1a63774d9a76a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:835d3953d06d1609f8f7da6bbf9464bb145930f21cd68feb53dc687f0650780a`

```dockerfile
```

-	Layers:
	-	`sha256:20acf0ddc72206fbd817f271ca06907aa9796a99fde5689edefa1ccf7c32133f`  
		Last Modified: Tue, 12 May 2026 00:09:50 GMT  
		Size: 2.6 MB (2594502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed51be14b3cea415e849e9b90aa9d4298b1cf709e753867105ecad0ee0d0c870`  
		Last Modified: Tue, 12 May 2026 00:09:50 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.in-toto+json
