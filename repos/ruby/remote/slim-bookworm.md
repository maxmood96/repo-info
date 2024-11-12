## `ruby:slim-bookworm`

```console
$ docker pull ruby@sha256:af044c9910442618c8a721a573aedd6432f8e9ae2bdba1be64014b765df9e8b2
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

### `ruby:slim-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:e090e30f8e93753d6f346bf2113b180259b54ceb4f386bdfd2ce291cd0dca40e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80862172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5a52d7e0245b9ea2ca9f4ed4866d57d28b8052de6f4840ad88d6327a8110a9`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 Nov 2024 06:03:16 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["bash"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b27ca67ea6eb24d2fe3d582fc5d98481575207bebe04e5e7e9b1cc7b590c330`  
		Last Modified: Tue, 12 Nov 2024 02:50:00 GMT  
		Size: 13.9 MB (13862691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8d420d062b796a02d7a627396e485ba8ddb7be0def38099a15f888415bf17f`  
		Last Modified: Tue, 12 Nov 2024 02:49:59 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc23a28a8c502692f956f3450557a2ba2ad225acf77ff47ba6a128d389672a42`  
		Last Modified: Tue, 12 Nov 2024 02:50:00 GMT  
		Size: 37.9 MB (37871147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642840fffac821a8f6eaab207e964c114d28447fb577be41dc7d2ab1bbd7ca5d`  
		Last Modified: Tue, 12 Nov 2024 02:49:59 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:8dbb473991b472313ff1afb20cfb8d9cd82f786e009f487ddea593464df4e456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3947762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a4ee25acd3cf87baef736f03868b566e4428923e26303950cd9147544c5df4`

```dockerfile
```

-	Layers:
	-	`sha256:c9f5992bd82c6e2875285d02b84b351aed4297261ef646008fec625047360dca`  
		Last Modified: Tue, 12 Nov 2024 02:49:59 GMT  
		Size: 3.9 MB (3922734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d12820ff773a76449ffc0c5c8eabb3cf1f958df896520368d61492e67e17ca4c`  
		Last Modified: Tue, 12 Nov 2024 02:49:59 GMT  
		Size: 25.0 KB (25028 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:48530cf1f384c7a62b094cafc2bc669aa64588013c2aa9bc6ab1160a64f24575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72711422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13ea2b65982046bf79a613585fd63e9761fad55a07c3a254e419ba242d077b4`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:28 GMT
ADD file:c8ec8d65b2f61866a2c6085ed61e936733bc484abeeba1b91d12b9f6a97e456b in / 
# Thu, 17 Oct 2024 00:54:29 GMT
CMD ["bash"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e51d4479d9f15eaafec663087c05baede0a0724dc30787f7912ade3b686f46b1`  
		Last Modified: Thu, 17 Oct 2024 00:57:27 GMT  
		Size: 26.9 MB (26887306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79ce1f192165e9a7ce336963643a944c339a24427a87c96c3698d3d6641f348`  
		Last Modified: Thu, 17 Oct 2024 09:49:24 GMT  
		Size: 11.6 MB (11620510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1368a401dd210cbfccceb2812e7b128f261e2e405f473856acb05966577669e`  
		Last Modified: Thu, 17 Oct 2024 09:49:23 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fade1148728be32eedc8bac3c7c2022345030a6c4c2b0a4b41911d326ee8b6`  
		Last Modified: Tue, 05 Nov 2024 21:10:21 GMT  
		Size: 34.2 MB (34203264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3085eb947220d180c7e622e2c7c1f1cf44583949fa7d94e37d03b7591cd9bfd`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:99d862d99a181a0b167719944ed20261f6599668684165a2707116fdf65b3135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3918284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7feb43eee4fb9c6cc5d9e313828cd35cb6bc97f226284a6951d6c6db16fafb`

```dockerfile
```

-	Layers:
	-	`sha256:96c769e65fba83572b0ea659893988cdcd6e0bde935ac812f07816460bca7319`  
		Last Modified: Tue, 05 Nov 2024 21:10:20 GMT  
		Size: 3.9 MB (3893281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15c9338e94e1e96c6aa336c40df883bbd239d6369dee8c5d0b7533ee978b7fdc`  
		Last Modified: Tue, 05 Nov 2024 21:10:19 GMT  
		Size: 25.0 KB (25003 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:5ecab75e297d14ee47ad05030eace5e8df7d12e5c783c231c67649cda2a166b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69757272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3171996d673a37e8b606bb568c8627258e06716d4e2037ca0e9432a0fa23f020`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Oct 2024 03:03:21 GMT
ADD file:e76e8ba7ebca0b1dcaec16ad1e863ab59c7e155f0b95ba46f5543e418a904b35 in / 
# Thu, 17 Oct 2024 03:03:22 GMT
CMD ["bash"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d6319e551f4eae5cadf245338228c7b7cbad94a77c481a88ccbffef7b89f0aee`  
		Last Modified: Thu, 17 Oct 2024 03:06:55 GMT  
		Size: 24.7 MB (24718197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad165fb974bace21f0a023b5b89416ab63e61be2107ec588eb1e3237717f2848`  
		Last Modified: Fri, 18 Oct 2024 01:28:48 GMT  
		Size: 11.0 MB (10960451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c56512ba6b2a6c37a25326a81238b0efa1d28a20513e43854cb3a8fb21267af`  
		Last Modified: Fri, 18 Oct 2024 01:28:47 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f825a0f7684ae2907d36e7eeadf90b295958d24a34b1079fc8de317611ef60`  
		Last Modified: Tue, 05 Nov 2024 21:14:11 GMT  
		Size: 34.1 MB (34078283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f621b136ede166b4a3d39b2ddce6443aabf9e06e8ce8c09f3cd99752d6adc559`  
		Last Modified: Tue, 05 Nov 2024 21:14:09 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:eb968186994866d517da71d40b3a9d8b78f2cfde8d95d013d881727b091308d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd695d3f3da985e152827e369047578fa372d5bd8703d0af80927fce5f2b75bc`

```dockerfile
```

-	Layers:
	-	`sha256:c6f2b7fe78e88fb72f9119a31d8d6c1f57759d754a7a9925504df5fae6e6cb57`  
		Last Modified: Tue, 05 Nov 2024 21:14:10 GMT  
		Size: 3.9 MB (3892828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44daa0214d979321d2161d3f77ae647ca16e507dc6655214625983a3322dfef4`  
		Last Modified: Tue, 05 Nov 2024 21:14:09 GMT  
		Size: 25.0 KB (25003 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:4a325eab1d553e3147c7e0b772edbe00c3e8fcabae8c63862ddb27b9da30e209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79794431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc4addce4d5ba016a42807f065b8927bcaec7f763039b7adad5e92d3dc6e727`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Oct 2024 01:11:59 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
# Thu, 17 Oct 2024 01:11:59 GMT
CMD ["bash"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15fa32e5c8f64ba8c5dc13eeb40a1f4b4139996b89fa1ff32fdbd39d393ee13`  
		Last Modified: Wed, 30 Oct 2024 19:10:25 GMT  
		Size: 12.7 MB (12705660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dcf4909f6f483e882642f22161f8fc2dfcf3a570e53433d1479bd85ea99340`  
		Last Modified: Wed, 30 Oct 2024 19:10:24 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671e32ea69c2b1ee8f5c040cc0bdf6d3423599c9e7db6d9f449ab2b661e1cfa7`  
		Last Modified: Tue, 05 Nov 2024 20:34:33 GMT  
		Size: 37.9 MB (37932091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1941dbfd10f7e1fbfcf59a25188a50e48e9af026093fc8207e9f571cef079f62`  
		Last Modified: Tue, 05 Nov 2024 20:34:32 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:71f21ede0619dc7ed389db565173dff54f9d399d77d44d2e9e7cacd33e919349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525b8e601ee9dcbfe86d9d4d683694be02dfd0c0ee861e179c5a66e62dd52e5b`

```dockerfile
```

-	Layers:
	-	`sha256:0502ecdf1a4459c71f80c7bb46ffe327f17ebf07122a85dd301a42e6b0f0bf62`  
		Last Modified: Tue, 05 Nov 2024 20:34:32 GMT  
		Size: 3.9 MB (3894000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3d4389eb633aab63892dbca40548a290a128e5da6254b6d260396a5e333c1ea`  
		Last Modified: Tue, 05 Nov 2024 20:34:32 GMT  
		Size: 25.1 KB (25053 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:6a1531be6362f465818a0e55bb65053df84e7daf0f233dad9020fdf6828fabbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77553943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb84598b505cabe944193cffe6550db1729fe3fdf450815b189f874154fe63cb`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 05 Nov 2024 06:03:16 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["bash"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bb38203301fa1e3b63e9368ca2cb183531d6dbf5cb4bafcccb427164317500`  
		Last Modified: Tue, 12 Nov 2024 02:50:09 GMT  
		Size: 13.4 MB (13417452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceec680ae39a5ac40944f4e0c1cf5ee2b87a69550ea360d9dec3871518242c99`  
		Last Modified: Tue, 12 Nov 2024 02:50:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4599ba98e33c31434bf46edf1285386ca405c7954a56bc95e267002eace70d0c`  
		Last Modified: Tue, 12 Nov 2024 02:50:10 GMT  
		Size: 34.0 MB (33990704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00629f836b8eb375f1fc212baf2f0ca3c85d13577df7ec99af49ba0240fee6e`  
		Last Modified: Tue, 12 Nov 2024 02:50:08 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:33a6fc29cf41e0dc125f213190bbeb756e8f6f33d338f8b72766c2094e8b8e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ce66fd391c1b6df98387c791a705c67c1c72c140a4207244c35df1565b863b`

```dockerfile
```

-	Layers:
	-	`sha256:19d47ac7f0c33d170ad705d0b94aab9b57f465a5b935cb35e7227d3145c10322`  
		Last Modified: Tue, 12 Nov 2024 02:50:09 GMT  
		Size: 3.9 MB (3916572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2946629e8150238572b150b7f3fb7e5c9406e049e6e6d3754eeeb1ae212378e4`  
		Last Modified: Tue, 12 Nov 2024 02:50:08 GMT  
		Size: 25.0 KB (24970 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:530724c0c824bc5a17a89a47c40c071d3604991d10f5b5943a56ea38e77115d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77384410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66039defb68661b01ceaaf8df4800a0076ccbeebfd17c33c7c65861bd7761bb`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:35 GMT
ADD file:6c11edc513b28b5a4034ee9c0d4cdcf019a82635ebb8a9e02732800fa457f683 in / 
# Thu, 17 Oct 2024 01:09:40 GMT
CMD ["bash"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8f9d02f0305fc460f51690aebcb328c22e13a197228c0910e24b813db943a15b`  
		Last Modified: Thu, 17 Oct 2024 01:18:03 GMT  
		Size: 29.1 MB (29124779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198948031bdcb429cca51550c93047bbe816ecd1fbe0ba6aac8b2b71b811584d`  
		Last Modified: Fri, 18 Oct 2024 10:06:17 GMT  
		Size: 12.9 MB (12886712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e80f555f871e3949b531fde798eac54202107de9e19a10abd8cc28c85152975`  
		Last Modified: Fri, 18 Oct 2024 10:06:15 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ba54a6c06cb48a9179a054d8f5fe72c29ecaa53f19c710274df4f9282fbf08`  
		Last Modified: Tue, 05 Nov 2024 21:14:28 GMT  
		Size: 35.4 MB (35372576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dca86db022f78938563dc1a033dcc5da200b716d2e4590e88498c8eaa002b6`  
		Last Modified: Tue, 05 Nov 2024 21:14:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:10197d8f148287556060a937265188b42d1a70817e42d3b58168566c9b0d9d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f7c491ca8be9042f82cfb49002717cef6d023d713f1771ad26c85aef87d924`

```dockerfile
```

-	Layers:
	-	`sha256:7732c8c45d1decab4e15dd2dac2d53fc46b21131aa8bdfd4d775f1aa8733dde1`  
		Last Modified: Tue, 05 Nov 2024 21:14:24 GMT  
		Size: 24.7 KB (24749 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:46a0067b5fea69399135e61bdfb81c6b15ca5fc9e1ece8796478fc2ac4e29ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83441382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e3113871de6f690fc9e915b701610ac2351d08b41cac06db2df4af18b0a696`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Oct 2024 01:18:54 GMT
ADD file:92b9ed0a5c924ec85b272100ff6dc81f126c6bd277ec2b3782af1119f9e07391 in / 
# Thu, 17 Oct 2024 01:18:56 GMT
CMD ["bash"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b5dc74e4487f0d4e25ed24462fe1564f5d931072ec24eeaee669f9cbe27f10c4`  
		Last Modified: Thu, 17 Oct 2024 01:21:56 GMT  
		Size: 33.1 MB (33122201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2085a9bf6425e1db4aceff65b459218746f21da3a2b2bc7c609f6e7f3bc13cc`  
		Last Modified: Wed, 30 Oct 2024 18:29:41 GMT  
		Size: 14.6 MB (14591140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d294ef697680ab988c128a54b9e09239e2b59f695cf8665e799a6dae10a3d05`  
		Last Modified: Wed, 30 Oct 2024 18:29:40 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994b1cc5781e13a22f3cb39d8f712688d76534a9a9351134757eeb924896b7be`  
		Last Modified: Tue, 05 Nov 2024 20:52:20 GMT  
		Size: 35.7 MB (35727698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569a47be6ef78a4e824cf8eb80fc4e01d7a8d09c3593a5509a0d30824a4b1fcb`  
		Last Modified: Tue, 05 Nov 2024 20:52:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:0fec1566bc1c6ae18dc6096c623ab9901bf0f0bfb4ab467d26dde749c66d1056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3933488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403447ad42ce29fd86ea0e72541799247009ba9ba306e32d89b256c831a6ca01`

```dockerfile
```

-	Layers:
	-	`sha256:521127d2156b5c3f6c4035640c82c293b672b973ca987ec3c81203f2e4936e72`  
		Last Modified: Tue, 05 Nov 2024 20:52:19 GMT  
		Size: 3.9 MB (3908558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8725b1773d1f730f6720ffa80a249a77399a702bdac10a21b628cfa3f02f304`  
		Last Modified: Tue, 05 Nov 2024 20:52:18 GMT  
		Size: 24.9 KB (24930 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:0a1756bbb302c56f230c09803ac75e36b8796ef1b7f955906ba31ef511242297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74529689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875158a6f8d8cf4fda2e52ba9af2c339c3c69234291c97a5ca7333142fb0b8ba`
-	Default Command: `["irb"]`

```dockerfile
# Thu, 17 Oct 2024 01:46:19 GMT
ADD file:53293b1530bfd7e933ac5a321d4b0604f56c0fa25d3afeaedb0cec1938b938a3 in / 
# Thu, 17 Oct 2024 01:46:20 GMT
CMD ["bash"]
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV LANG=C.UTF-8
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_VERSION=3.3.6
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.6.tar.xz
# Tue, 05 Nov 2024 06:03:16 GMT
ENV RUBY_DOWNLOAD_SHA256=540975969d1af42190d26ff629bc93b1c3f4bffff4ab253e245e125085e66266
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 05 Nov 2024 06:03:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Nov 2024 06:03:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 05 Nov 2024 06:03:16 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3544f1137f2bd42b766143fd0dc535d7e3a32f7fab936cdbc531329371bc5687`  
		Last Modified: Thu, 17 Oct 2024 01:50:31 GMT  
		Size: 27.5 MB (27490084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdaf62e0109103a0f4111ef4c0c7a451f221c717e4371b21f8c5dbd53f766d93`  
		Last Modified: Wed, 30 Oct 2024 18:37:17 GMT  
		Size: 12.0 MB (12041273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a34458864c6076d695a68c5f4e6a0976af64a04a40b45a7583b69ad5811fb7b`  
		Last Modified: Wed, 30 Oct 2024 18:37:16 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539ff21b52a16466fd9e07581b2db18717f565cf360851a0a9e303fc1c9c54ad`  
		Last Modified: Tue, 05 Nov 2024 21:08:37 GMT  
		Size: 35.0 MB (34997989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34e80ddb995df0ec94a697a5359f600f529f8c11f1d2d5c1c912aaeead7cd7e`  
		Last Modified: Tue, 05 Nov 2024 21:08:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:4ee86743ef27525af74d44074cf223fcc7f56ae040ff06f65d7ca6ebf1977fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3935741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df202c7b91d9dec34a4419cb033971140e1bc1cbafea01a607ae50010dffaf9a`

```dockerfile
```

-	Layers:
	-	`sha256:1abc3d3cc02622f9672d8a1e998fa6dfeb6bff0c1fc2231139fc8944a2c58a3f`  
		Last Modified: Tue, 05 Nov 2024 21:08:35 GMT  
		Size: 3.9 MB (3910879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178507c25947562ef6cf6ee219ce4f7976f8bc13d414c2147f7b1678348e51af`  
		Last Modified: Tue, 05 Nov 2024 21:08:35 GMT  
		Size: 24.9 KB (24862 bytes)  
		MIME: application/vnd.in-toto+json
