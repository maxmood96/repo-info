## `ruby:3-slim-bullseye`

```console
$ docker pull ruby@sha256:40d54192b00f4454abd5cd800a38e245d6d3dbfa5aae3d8569ef18e7efe61313
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

### `ruby:3-slim-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:42fc8c0a1b1e03a293eade463308f7f19ffb745acd9d65f34916a73743a8c651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77629723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424d77abbbb74f34523525088a0da76082867cbc6443f5999ef1ea814db8fdf7`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 07 Feb 2024 00:26:58 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b03e0b9327cab3ce58e401160a57ac1003ff72665d7c6aa3584a05d6403c6e5`  
		Last Modified: Tue, 13 Feb 2024 01:57:42 GMT  
		Size: 10.0 MB (10019268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f870de51c24d2eaedf07b5d72716fe6c2cec8f812e84bd438a55398754ac90`  
		Last Modified: Tue, 13 Feb 2024 01:57:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04ac767566d7a9fc5702322427e9b9f6f4515bba874e893e398824b36d61099`  
		Last Modified: Tue, 13 Feb 2024 01:57:42 GMT  
		Size: 36.2 MB (36187692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9812673232aa0f6231ede1dab622078290c3574b9e0f04846c1505c42c71030f`  
		Last Modified: Tue, 13 Feb 2024 01:57:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:5852fa1287e2fb9e5fc8bbe1904eb3b1629daca6a6419e99a04abae358765370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3581045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39b54b45171708f7555118e3be6305bb680e89a7057e787eaf9265c35a06fd`

```dockerfile
```

-	Layers:
	-	`sha256:c05c6ffec2be3c68e2a3b79df2499d296ec721a144960242c27f35c630ad7f99`  
		Last Modified: Tue, 13 Feb 2024 01:57:42 GMT  
		Size: 3.6 MB (3557441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14a53b983cf8bb33867c11e5456e365377ccc90aa3cf473c655be05703dd47d0`  
		Last Modified: Tue, 13 Feb 2024 01:57:42 GMT  
		Size: 23.6 KB (23604 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:36816f5cad72e6f480f6e6cd0c7d124e69549e23ab5f3d526d87100aeaaabe42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69807951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7a763f22ba2f80cd27c417d5ad37850855c1599af20312b18be9785d89b8f0`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 07 Feb 2024 00:26:58 GMT
ADD file:2900145429df7cd46dd4818f44636aff96d0ef5335d5eb8cd5ed3106caa8b031 in / 
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:237c1c7c36842faaa132f240658a3f42b8e6adb150f7850dc25fb4b50ed242ba`  
		Last Modified: Tue, 13 Feb 2024 01:14:18 GMT  
		Size: 28.9 MB (28924482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1e9fbbd971ccf44516036fe26277944369d35fc2de21be77c5e676181f402d`  
		Last Modified: Wed, 14 Feb 2024 02:35:58 GMT  
		Size: 8.6 MB (8632525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cb2f8bb771dec284f0ae52412f70b415918deadd14756117daa719f25edf2c`  
		Last Modified: Wed, 14 Feb 2024 02:35:58 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788ad6a6a63302c5c7ed0aea5cc61db3a36432ab98a481ae46f0fdc11904540c`  
		Last Modified: Wed, 14 Feb 2024 02:35:59 GMT  
		Size: 32.3 MB (32250603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7244a2d646e0c0d29efeeba61b1b124e3d02e992b767897a81ca469453ea3e`  
		Last Modified: Wed, 14 Feb 2024 02:35:58 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:db32fdf8dbef1c3e4dedb769f63d45fdecd133885124a1a46b3d8b180a4bd36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3556241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfcaebb7e3d1817a0d5ddeb9825a11359a7fd49829944582c5af0b214cdc6e8`

```dockerfile
```

-	Layers:
	-	`sha256:5c81d7ebed6a97cd4a1a2a63b55c8f2430dcf4eaa7fe4fffb8a59b3e89d2a342`  
		Last Modified: Wed, 14 Feb 2024 02:35:58 GMT  
		Size: 3.5 MB (3532699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b7288b28d4ebbcf6b5a41e30d72e85da1e6d242c7e32a3a972cfb30bdf15aa8`  
		Last Modified: Wed, 14 Feb 2024 02:35:58 GMT  
		Size: 23.5 KB (23542 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:ca6071884f90e2c6b953920a87d37e72066b45826d0d386270ecbcbdfa4443dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66674141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de0c308d985ccfb20fac207a3a03f7fc9af7f57da33ecddc911aaccaaf5153c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:65b9e2efdf2b09faf0d5ea0e2e00984ff3c8cf89b7959287bc6ca54c7772801d in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4de6a546d77461a35cb9514c6432142adfb72460cf04bac21bd261d66c288476`  
		Last Modified: Wed, 31 Jan 2024 22:49:36 GMT  
		Size: 26.6 MB (26579212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb8b1e53340c66d7f8666bead8dc92493a496ffab6753fd5a1d5a71200fc19f`  
		Last Modified: Fri, 02 Feb 2024 10:50:27 GMT  
		Size: 7.9 MB (7936144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7fea31b19e61a014b3c03b4f0d1a107468f693b69e4c8002ddc2971cc18850`  
		Last Modified: Fri, 02 Feb 2024 10:50:27 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988c26e6dff40d74de64ec63e7869a7f2e8caa5d33f6b06fba814c7cac552688`  
		Last Modified: Thu, 08 Feb 2024 04:53:51 GMT  
		Size: 32.2 MB (32158444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f3f83c9e3feee529f33bea41f93a7ff9be367d2ab1b98da4696f69a6320947`  
		Last Modified: Thu, 08 Feb 2024 04:53:50 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:ad725cc97caf1f36e61442e13e74dc0e9d6aaa9eb85d149f8b21262dcae65f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3467239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb36cdb6cf764f10cc15c1df5af9fb4b8746c84e1e541a72399b7ae4a9049b68`

```dockerfile
```

-	Layers:
	-	`sha256:4e86fec737f40e6cc298bb0be49f57e3478847857998fbfc7391bae5beb96c84`  
		Last Modified: Thu, 08 Feb 2024 04:53:50 GMT  
		Size: 3.4 MB (3443697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd3c81fd4fc09b5e23889ef0423ae2c4b324e5e5c843744559bad5156d84da85`  
		Last Modified: Thu, 08 Feb 2024 04:53:49 GMT  
		Size: 23.5 KB (23542 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:58dbfd40a1ccbf6796d209a74d99a086dfa9010f56fefe93a2a723d0e4786bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75403403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65799d8bd74e8503769f4453ae9f05c6aec6a6ebb4f685e8509856ae07de1243`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 07 Feb 2024 00:26:58 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e97c022709be1e17b17f402896b1bb1848ac5a221f138773e28f7d47d1e4e86`  
		Last Modified: Wed, 14 Feb 2024 08:22:17 GMT  
		Size: 9.2 MB (9240742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe340a408654e6223a3620962945372c82dbf2fb43915bea5ae05c27263e47f0`  
		Last Modified: Wed, 14 Feb 2024 08:22:17 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee8faacfe56b64792fdb97d7f258af2cabc096c1f4665d1b7e5a1deb821d0b87`  
		Last Modified: Wed, 14 Feb 2024 08:22:18 GMT  
		Size: 36.1 MB (36091242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42928b46c20a02bf439ab18d4dba8df272e1d1e24f863497d7c64accf3e6d20e`  
		Last Modified: Wed, 14 Feb 2024 08:22:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:bd1a012da76f8b2bd0fb6684840a00552bedeeeb3731b6e2e30106a33f8faac6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3558828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67562ed3c6bc48ee8c45ab53bdd26eeaeda80e9856b07da576769bda4e542f2e`

```dockerfile
```

-	Layers:
	-	`sha256:1b38d2da408bacb7ef7c5af32c2df083422538ad02b158b3df4128562c3b4135`  
		Last Modified: Wed, 14 Feb 2024 08:22:18 GMT  
		Size: 3.5 MB (3535386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62932fee6c297e8f5c6d2d04d9b171eb8ac49986aec5e85e31de4774e51d8852`  
		Last Modified: Wed, 14 Feb 2024 08:22:17 GMT  
		Size: 23.4 KB (23442 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:7eb476ea2cf8930ff489f9549bafc3d2d0892717d204dfa59297ed036d324bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76637863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4986e8092fc50b71165742391ceec8f7eb6465e070449ed5cfadb86b533956`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 07 Feb 2024 00:26:58 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a0b5323c48ad80cd9bd0989e07d35a1d29ede7ab2fa388b9d365ba4cc4cd94`  
		Last Modified: Tue, 13 Feb 2024 01:57:33 GMT  
		Size: 12.0 MB (11994442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2018fe8cf82b06e1e7a79f0cfde315dc1594882e1e3ef41285a952a8a48e1`  
		Last Modified: Tue, 13 Feb 2024 01:57:26 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a078a1b83ac0f85bacafb992752ae700e34acba0e05a6f92f9f13e5d9c479d`  
		Last Modified: Tue, 13 Feb 2024 01:57:33 GMT  
		Size: 32.2 MB (32235640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb586fc5adcfd31ba3415ff2de63403b1913bd8e1143131e8e99e1e223ff87d`  
		Last Modified: Tue, 13 Feb 2024 01:57:33 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:05cf3b0d99af4d36e91009dad43a8890c63394fd87d6b81b7345453a924e29b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3584260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b5999c049425d5f562fcb302c525591fcd40ecfa024f1521ccb57f93225c3c`

```dockerfile
```

-	Layers:
	-	`sha256:fc358fe281623227a6e82808cc378173f14d53cdf59ef7df80a34446bb0ec512`  
		Last Modified: Tue, 13 Feb 2024 01:57:32 GMT  
		Size: 3.6 MB (3560691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bae34dfeea0297b2412b07a36c2199c89541717e4d7f86ef7d8eb35df4a1dab1`  
		Last Modified: Tue, 13 Feb 2024 01:57:33 GMT  
		Size: 23.6 KB (23569 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:60abcf5427c943e15e55681c49e4c60591c838f6c8e3a87620585e5a4b5cac3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73041740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3983cf27f966fafa772672234ad02e605db08d5352f9bb38f96b3c24091288d4`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 07 Feb 2024 00:26:58 GMT
ADD file:aec249f679ecc1ccad460833afd79f8f10ccd9378d1275ed1f23fa98cf3f99b6 in / 
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c99d8d33768bdc2aba62f6b3cc956b807c30b43339ac2ffa3db52a47112dd416`  
		Last Modified: Tue, 13 Feb 2024 02:16:36 GMT  
		Size: 29.6 MB (29640432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c401c3f98194fa1cb075ab91361dc01555d5d42de57de76cdc76c6e785c68d0a`  
		Last Modified: Thu, 15 Feb 2024 06:31:02 GMT  
		Size: 9.8 MB (9833931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da743a13ec9fb26974a9367cac435640a3c8a96610f41ec5eaaf6bf6ba0c1987`  
		Last Modified: Thu, 15 Feb 2024 06:31:01 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654f17d1605be2b7f0668180bc8c3c140dc1be337fe67d9e3b4063ff8d43626d`  
		Last Modified: Thu, 15 Feb 2024 06:31:05 GMT  
		Size: 33.6 MB (33567035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c5682c19c7b3d7666fff7074445cbeb6d3c9a4e53bf3ee42df9061e12af333`  
		Last Modified: Thu, 15 Feb 2024 06:31:02 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:9b932e0e2ea6849304ff30251aeb2706e8e7777648b0e8f2c44f50757246565b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 KB (23283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a727bf5a89f8f3773d2e590b897da69037c09144fc8690c1a367f9ccbee54e`

```dockerfile
```

-	Layers:
	-	`sha256:e9175432bcca017499b80e317909aa6ea3a638be6aa3415935f0a689f132a983`  
		Last Modified: Thu, 15 Feb 2024 06:31:01 GMT  
		Size: 23.3 KB (23283 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:fd31c1084ea698c2115b5646665a4ec5d3de692fe1f2d18797905273157fbe24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79701162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4059a750a4de46aab8f23bbae4090f877ac2b033f0030859bab75125027c04`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 07 Feb 2024 00:26:58 GMT
ADD file:f8e53a63f5fbfb32b4bac66dc2b16f2e2d101e5feb6cd9e3b6d3065fb8aee14d in / 
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5c87ba6a2e42f083a6cfdea0d3b1b3bc977a5065ff0087fdbf4fc8dbc7982a38`  
		Last Modified: Tue, 13 Feb 2024 00:44:50 GMT  
		Size: 35.3 MB (35297799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2643e4e06fe71f452e4298b49d63c37ea9b10701eb01ccf9775c017a8d73831`  
		Last Modified: Wed, 14 Feb 2024 04:42:48 GMT  
		Size: 10.5 MB (10479507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa588bcd76b4962e69ab665cf8bb4e6d06fc6aa058863b16292a7c1c9942e66d`  
		Last Modified: Wed, 14 Feb 2024 04:42:47 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432c4595d3114c4ab011819cb499554e9d6901a6389e368fdbfe4b33f913cd15`  
		Last Modified: Wed, 14 Feb 2024 04:42:49 GMT  
		Size: 33.9 MB (33923515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12bd49981f1d7ac28d83a3d7d6858e8fd0d8f4d8b97a8d71ab4d134eadf7d5a2`  
		Last Modified: Wed, 14 Feb 2024 04:42:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:459b4986b77ba0699b0dc8203de72964d47d99c780c7014a3e5132d7791e2023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079f8ec98c80dd9c6900659052ca093f34c0ac60fb35c70334dd00d30a612418`

```dockerfile
```

-	Layers:
	-	`sha256:00a8f7444e5da4f9a0d302be25d3c98ee1e7cc11621862dc5fbf8b1e6f7250c2`  
		Last Modified: Wed, 14 Feb 2024 04:42:48 GMT  
		Size: 3.5 MB (3548773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c288a0b880128da158cf31a85550022e78e5d8d9d29123fb34af274454fbced1`  
		Last Modified: Wed, 14 Feb 2024 04:42:47 GMT  
		Size: 23.5 KB (23481 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:67b79b947d9db76220d13436f7afa3ab8167d8368699c2a125048e7d9ebfba6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72033182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8627ceaa7530be411903a919fbd26dc903f716667ab06b97459b008c8d56305`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 07 Feb 2024 00:26:58 GMT
ADD file:08d247ddc5feae7a34870daaf7096c41de9c1bb9fc04bc305db02fe94b34d2e5 in / 
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["bash"]
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV LANG=C.UTF-8
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_VERSION=3.3.0
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Wed, 07 Feb 2024 00:26:58 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Wed, 07 Feb 2024 00:26:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 07 Feb 2024 00:26:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Feb 2024 00:26:58 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 07 Feb 2024 00:26:58 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2ac5fae051fa0d97737a12baa9ac705d62ae16e9a4ae39eed54e3f977616ce05`  
		Last Modified: Tue, 13 Feb 2024 01:30:53 GMT  
		Size: 29.7 MB (29660168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f258da6cceecf5c0f7ccc2c92bc9661c5707ddc2d08dc3b54f9644f30df2dc`  
		Last Modified: Thu, 15 Feb 2024 17:55:48 GMT  
		Size: 8.9 MB (8860667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0bbe743c4c86dfe8406ae6e1ae48dd2188e11d67401106b7cdd68fc0d88ca94`  
		Last Modified: Thu, 15 Feb 2024 17:55:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e79fab511f62707bc08a11db5cc77cd490525490c12e4ae611709cb4ad74442`  
		Last Modified: Thu, 15 Feb 2024 17:55:48 GMT  
		Size: 33.5 MB (33512006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e9add73cc48c770aa8d2a5fb86eb1a97e80600214647bb2dd75575a7c2f2c7`  
		Last Modified: Thu, 15 Feb 2024 17:55:48 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:4e7af151adcac6a159a85fa9c913f0846fa3887bfbc30ce2376afb991b4425c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3570931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6580adc464ce52696090078a8abcc1cbeae4affa6e0dc3b32e7082c6427eadb7`

```dockerfile
```

-	Layers:
	-	`sha256:ab4ad822adfa505b263ad24ee68b4bbe3b84852c123c94620ed28d1105fc580e`  
		Last Modified: Thu, 15 Feb 2024 17:55:48 GMT  
		Size: 3.5 MB (3547500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:941031f4c9b2bfea033a1801a42451a0a3a041da8ef1b1afd0b58071e44c7962`  
		Last Modified: Thu, 15 Feb 2024 17:55:48 GMT  
		Size: 23.4 KB (23431 bytes)  
		MIME: application/vnd.in-toto+json
