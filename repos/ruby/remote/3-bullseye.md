## `ruby:3-bullseye`

```console
$ docker pull ruby@sha256:3ec9044427d53699c7f40e4ba5c209553cf5b8c5a03f3672f1916b1736168b9e
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

### `ruby:3-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:b654c5e33be6f881a0697a90a2d9b59c38e0bae8bdf602c7fcb5b135de4a2833
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358804188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432962ce313fe662264ce4e95ddd2a58fa523191698de93983916bc5ec6304ea`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:57:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6043113e1c69109f845390049c3534bbf0249241ce681aafd8e6d4bc4306dcb2`  
		Last Modified: Tue, 14 May 2024 03:06:01 GMT  
		Size: 197.0 MB (197014118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a8acc752736ead4114639ae77467ad614d1a3ae4449c2018f47ac48536eae`  
		Last Modified: Thu, 30 May 2024 23:59:29 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe1dc769e971f73d12310737bd5096728bc44a5f3ec8c1a2c93dd8b51c573c2`  
		Last Modified: Thu, 30 May 2024 23:59:31 GMT  
		Size: 36.3 MB (36335857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb855771ef369f170892e1588a46eaf0e68b233eedbb564bd71458d4b874efb3`  
		Last Modified: Thu, 30 May 2024 23:59:30 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:03abffe7fa11dd91c96d97d8ddd79c6dca6e9f751a15c8f918c6afc748a4b598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15088767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a29c9424c9b9d9c875fd96a0351be8af524503a8451051b878e53f4322630ac2`

```dockerfile
```

-	Layers:
	-	`sha256:9f9c3c6c1d0e56e0ab126baa985fa3bc35a0a30d432457788742198d533013ef`  
		Last Modified: Thu, 30 May 2024 23:59:31 GMT  
		Size: 15.1 MB (15066583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0feb23ad0b98fa356f93dbd9c86b6ffc89b827c138a8cbd9de66fdec2208a983`  
		Last Modified: Thu, 30 May 2024 23:59:29 GMT  
		Size: 22.2 KB (22184 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:7fd54a27dc7ca2c71e8f6325b02042e67f9ccf91f617f1038f9505fbd4271624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327928892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc293574fc8ad772151592f99cf3653839163261a186e48dcae45a16a3e189a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:48:42 GMT
ADD file:74e1eadc44e9ed60fef85028d1af7cc94cf71327c3173769ec9d74b29e4e19c6 in / 
# Tue, 14 May 2024 00:48:43 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:13:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:16:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:bf31f3332f7a686a69b7a5dd4c95c8f289bd767f54d9be178626f04a40b1d56b`  
		Last Modified: Tue, 14 May 2024 00:51:55 GMT  
		Size: 52.6 MB (52602710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62dd30089ebb575f8eaa5d60cef9d41adabaed93cb054f7b1db47072859eb02`  
		Last Modified: Tue, 14 May 2024 01:23:00 GMT  
		Size: 15.4 MB (15376278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236e767fe9ffe05ea096e155f4751d0f234211ef6dae223a22f311a6d8c2060`  
		Last Modified: Tue, 14 May 2024 01:23:17 GMT  
		Size: 52.3 MB (52330199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31197eac3efc2f96a29f1e2fee22a1ee86df97c3fbfba3e488f95d5c9fa67bb1`  
		Last Modified: Tue, 14 May 2024 01:23:51 GMT  
		Size: 175.2 MB (175212599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ddac6f8c4367d393997c4acd7cb478de63ea4ed7dd76b4f08561c074faed3d`  
		Last Modified: Wed, 29 May 2024 23:21:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e73d2971de10a433d0133e54e88cc1d3517b38ecaa8e9c1e97aef040f55299`  
		Last Modified: Fri, 31 May 2024 00:10:56 GMT  
		Size: 32.4 MB (32406767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9dc96c8f7c34252b1776821918dd6a5d72b8c04421563ca7fc59b4971a20a6`  
		Last Modified: Fri, 31 May 2024 00:10:55 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:f4e92bde62e809ae29ac2b26b4be81638e4d7381a550b5246bb18b81fa098070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181f2b104906e45199a0e1c4a865decc7df4caedccc7a68bca15a0bdf3b07fb8`

```dockerfile
```

-	Layers:
	-	`sha256:b9fd7ddda3380b96bc24d592f42230379c12611d00adec0e29692063acd29d2d`  
		Last Modified: Fri, 31 May 2024 00:10:55 GMT  
		Size: 14.9 MB (14863093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f3acb7fb56c8bac12d6658e8a677a2fdb29f32169ada52b17d29036e454625`  
		Last Modified: Fri, 31 May 2024 00:10:54 GMT  
		Size: 22.3 KB (22280 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:078dc865cbef221f220feaaae49f9a3a534b8bba82b1a33c44c032aa0cf52edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.3 MB (315289156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda6165e733ec9f2f2ab9087018b606ecdfcae36567a762ccc260945b2554d0d`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:08:54 GMT
ADD file:e0e66bc918a84b9ec6caaae1380270276be179a5864b6234a18c001b3e94f855 in / 
# Tue, 14 May 2024 01:08:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:37:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:38:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:ebc97a184476667a6a83dfc0759e34e05bc66d258ece39a010b6273982b4dc57`  
		Last Modified: Tue, 14 May 2024 01:13:05 GMT  
		Size: 50.3 MB (50256445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f46483bc34de5be97fb9e8af88e9cf41c36db4eecccc529cc7904ee92a32f72`  
		Last Modified: Tue, 14 May 2024 01:48:02 GMT  
		Size: 14.9 MB (14880295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d6f4b9983a8ee98e2432d49e727c6278cadb8efecf5ab79268999b8d08c984`  
		Last Modified: Tue, 14 May 2024 01:48:20 GMT  
		Size: 50.4 MB (50359447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b75020cd82336d3062778f825587beaa94285a03f3e7cdf28704af4743b57a`  
		Last Modified: Tue, 14 May 2024 01:48:55 GMT  
		Size: 167.5 MB (167476287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae1c2cb90f324ce39bb06722c667b42ae1372e8834e5fd9fef4a7cdb3a3032e`  
		Last Modified: Thu, 30 May 2024 03:43:20 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69dad9d7e9a2cb517114d00a643e2f3455db87afd34fb943deb5de158df0f8c`  
		Last Modified: Fri, 31 May 2024 00:48:01 GMT  
		Size: 32.3 MB (32316341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a6218d8c867f7a34c59a256131d2f70fe744476a04c060ee93cdc7b6ee91d2`  
		Last Modified: Fri, 31 May 2024 00:48:00 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:3c1f5b982ece11d6b8139ee11cae76da22ee4bc777da7a4c7dd7d01bc19479d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6112ed831d4ce79d93fed15d8408293c201ee0080e2dff911ac2861a7cb545`

```dockerfile
```

-	Layers:
	-	`sha256:33441c6b332dff9c6bd14d4be83c25336d34078bf13de9d4c16ef60f3574eebd`  
		Last Modified: Fri, 31 May 2024 00:48:01 GMT  
		Size: 14.9 MB (14868467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1983ec64794dcdba36c43ebaaa872607a5bdcfc3b959b66d949af751957ee753`  
		Last Modified: Fri, 31 May 2024 00:48:00 GMT  
		Size: 22.3 KB (22280 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:474e0aa35168d7f02412232a843a357f1f3768e4353928f4ba7f48add9180dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.4 MB (350373041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03e82462474e61be9fbccb961b4e4d4e700c9f0224bb6f47ec2bfb9e7755b82`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:45:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:46:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:46:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691cb555e773cb93573d3bc043d7cf17af1d4819163089dfddab3f4cc971718e`  
		Last Modified: Tue, 14 May 2024 01:53:53 GMT  
		Size: 15.8 MB (15750525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dce352085291a4828eefe3a8fe5557c610cb7e308cbe4a56a62e0922171dc1c`  
		Last Modified: Tue, 14 May 2024 01:54:08 GMT  
		Size: 54.7 MB (54696093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9dcef9945e6cc16f20fb350f760e6d9f98378b467040f7a00ac783d81334031`  
		Last Modified: Tue, 14 May 2024 01:54:32 GMT  
		Size: 189.9 MB (189936403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa7521b23ca44d2c7934a3a7e622f62cce1966e8e3e6a083f81adeb8706799d`  
		Last Modified: Fri, 31 May 2024 16:39:56 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595e0a4feae44776de16c6411ee15b87d958da848d49706d831fa67b562e64ee`  
		Last Modified: Fri, 31 May 2024 16:39:58 GMT  
		Size: 36.3 MB (36250690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cd0586bd5bb31f9272d06c68251e1dbc1c198aea6fa5fef02b1fb17fd2def4`  
		Last Modified: Fri, 31 May 2024 16:39:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:425041e75b9c77fd3cacd7fd6ebbdbc1c2d232ce4223191a4786eb1638f56059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15091587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25816a8b646cd17d934cd95bccede4159051c55670989e6b95f96e82a73a6ef2`

```dockerfile
```

-	Layers:
	-	`sha256:3cda20c6e2bbe3f99ddc5c4f7302bb076ee1530a845097d979cd7c4e02dce9f2`  
		Last Modified: Fri, 31 May 2024 16:39:58 GMT  
		Size: 15.1 MB (15069091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa693222423573341b2449bc4d35def792f8ce92cb3567f79b568a3f559d879`  
		Last Modified: Fri, 31 May 2024 16:39:57 GMT  
		Size: 22.5 KB (22496 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:7b7a2e02166c0408700cced4153d2bf156c800b72a7d34c683af2e3eb151f5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.6 MB (360582825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191b584db1df6f2b28622adbadc90080a9b7dc03381d065b368f39d0e9cd451a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:47:22 GMT
ADD file:052f086288480e72435d634b2bf07198eb86bd50d8625c576e50f1c86e39f537 in / 
# Tue, 14 May 2024 00:47:23 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:03:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:03:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:04:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:e2ec811b59a6f77ebbb7b1faa7ee83a70e39a8f7628970c01799c727a412a1ca`  
		Last Modified: Tue, 14 May 2024 00:52:20 GMT  
		Size: 56.1 MB (56076057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182e16878498082da3be413141adb855109c55626d0485b6aafb79e1cbdc5474`  
		Last Modified: Tue, 14 May 2024 09:14:33 GMT  
		Size: 16.3 MB (16268989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45622f6623917a1133bbaccf5f0fa4ae87c3ed7e9cbdcb259e65485804757c02`  
		Last Modified: Tue, 14 May 2024 09:14:54 GMT  
		Size: 55.9 MB (55929438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584614a415369245291ab36f58dddbdd2da056a8b7929f7069c0a8d75f68b86a`  
		Last Modified: Tue, 14 May 2024 09:15:41 GMT  
		Size: 199.9 MB (199916723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599357f101be12fc05dad1f81fbcc29d03bd81bb8e62f0079ee0ca64c1909b0e`  
		Last Modified: Thu, 30 May 2024 23:59:18 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c49fe2e11e255572cf72106013e7d666ee74971221fadb81c5caa4ba0a1b86`  
		Last Modified: Thu, 30 May 2024 23:59:24 GMT  
		Size: 32.4 MB (32391278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffa949f0c8bbbc6cdad3cc1738bdbb25fbe063e681bb919f777fc5c45dbef73`  
		Last Modified: Thu, 30 May 2024 23:59:23 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:aec3faefe0702343510a8ae0f8569c056bf0d18f4e5567d9a38fbccd8f3195dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15077563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e8fa5d09c7d8404d79caa43d24942354c4ca163e724648730c192176a413dc`

```dockerfile
```

-	Layers:
	-	`sha256:3d81e4738931976fdffd7641c6718be3aeac4946405ef5a9397532b9b1c135f9`  
		Last Modified: Thu, 30 May 2024 23:59:23 GMT  
		Size: 15.1 MB (15055412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:736e996e6a8c7c25ffe6058f378c84421ce8a54be96b68c3f96bb3d36c2e38c3`  
		Last Modified: Thu, 30 May 2024 23:59:23 GMT  
		Size: 22.2 KB (22151 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:95cfec8f49b71d5c9741152a416e8f2eeb8ce5b4993b0edd904899260488fb31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.0 MB (335020770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229939d222893882ff1265379e5d9631479a30edc05f28a9214f2715ac1c9265`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:11:41 GMT
ADD file:21c5796082f318cf57901c774792fb836e16ed2e984bfd93de345b83005884b5 in / 
# Tue, 14 May 2024 01:11:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:08:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:10:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:15:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:fc8239cb1934c4e9e9368d2009f62f73698f5ad0167ec8a7f5128c5b24848b49`  
		Last Modified: Tue, 14 May 2024 01:23:03 GMT  
		Size: 53.3 MB (53322052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae485d7e63e18bea6220a5c2d4a706379e1cf701af08f3d2bc40119bd3dd7ae5`  
		Last Modified: Tue, 14 May 2024 11:40:25 GMT  
		Size: 15.5 MB (15530346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1b7741bff2a58b71ac6371e1fbf6f9dcb366c82fb6243829c330c2a13b5037`  
		Last Modified: Tue, 14 May 2024 11:41:09 GMT  
		Size: 53.3 MB (53312597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a5c693cc8c99f19e173787a1971e0d4a76aa939dbd2b62fe612add7ec9c0e7`  
		Last Modified: Tue, 14 May 2024 11:43:06 GMT  
		Size: 179.1 MB (179132072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b02acee6d51d2bf1ca3abc1db5a5efbbee80775e2500052ced5ed203d76146e`  
		Last Modified: Fri, 31 May 2024 02:41:29 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2a605205106480c603a08279884c5f261b30c55f2affd89a3bca12d8a2d7c8`  
		Last Modified: Fri, 31 May 2024 02:41:33 GMT  
		Size: 33.7 MB (33723362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c210722111b81ff00d03f9776cf29b4a9fe342f398fdfa420979cbe54423889a`  
		Last Modified: Fri, 31 May 2024 02:41:29 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:727cb003601b2ddabf3b6f9f0c81f8d59b02bf9cb2293427fb68506fbb3c8314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 KB (22027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c164595da4bc5e6e631d0543e2b697642e8623ccc34fc342e275a1e14811813e`

```dockerfile
```

-	Layers:
	-	`sha256:66d37cb1a742d7353796bf35ae8c691b06bf0d03c0815629b489191003c863f2`  
		Last Modified: Fri, 31 May 2024 02:41:29 GMT  
		Size: 22.0 KB (22027 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:2d324e57b183e1caa8bf82941c5a2fd0867aabdc7eaa8cc33821797cc2a80983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.1 MB (365052291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27340afa09e8b96f438239a6cbb921b8b23798670f4feaeb57e4cd426a5b43f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:20:13 GMT
ADD file:4b54ed39e81b5ea585c47d145304cf7a54b08e7b1ac284a533f59d1a4768da9b in / 
# Tue, 14 May 2024 01:20:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:58:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 07:01:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:d13e42d2790e01b63e6e5f051b276a525e360366071e8144b80a7a814c950f7a`  
		Last Modified: Tue, 14 May 2024 01:24:27 GMT  
		Size: 59.0 MB (58969434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe3151b57b060a2fe0ca52c8936b461c9e0545bc85c0c2eb5f57ea98c7a94a`  
		Last Modified: Tue, 14 May 2024 07:11:41 GMT  
		Size: 16.8 MB (16766925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435512f1cbc8e07bb0a635d32fa068bcf448922bef667d36de93d14ae1a1efaf`  
		Last Modified: Tue, 14 May 2024 07:12:00 GMT  
		Size: 58.9 MB (58873785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d0e9056be49b56fb034ae67015f749411fff8fbd5b427d798c9847f60a8251`  
		Last Modified: Tue, 14 May 2024 07:12:37 GMT  
		Size: 196.4 MB (196363387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441eb7cdcfbe8fbb426f6dafb62a0e93461fe81c33decbb74bf0e261cc58e7fa`  
		Last Modified: Thu, 30 May 2024 03:27:52 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6665fcb84e52f5863c3704a3abc45f7a541fee03625f0c169cc9ebc9f3651dbb`  
		Last Modified: Fri, 31 May 2024 01:48:41 GMT  
		Size: 34.1 MB (34078419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdc61191f97afcd4ea1c9fbf1716a08ff38f6e84ed7ec4145a7e76be9160ce6`  
		Last Modified: Fri, 31 May 2024 01:48:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:82b912021c88d6707dea0f08523637ae47193bd7f991228660c4be3484bccf66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15058111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf3807baafcdc05ea92915ed9272a2b7aefdb9365f987f2a4697b778eca86ae`

```dockerfile
```

-	Layers:
	-	`sha256:2723dffffccfb5c185a5b35209c5e3b4d536848507f5bcf29112d10d31f1b5e5`  
		Last Modified: Fri, 31 May 2024 01:48:41 GMT  
		Size: 15.0 MB (15035885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6a8de9f48462df08724b84f7db7a70a58c9ada60e2878ddeb5d495e3e2ac1a`  
		Last Modified: Fri, 31 May 2024 01:48:40 GMT  
		Size: 22.2 KB (22226 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:e987bec9c83f8c4aa758f1b32612fd86824ec9f551478d4ae30993ae42c74486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.8 MB (329757005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1dd41cda91dc64768b5b71df0bdad11b736dc5db2ae82785a405a0b3a8303f4`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:42:51 GMT
ADD file:a0baaba4b04b93c49efe9fdafcb2308d4f775370b8e2a926df265487484d9788 in / 
# Tue, 14 May 2024 00:42:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:21:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:23:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:43f368780ca3724d6cdfa64641264541097ebb1b158cd3e0439fbf1846f179e9`  
		Last Modified: Tue, 14 May 2024 00:47:50 GMT  
		Size: 53.3 MB (53337573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a81dfed6865ecaa40f3f43b4bd4c389449dd3e0fcdc04d95ffd4c8e09fa9cd`  
		Last Modified: Tue, 14 May 2024 01:30:16 GMT  
		Size: 15.6 MB (15642393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0bebc382626195b064b7bc5d045ae9224b0d8f3c00157347449a593b555471`  
		Last Modified: Tue, 14 May 2024 01:30:30 GMT  
		Size: 54.1 MB (54076843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c7ec963ac714a2f94b076f8e287270d7deb6f725c170e54c73463524ff8f0a`  
		Last Modified: Tue, 14 May 2024 01:30:55 GMT  
		Size: 173.0 MB (173025883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f643953c27d28e2bb1a099985df7617e4290a87d4107b66f653499d5b7b60868`  
		Last Modified: Thu, 30 May 2024 01:41:51 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e5c9181e878c28fff18bc4dbaade504e0b89ca6266f8b7812525d866bf2552`  
		Last Modified: Fri, 31 May 2024 00:55:05 GMT  
		Size: 33.7 MB (33673972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf33ae3ee68db0e251d76291903772ab5581170bbbe119bc5d11eb3d7d0ada3f`  
		Last Modified: Fri, 31 May 2024 00:55:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:86fb87fa020ea51211feee1c0cf9141dd09d77e15dc4fa5ae45db9994bbb622f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14910438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e1d47e8ac42a11d3b08ad1b03a86d24f2f27eb28cd60566613e5abe40ad114`

```dockerfile
```

-	Layers:
	-	`sha256:eb26d323e9de5da77b64d3282950ae11987ddc73ca901c9263042d0f6b1db30b`  
		Last Modified: Fri, 31 May 2024 00:55:05 GMT  
		Size: 14.9 MB (14888254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88a4679a5405bca01dc3b55f23d4c0379b280b717c7ea7394a31fe6b260884ee`  
		Last Modified: Fri, 31 May 2024 00:55:04 GMT  
		Size: 22.2 KB (22184 bytes)  
		MIME: application/vnd.in-toto+json
