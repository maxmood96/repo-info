## `ruby:3-bullseye`

```console
$ docker pull ruby@sha256:9ee3aeb9c1785798fbc177afcc0233e11faf51c3629f43dda95d4e5114d136b7
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
$ docker pull ruby@sha256:41c8450df34b229bfc5cf6f0b330b282ef2a23244384391cd3d51f8488b72f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358753324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5682522a5033eabb11e151f71b050b4a6a5e7751396541ab20a832067e851a02`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_VERSION=3.3.0
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:54:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff24b88ad3798f817849ad391d809ece121dc9b7f82f24bb68eed84561f048`  
		Last Modified: Wed, 10 Apr 2024 05:36:15 GMT  
		Size: 54.6 MB (54588743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f58f24df78e3aabf785017c3197c2a09fd606e7f19a830a1cfde41f681f39e`  
		Last Modified: Wed, 10 Apr 2024 05:36:46 GMT  
		Size: 197.0 MB (196985611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1be564d41ed2ab1dcd1ed2dc142d58b3ad9b2b0f89063038b241112bb5a47c4`  
		Last Modified: Wed, 10 Apr 2024 06:57:04 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6bbc5437fcbbb4d26c8deeac416c4a1d83acc1b788f963a759cb93b9966322`  
		Last Modified: Wed, 10 Apr 2024 06:57:05 GMT  
		Size: 36.3 MB (36324846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf161a0524b5fe91d8d792a0652634c16601fa565ac33dc7d10584f6e9302ae`  
		Last Modified: Wed, 10 Apr 2024 06:57:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:b131c904c6a1a558f9012178d1d47029f687fa27ead295f426d716d06b90b55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15090056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1f974b4c8b9a63c50a6ca24473ddbceb358f3800c49e002174e388676fbff1`

```dockerfile
```

-	Layers:
	-	`sha256:77e9ffdf8b097c62e6d4420d2e827cf94108c9bbc4b7972da211b50d108d1c53`  
		Last Modified: Wed, 10 Apr 2024 06:57:05 GMT  
		Size: 15.1 MB (15065953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eed506e984dbdd2627b827ea51ee5cbbb8c5dd00893e8a05418684f41da1fcf3`  
		Last Modified: Wed, 10 Apr 2024 06:57:04 GMT  
		Size: 24.1 KB (24103 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:97881de28762d15860d5587baffb19e14d2acd0cddb5e4a9ab29d62c7de7225f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.9 MB (327882699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7071338703466e988b586b95a13e0f6603509293869d9ab8644ac8ad85331ed`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 10 Apr 2024 00:49:22 GMT
ADD file:1eb31b3bcff4decb2d77374005bc7e0451f76188c3586232986a3f72e069dd04 in / 
# Wed, 10 Apr 2024 00:49:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:44:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:46:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:73e28a24bff6aad570d221d844a24c5be13f1afcd4819e3c4842ae6b4ae928ed`  
		Last Modified: Wed, 10 Apr 2024 00:54:59 GMT  
		Size: 52.6 MB (52591634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4248f04ac8d108861dbe994d7550102128ab72a36f2e74ab8c4831cd3f62d60e`  
		Last Modified: Wed, 10 Apr 2024 04:56:29 GMT  
		Size: 15.4 MB (15374797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1659bd5d3219d4aa530cdde5907a7ec6f956403ff1fdc412cca4f0d6b591c179`  
		Last Modified: Wed, 10 Apr 2024 04:56:46 GMT  
		Size: 52.3 MB (52328994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78adabbe39c0815a36cf1d8811e270a15ac0d9983160eef6eddab0bfca7efabd`  
		Last Modified: Wed, 10 Apr 2024 04:57:22 GMT  
		Size: 175.2 MB (175154967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fef622c56ceb932b63dfa5a048c802b585e2963934efa6b2f12c9ff8bd53ae`  
		Last Modified: Thu, 11 Apr 2024 11:55:59 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6466f83d039261957229f3bb3df8c3c006f4fcef87bfa0f06bc435a053aecd0`  
		Last Modified: Tue, 23 Apr 2024 17:06:25 GMT  
		Size: 32.4 MB (32431965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a134a71b518e3614335d11466881c02ebf202b6646df8619c7ff3c23a2107a01`  
		Last Modified: Tue, 23 Apr 2024 17:06:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:db3eb1846b52afb26cb08b9f33304eb787eb86fbec1fc88d6eeb0460d83b0471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14885328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda7b19d442a090c5c3e8becdd31c501998008f5d26a81e3b62b0459c613fe6f`

```dockerfile
```

-	Layers:
	-	`sha256:d9d8366692c79b1914b165c51f0f644886965f2ec5e50cd5e8cc7bcfa733e2d1`  
		Last Modified: Tue, 23 Apr 2024 17:06:25 GMT  
		Size: 14.9 MB (14863048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2b60d91d46d9b13ea57b7a56523f8309cb85f8aafc5980e76147e4b0f579cc6`  
		Last Modified: Tue, 23 Apr 2024 17:06:24 GMT  
		Size: 22.3 KB (22280 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:ba88fbc396d74c7999564d17e8c9fafa2005b68d220822425cc1013dbc7fef6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315231190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d690fd00db4e7855b24d3621b15c5dce848738c7cbf8dfa890609ca0ef97ca`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:eb53aade3ed19f72413045948cad3084902fe630cc20789d2c2b5bc334679575 in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_VERSION=3.3.0
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:54:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:23ca580217f1a6b17dba868e7ec34ae7fff221e07640fca532510daca8ed46f6`  
		Last Modified: Wed, 10 Apr 2024 01:04:48 GMT  
		Size: 50.2 MB (50246481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89b030e474718221560707f98fb967bd582bc0f355ca5caf120fc5f25b2d58`  
		Last Modified: Wed, 10 Apr 2024 07:01:21 GMT  
		Size: 14.9 MB (14879245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef8c5cdb2957e3cc1b26c037acafd549c7286845f8007127da85b383702cee3`  
		Last Modified: Wed, 10 Apr 2024 07:01:40 GMT  
		Size: 50.4 MB (50357907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c48f55e50a2918f423e3f80c787998eca4a47eec492d7e81553c5a738f095b`  
		Last Modified: Wed, 10 Apr 2024 07:02:17 GMT  
		Size: 167.4 MB (167441750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1739d19392678311ddfde15479d625ac11e2d69d2d9bec120567e86425c7263d`  
		Last Modified: Fri, 12 Apr 2024 09:49:08 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9107f5f0db02f266a44b059196ca4f57f64663ee81f9f9754338434b12e81680`  
		Last Modified: Fri, 12 Apr 2024 09:49:10 GMT  
		Size: 32.3 MB (32305464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d1f3baef9cafece2ddeec235e6e6042496e9dbf8664c700ebf4c75cdc81a4f`  
		Last Modified: Fri, 12 Apr 2024 09:49:09 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:55607c219a7357f163fe024c5c6d3ca9a2d19b4bd29119bdaee76a29ba6b7f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff53750a492f3a831e5f903192778fc133c5ae9f3295c7e772b03baefe856f9b`

```dockerfile
```

-	Layers:
	-	`sha256:05763467c093527d37953269751016709add4cf071a3a106fb4322f16e381482`  
		Last Modified: Fri, 12 Apr 2024 09:49:09 GMT  
		Size: 14.9 MB (14867842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b63f023856f85a90479c9b3b21adcbde55a08560c5c6a8f30905c9a20cf467`  
		Last Modified: Fri, 12 Apr 2024 09:49:09 GMT  
		Size: 23.5 KB (23536 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:aabb0d1fc64295f276c41ffa5eab414c179454b91be2fe4caab16b14c177b4f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350320610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:301acec30ceda35ac5603e97424b9a55d6f1893a4faf2e93a79cd25ad73d3486`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_VERSION=3.3.0
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:54:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3f4a530684a6d51e431d14164bdf20c7ad515e8948ddbfbf5f9c2c3680727`  
		Last Modified: Wed, 10 Apr 2024 04:33:00 GMT  
		Size: 15.7 MB (15749239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27317b8832e116e0457de89bfb9097cbcd3165d6079c38230f3728894dfb3af1`  
		Last Modified: Wed, 10 Apr 2024 04:33:14 GMT  
		Size: 54.7 MB (54694342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dceb3c5772a800dd46b1b628a79e2167bd6bb0e9844a04e9ffc8a550a182b`  
		Last Modified: Wed, 10 Apr 2024 04:33:40 GMT  
		Size: 189.9 MB (189914112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f01f468387a79a47ff5d789791c047780796a482b8f248d9f0522bd101d09ab`  
		Last Modified: Thu, 11 Apr 2024 08:36:57 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac1cd6134e8a843d7c04971e2cec74fee50160b46587f99b6dda991e5d38e51`  
		Last Modified: Thu, 11 Apr 2024 08:36:59 GMT  
		Size: 36.2 MB (36233397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bdb35795cb5fcb276f28d3e119a0c0e0432ea1d0ee71bf144e03cbffde044cd`  
		Last Modified: Thu, 11 Apr 2024 08:36:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:0309d6172114b63149788d9285faecd49375411ff5cffcac790b73a11eef2eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15091869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99267ae34a2e5dfd42c628f60ee5858b0f23449619e3e166b0bdd2cc8592ce61`

```dockerfile
```

-	Layers:
	-	`sha256:1bef6238919f929796bb09fa6f6cc9e56065e7033d0303cf18d6abeb3a7126e8`  
		Last Modified: Thu, 11 Apr 2024 08:36:58 GMT  
		Size: 15.1 MB (15068419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c9a6afbf0686ffd8296e5d0337b6712515fcd0c42fa57b97559b525d3faecec`  
		Last Modified: Thu, 11 Apr 2024 08:36:57 GMT  
		Size: 23.4 KB (23450 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:da964b17cf84791019fd2fc707fdeb78c7db3d96dc4f86b739c1cbc21813f232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 MB (360529909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab72300ddd174bdf57c5efb3ae3f2cbe2ddc6a206ff85954450eeefce38b665c`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_VERSION=3.3.0
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:54:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125c557bd27681f5387605727a1b0d44605793da722ea6f8f66b86df9aa54384`  
		Last Modified: Wed, 10 Apr 2024 08:07:12 GMT  
		Size: 16.3 MB (16267921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13acd7d81d47808020936c58e9842c82c55c0205f369482de2b263fe21ed2dc6`  
		Last Modified: Wed, 10 Apr 2024 08:07:31 GMT  
		Size: 55.9 MB (55927749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed69373b65ed4263cd1d2ead3d6570264c8de6a744aa10974a8266c660515080`  
		Last Modified: Wed, 10 Apr 2024 08:08:16 GMT  
		Size: 199.9 MB (199890546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a54b2fadc304f37f635f2b0db88d1547a603be8fb7d6143615b280acc566c6`  
		Last Modified: Wed, 10 Apr 2024 08:58:09 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9052878daed06d87184714511c1ad86e383ffead958c7beb9d137c127184f8`  
		Last Modified: Wed, 10 Apr 2024 08:58:11 GMT  
		Size: 32.4 MB (32377162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f4f93fa0fa01f4e90bdc26f2dff4908ff0593a532d8f01bc6cd10ec2bd45aa`  
		Last Modified: Wed, 10 Apr 2024 08:58:09 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:d2eec1878f5ca68870f6facaf768f736a76bb6ed00f6b1a2285d24ffb09d2ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15078853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed1f942a91e0b0e13360be3629136d83c2816a1a4045e7dc9ec99333b737979`

```dockerfile
```

-	Layers:
	-	`sha256:2495cd6b1217fe3af14ac8d7f17530680c0e383fb3995126ee26376aec42b86a`  
		Last Modified: Wed, 10 Apr 2024 08:58:10 GMT  
		Size: 15.1 MB (15054784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c4d085a4f1888e520f5322869b0fcf7ca3012b78cd644b9ff1834d65cb36a0`  
		Last Modified: Wed, 10 Apr 2024 08:58:09 GMT  
		Size: 24.1 KB (24069 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:cf9207b1b4f3ba3ffb9f169b8ed50b10bdbf6e4fb0b8bd3def18f33f0790c1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335159346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c03948c338bafdce2a03c05077c966ddbb7c7a099d101c474d4039ab5c0c9ce`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:b9ae0499407c5db6a4d213452b2b485d2f0c9fae0792c77a629177988969faa3 in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_VERSION=3.3.0
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:54:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:eade21836c93150a05690be18ba07f9d56297d4f2b59f348647ec05e7c1435cc`  
		Last Modified: Wed, 10 Apr 2024 01:22:42 GMT  
		Size: 53.3 MB (53309804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bca85f765a047c080d3e09be0e52f8fa2f73c3a685e3fe6eb266733dcea65e`  
		Last Modified: Wed, 10 Apr 2024 15:49:45 GMT  
		Size: 15.7 MB (15734419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ae3ab149a39251a612af123a349e1dc5fed6c4e6c2fd0dcdd471587d9f3d1d`  
		Last Modified: Wed, 10 Apr 2024 15:50:30 GMT  
		Size: 53.3 MB (53311077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4245946189955b46a9c5b538da5eed5252d87a1fd7f2f33fd5fb3289f5d6cb44`  
		Last Modified: Wed, 10 Apr 2024 15:52:29 GMT  
		Size: 179.1 MB (179097898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dfd47d5e7c5df2608f3acfeb414f8037fede20bfe089b3d43ddfe5aec0099a`  
		Last Modified: Fri, 12 Apr 2024 17:16:23 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab585f1cfe9fc34b39c8d444c62e5324d0a7b3f2c61b3a0606fd08133ecef33`  
		Last Modified: Fri, 12 Apr 2024 17:16:27 GMT  
		Size: 33.7 MB (33705807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1c4fc96e0da014a693270ad002246d37c96d77621d3c033ec20b419653bc3c`  
		Last Modified: Fri, 12 Apr 2024 17:16:23 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:df0c65362bdd22168004c48ba4d5eed1a3588869383110df7087ed408da4544a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 KB (23288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92cc9b3bfd4607e0cb5c11d0f2f1137d62a161fe9573affe6b897328fef1946`

```dockerfile
```

-	Layers:
	-	`sha256:72e365b5c93c7c267ca32b1fa782cc3b29262214a99bb744406ef0982cbc7b3a`  
		Last Modified: Fri, 12 Apr 2024 17:16:23 GMT  
		Size: 23.3 KB (23288 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:900730bc788d11e42c014a234c6f96c4fc1039fc16836448d956e881e2a4430a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.0 MB (365004080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc12c458d646fe1ed185beddc2f760575ef9cb3205bc1275eadf59cfe8f392e2`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:774dc7f7db45435bfddcc1ff7bb4ae0716252e8f7c3d074ff7611070207b8314 in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_VERSION=3.3.0
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:54:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:eed533dbdbda3df66dcde8a75fb0ab317466f575d116ffa4e053da66ab0dd942`  
		Last Modified: Wed, 10 Apr 2024 01:31:35 GMT  
		Size: 59.0 MB (58959030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e798a4c3c738ae3b2b3ae6f2b6f02c6db9d510fadd63004b60dd8268c907ee34`  
		Last Modified: Wed, 10 Apr 2024 07:17:41 GMT  
		Size: 16.8 MB (16765741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a0da44da0fa59c2e0283157a263f65dcc5e2b22c7a5515c68bd6d82e305a55`  
		Last Modified: Wed, 10 Apr 2024 07:18:00 GMT  
		Size: 58.9 MB (58873011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711cc15f136ce528a3936b4864554b8879c5d361f9d968ba9b756dd216f192eb`  
		Last Modified: Wed, 10 Apr 2024 07:18:39 GMT  
		Size: 196.3 MB (196345047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c1985596de9417ab3835bd7b3373f8774783130d4e81732a74e17a13b74a56`  
		Last Modified: Thu, 11 Apr 2024 07:33:26 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1666c0bc6c8bd0ede1e0380b751936d21bea88576b31ac1bd4a82715d8d463`  
		Last Modified: Thu, 11 Apr 2024 07:33:28 GMT  
		Size: 34.1 MB (34060909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3667abcbbbe5d110b40bd0aa53acb65b8ed4038cdd3c148efe0ba37980707c8d`  
		Last Modified: Thu, 11 Apr 2024 07:33:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:50bf366d5487c3be5719999004beee5de24d5cdb55a52701d73d72542b5862d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15058739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c46dc30b16e0cff5f19b95893f573d780279b8c887ee786e14b5dc17eb451f4`

```dockerfile
```

-	Layers:
	-	`sha256:8582cdb3649c9ac4c50187601a32e52d51ace762a8cf82ec750182d247f9df41`  
		Last Modified: Thu, 11 Apr 2024 07:33:27 GMT  
		Size: 15.0 MB (15035258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c3a51151195e2ab2a4ebcda458b2d79ea8dd68f1c144aba82efb23e4c9f82e6`  
		Last Modified: Thu, 11 Apr 2024 07:33:26 GMT  
		Size: 23.5 KB (23481 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:893b79e0796d686063a2b3e9a818a401bc6547b1c0cdac2242d9a8505c5d3463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.7 MB (329689174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a0f787ab4afcb087476a4b8ef9285c3286033d03410abc991ccf63c31c8991e`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:ca4cd0bb2344426b8777da3ac3278e42efb1e15064ff144111d7ecacdf3cbd4a in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_VERSION=3.3.0
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.0.tar.xz
# Fri, 05 Apr 2024 21:54:06 GMT
ENV RUBY_DOWNLOAD_SHA256=676b65a36e637e90f982b57b059189b3276b9045034dcd186a7e9078847b975b
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 05 Apr 2024 21:54:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:54:06 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:8d59905935c60c8e62d2bce55ff58a911d9ceda48b95f8209712af92b63b5ceb`  
		Last Modified: Wed, 10 Apr 2024 01:48:44 GMT  
		Size: 53.3 MB (53324935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389d06a9a1a36eb81d725be8859911dbff14d557f54a14795436ae38ccd42a97`  
		Last Modified: Wed, 10 Apr 2024 07:31:55 GMT  
		Size: 15.6 MB (15641598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ed65098ad9320ac0b40e4be7ea7a1b7169e2786089554bc580dd22bd53591c`  
		Last Modified: Wed, 10 Apr 2024 07:32:09 GMT  
		Size: 54.1 MB (54075652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad291048530ded42ea1541cf11a0c743fbc2f8d434ea0ada83f8c96dce458a0`  
		Last Modified: Wed, 10 Apr 2024 07:32:37 GMT  
		Size: 173.0 MB (172991518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0a4ef942ca2b9c4253f1416ffee2caa6c2beb750396e3be5d07114f6a35fe`  
		Last Modified: Sat, 13 Apr 2024 15:25:10 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e0d46f0b79955acfc643fc21505c9da447fb3fc74aa8caf061be0147490e16`  
		Last Modified: Sat, 13 Apr 2024 15:25:13 GMT  
		Size: 33.7 MB (33655129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cccffafeecd9b27f97d54a02728f7c6a58ef7891c480964dda9f704032121d7`  
		Last Modified: Sat, 13 Apr 2024 15:25:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:58e8aa02026c2d38f774d153a53d61b72a31bcd8588bcdb67ab948473428fc2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec802b2d83862fe66dcfc5a79a041e9db3255834e0d763c6c0f0e821bb572c70`

```dockerfile
```

-	Layers:
	-	`sha256:39daf4103eaa55a27e734627eda5b0f38833c213a7039d608dc8d9317debccfe`  
		Last Modified: Sat, 13 Apr 2024 15:25:11 GMT  
		Size: 14.9 MB (14887629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d10096a891ddec072a1c61de7cb43bfc26cadf8fc36ccb0b1896f4a98b9b5d1`  
		Last Modified: Sat, 13 Apr 2024 15:25:10 GMT  
		Size: 23.4 KB (23440 bytes)  
		MIME: application/vnd.in-toto+json
