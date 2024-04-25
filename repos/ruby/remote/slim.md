## `ruby:slim`

```console
$ docker pull ruby@sha256:4588f64e228e6ce36706b8d1ced410142b2652da40f0ee035f08da25bbf17409
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

### `ruby:slim` - linux; amd64

```console
$ docker pull ruby@sha256:454d42098318ff7ce066f4ab2a2ef4367918073f60b44e5afce103e31a6b613a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79125520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e332019d358562417c1cefc72839e9ab6167da0e84e7e40a326977d04e1b0a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.3.1
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0686941a3ec395a15ae2a852487b2a88e5fb8a5518e188df00d8d1bb71a6349b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184ad629b9ce80fa8a4a895c0c63c5dc390358a94e889918dc90a0502e00c127`  
		Last Modified: Wed, 24 Apr 2024 05:11:26 GMT  
		Size: 13.7 MB (13657825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cec1be417e55d0e980812909796b644b94e1c620f2666a221e7fa8eadcc4c7c`  
		Last Modified: Wed, 24 Apr 2024 05:11:26 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c20a04120ec7b7a6fc3eb5db2eeee7b7d981a8906d53fcf95238e434f8d10d`  
		Last Modified: Wed, 24 Apr 2024 05:11:27 GMT  
		Size: 36.3 MB (36316873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a163c8b0195c13c9f48dd5adfe2c0e228e9a5e1728afdfd42f48032ab4ea1d29`  
		Last Modified: Wed, 24 Apr 2024 05:11:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:084769487ee6457f1fa2d0bce35b05883cdc45a78cc347d656eae9d840f045e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3887694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97e6e7199fa8288cda28536d1ec94523f0778a98c82033af875ad9d18c57a7b`

```dockerfile
```

-	Layers:
	-	`sha256:d9d529b6381f165061aaeaeffbc4a763be1363454ff7c653de8ee120ca77faf8`  
		Last Modified: Wed, 24 Apr 2024 05:11:27 GMT  
		Size: 3.9 MB (3862873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8e62e1df2222257a57f8822baf3180bb2acb25b564d396e670f9e59b3de78fb`  
		Last Modified: Wed, 24 Apr 2024 05:11:26 GMT  
		Size: 24.8 KB (24821 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:ad12968feaef5a3e669c6eb8f59bcd5366cc4a5751289930d76251a792622e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71072873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad53d7d294f54e177241aa73c5dcfd34ff0a9d3eb3dc0e2c93cb01d8f66ddfa6`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.3.1
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0686941a3ec395a15ae2a852487b2a88e5fb8a5518e188df00d8d1bb71a6349b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce0d8daca6dd823c875685e21d5b1a3370eff7592c11024d5d631342aa43e8b`  
		Last Modified: Wed, 24 Apr 2024 23:55:49 GMT  
		Size: 11.4 MB (11414688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a9baf8c4d252126c82f93d597293913a5091a1ec6952aa01a3b04f4a1ca7aa`  
		Last Modified: Wed, 24 Apr 2024 23:55:48 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a8d3657cd026248f2479dd1768f429c3770e95f48e18656ade5fc7279484df`  
		Last Modified: Wed, 24 Apr 2024 23:55:50 GMT  
		Size: 32.7 MB (32747814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20376f29c8e3e025064732dcdf8f0dad30075766af659c20b39b627e024e2c83`  
		Last Modified: Wed, 24 Apr 2024 23:55:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:e440387aec2f2fdab9567e014efe1b2251a32c25556c64eb8001661f7c8242c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3857966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ffe3dae3f86965bb0b19a5d280d2332f930c55221a636d612d4af11c01f526`

```dockerfile
```

-	Layers:
	-	`sha256:d74c516a1771947ee0bfc3c2152cbc353d5cc577dfb185053077cfe7f1e3e685`  
		Last Modified: Wed, 24 Apr 2024 23:55:49 GMT  
		Size: 3.8 MB (3833171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d654f9a0cdc02eeab428ba4090b4ea9e45b05cc957712ce8a5a4d8d257d33db0`  
		Last Modified: Wed, 24 Apr 2024 23:55:48 GMT  
		Size: 24.8 KB (24795 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:29b08a1237e119b5d3c7687ac0bfcaf29a25102138f226f4bca17ea8d0df3541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68117990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17004951f69a60f2191159700d729f54f95b11e61fef91829b406e36e2240478`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.3.1
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0686941a3ec395a15ae2a852487b2a88e5fb8a5518e188df00d8d1bb71a6349b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc47ccfa8557f9a06a010e319316c7ef656e743f109a166be263e3eb468b8b73`  
		Last Modified: Wed, 24 Apr 2024 23:41:28 GMT  
		Size: 10.8 MB (10753023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef82d351ab736db5b88651cc5d2d237c795e5bb13c49d2db3beeb4bfa7a47b17`  
		Last Modified: Wed, 24 Apr 2024 23:41:28 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507e408a8619ea84eed3b5eaf028ecdfea22537d5ce17f56708c4d24ffbee989`  
		Last Modified: Wed, 24 Apr 2024 23:41:29 GMT  
		Size: 32.6 MB (32624181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba57f2147e5c4ebef7ea9ff9076213c4b3f472ad00fe0eca2db6af0fbdc5953e`  
		Last Modified: Wed, 24 Apr 2024 23:41:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:de1a1aadb57768aa6f732917f6dca63751c3f357b79a2a5053e245b378bda2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3857762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6092c1334a8692d7a22140f5dc0b9a2ce9d08ebb64c5a56f1a32cdd7d5170f0`

```dockerfile
```

-	Layers:
	-	`sha256:ebc3ebbe25b63497f3560fc75e4c90d2ec6b02571f34e27ee5d7fec43ffb651f`  
		Last Modified: Wed, 24 Apr 2024 23:41:28 GMT  
		Size: 3.8 MB (3832967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed8a4d94b5ea3e89c7e57157a54b445d9a0b1cc84c983a66117bcee1ec99600`  
		Last Modified: Wed, 24 Apr 2024 23:41:28 GMT  
		Size: 24.8 KB (24795 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:96bf204622dca624da6da502979c0dd1493f85813b90ca0e0c396050325829a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78029785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f32ec0d88d38774354b2ed373591945d933c8bd02228327fc01f7a0107d3d5d`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.3.1
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0686941a3ec395a15ae2a852487b2a88e5fb8a5518e188df00d8d1bb71a6349b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cd60c1d2b545dbe2c10439e6215af14355a2749e2c983dfef7d3db00f867b1`  
		Last Modified: Thu, 25 Apr 2024 15:41:46 GMT  
		Size: 12.5 MB (12500309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b90ec0aaef9170a29a216d7e1ea6f1452fe0ff679b52c9c83eb118fa0307a4`  
		Last Modified: Thu, 25 Apr 2024 15:41:45 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dad7f104e012810f8cb542bb08ed5fb257b9c7ae92ea2e98e4339f04323085`  
		Last Modified: Thu, 25 Apr 2024 15:41:47 GMT  
		Size: 36.3 MB (36349197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a740df710a7bd8a239aff81e66d53fafccd823c0efa87b69dcbd4ff5e1d01ff1`  
		Last Modified: Thu, 25 Apr 2024 15:41:45 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:716132183718f1e8813afda3902b9c488f7a8dd47b49e7b1c2300d619948c3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bfcf4dff519825de7239876142b6d334c3c57746c106b6fc69eab3cbf19bda`

```dockerfile
```

-	Layers:
	-	`sha256:19e9a96bbb5a4d3c7423d92205218fe97b4599ec142c493d6b8b478f368d6d31`  
		Last Modified: Thu, 25 Apr 2024 15:41:46 GMT  
		Size: 3.8 MB (3834054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5639e2d2b9bfec112c00012c39bc5d89ca842d9ae1301409c9370e4c20db1c3`  
		Last Modified: Thu, 25 Apr 2024 15:41:45 GMT  
		Size: 24.7 KB (24672 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; 386

```console
$ docker pull ruby@sha256:70f9940e50556f128bc897db1880c58d9430e178a499bd88955318861a4e932d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75913056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8006e5e4fcbb53184f391cbf38189d003a71ecd1b95a0b20b7034eacf64123`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.3.1
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0686941a3ec395a15ae2a852487b2a88e5fb8a5518e188df00d8d1bb71a6349b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af90fae5ea15ec148e26d9c7feeec27fb72ae380b1607f009f9a7728ce31b1a`  
		Last Modified: Wed, 24 Apr 2024 05:11:46 GMT  
		Size: 13.2 MB (13207785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1dabd280ed9155f8fa97373087c63237f82987825ae3701ace3c472563ae6e`  
		Last Modified: Wed, 24 Apr 2024 05:11:40 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9a16b31b3394881a234e27a5e4b90d8c9ba0d8a5b34d19575cc0c59bdb8ed5`  
		Last Modified: Wed, 24 Apr 2024 05:11:46 GMT  
		Size: 32.5 MB (32541744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e1489745cb389ad8f3c46464af552a706d66619208eb948ed059ba18d6ff6f`  
		Last Modified: Wed, 24 Apr 2024 05:11:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:9768aa69ee0de488e61dab1b303035d9a6b414590e39f1170d02c8ea950cf766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3881477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b836883844778793741525a80106b3281755722a911bc9f5ef390971c1cac7`

```dockerfile
```

-	Layers:
	-	`sha256:e7a1cfdc757f4abf04531d6bfbac9c65c4b94375978a169f340093e0957496fd`  
		Last Modified: Wed, 24 Apr 2024 05:11:45 GMT  
		Size: 3.9 MB (3856711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:022bc0cb96e13d0a278d6186e7d2db839be260cb495b432a4067bf681e08fb79`  
		Last Modified: Wed, 24 Apr 2024 05:11:45 GMT  
		Size: 24.8 KB (24766 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; mips64le

```console
$ docker pull ruby@sha256:f762ec6f164eb2075a8e4ec26db0bb7efceeea8989c63ebbd26c6b1cfea4f988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81604801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bde3cb5686101336c35c884d99a4a6640962290c6f7b1928bb14359438fea9b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Apr 2024 01:10:04 GMT
ADD file:c07831a1f2abb22986c788bb198b484a259e7e68ee8b03da0daeb4b41d8d83ce in / 
# Wed, 10 Apr 2024 01:10:09 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.3.1
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0686941a3ec395a15ae2a852487b2a88e5fb8a5518e188df00d8d1bb71a6349b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a99180cf1634aa211024be7ce3258cac9c0823e82f09b97870da9d9b21ea68ca`  
		Last Modified: Wed, 10 Apr 2024 01:21:58 GMT  
		Size: 29.1 MB (29124665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e1d7084fa473284ee4888b4538e37285f27f2b56222f102c79899d109273fa`  
		Last Modified: Tue, 23 Apr 2024 17:26:08 GMT  
		Size: 18.7 MB (18713230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c39c2d714f47db1b2b697056fe78524a01306ccb84d8f42b399e3fafef3278d`  
		Last Modified: Tue, 23 Apr 2024 17:26:06 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9949d5874f4e3a05f4fed0b3f7d3468c8f1cf7e7dd4a0ced1750da8d0eb8fd`  
		Last Modified: Tue, 23 Apr 2024 17:26:10 GMT  
		Size: 33.8 MB (33766564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08da34de90ceb75bd90b6e307de08569395483331598b8918ef5ccda1b965d96`  
		Last Modified: Tue, 23 Apr 2024 17:26:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:a5bf712ce7ff524e103fddc73e667a1c8b1c4dc416c6bd5c7c6a85c598d16ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcf76602d4d4ffb570b6da478fd00755380fb74dae08fa0dc8770301afda5cb`

```dockerfile
```

-	Layers:
	-	`sha256:1255f1267f3e368119f65aced983d19ebe7d7c65ff8a4781f77cb2b95ed07db5`  
		Last Modified: Tue, 23 Apr 2024 17:26:06 GMT  
		Size: 24.7 KB (24704 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:ebb189f170be87f2fdef8ef92ec71f91c4eb3ace5603b3a91a2a4c7292f50948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81662083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d73d59748e996733e7206da2f468dfe0e11d1688c7a5e7420dc224cdbb04c9`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.3.1
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0686941a3ec395a15ae2a852487b2a88e5fb8a5518e188df00d8d1bb71a6349b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c793d842270657a0c983a75e1700e71bc459e9519a8dfcf4ceb56ea892c81b`  
		Last Modified: Thu, 25 Apr 2024 08:31:11 GMT  
		Size: 14.4 MB (14379781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b995b7f0d0a2213bd8d9883eb14646b6d1daba2a3c680814e12491b3aeab7e3`  
		Last Modified: Thu, 25 Apr 2024 08:31:10 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6defd997c93253ced74f4d4bf6fd19c8399e3f41f561bf27841950e7bc0a7447`  
		Last Modified: Thu, 25 Apr 2024 08:31:12 GMT  
		Size: 34.1 MB (34140759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0afbee22638df96ed65c4b8cdac8483ca79ccf943352411e815a77844a183f7`  
		Last Modified: Thu, 25 Apr 2024 08:31:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:e55cd8ba6145ec16a1bc9c59b6a5274d126ad8bec29c6b14fa35e8f08f6d0f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3873418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa3a72493dca0bb526f6766bee3814ff167b8243718a3eac6c6e0ff7f2763a0`

```dockerfile
```

-	Layers:
	-	`sha256:1e8bccc660921448c32aa02ca32525922e3a3ea313a842129fbb6be70435068c`  
		Last Modified: Thu, 25 Apr 2024 08:31:10 GMT  
		Size: 3.8 MB (3848697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01f3cd8a4dbc1fd32138f7e403ad03c737efa7673b770c0db43f4e132553dcb`  
		Last Modified: Thu, 25 Apr 2024 08:31:10 GMT  
		Size: 24.7 KB (24721 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim` - linux; s390x

```console
$ docker pull ruby@sha256:94ae12365573c770121fc654389f7d99683b2ace7b83fd64836b183119519c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72735710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee46842f7651075ea68c74cbdfc7816be839f2a039d8902375596292481cf795`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 23 Apr 2024 15:14:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["bash"]
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV LANG=C.UTF-8
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_VERSION=3.3.1
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.1.tar.xz
# Tue, 23 Apr 2024 15:14:18 GMT
ENV RUBY_DOWNLOAD_SHA256=0686941a3ec395a15ae2a852487b2a88e5fb8a5518e188df00d8d1bb71a6349b
# Tue, 23 Apr 2024 15:14:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 23 Apr 2024 15:14:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 15:14:18 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Tue, 23 Apr 2024 15:14:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591a904e1b4f23aebba8e417eb670c1bd4d6703d5a1d9bb5e8cd163ad429bbe3`  
		Last Modified: Thu, 25 Apr 2024 08:47:34 GMT  
		Size: 11.8 MB (11832584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e32ce10cf740d787606c1c7ba7d44ab324de29d20d1e832d57cd1ff5bf29473`  
		Last Modified: Thu, 25 Apr 2024 08:47:33 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbded9079b1301b2bbad1fe48423b11e6043a53f28cd10447963cdcf979a2b23`  
		Last Modified: Thu, 25 Apr 2024 08:47:34 GMT  
		Size: 33.4 MB (33390429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0272501845910c3a340b35999c4a83253e4afeaa2f48bf1daedae409ddab5a`  
		Last Modified: Thu, 25 Apr 2024 08:47:33 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim` - unknown; unknown

```console
$ docker pull ruby@sha256:354a52846d167205391237defba0a4a88cc1848b1066bcb694a59ac7234773b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3875778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e440dce2f08bfeac26a53f51ae81d4827f5ce7f978395bebdec02886da041bde`

```dockerfile
```

-	Layers:
	-	`sha256:c2c20c016915590eb7c779cd30dedf6c6ed7501835d8d82eb8594ca5e7b0f08c`  
		Last Modified: Thu, 25 Apr 2024 08:47:33 GMT  
		Size: 3.9 MB (3851124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a14244a9f09795d3338debe0a06a584ae5b073e10cc6a0499c035c5ad74b382`  
		Last Modified: Thu, 25 Apr 2024 08:47:33 GMT  
		Size: 24.7 KB (24654 bytes)  
		MIME: application/vnd.in-toto+json
