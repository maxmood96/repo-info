## `ruby:3-bookworm`

```console
$ docker pull ruby@sha256:fb9d97f39ada3ff3ed0f1d04fc94efb59490c6c519f468b54a91e48de9ea0ec5
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

### `ruby:3-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:825b6d0a6fc7d79ea9120c64f540471f1071a8732e9124ac0cd704505dbe7585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.3 MB (385302699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1b2a0030c12a256c1f37fd2477af7fb66c935a25ca74077628fe83e29fc547`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:23:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9fe7fef9befda786bc8e1dd1ae42ffd8b9c37a4cce3c433e65ebb890cb1672`  
		Last Modified: Wed, 31 Jan 2024 23:33:14 GMT  
		Size: 211.1 MB (211111518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b04e2a9f989a8520ad72fcf0224588e4365f0a65416ef76549c43be5fa12afa`  
		Last Modified: Wed, 07 Feb 2024 17:56:05 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7653cacde4362ac822094fe048d6d900c02ab78a8b1ace8f9d5943af30db025`  
		Last Modified: Wed, 07 Feb 2024 17:56:06 GMT  
		Size: 36.4 MB (36414671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e59d5137a9863a6d70ed4b2d092c632b59725012c52d57ae0f8fdf73bcf5bd`  
		Last Modified: Wed, 07 Feb 2024 17:56:05 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:0937f7c428612f8b293cb0564dcbf40f2bec3ede4e4316f6c5f842d1aa90b6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13547124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dfe7c04daa1a19b535d8f30c8e0cef97ffeedd01bc1064c7ad8ae6a02e7705d`

```dockerfile
```

-	Layers:
	-	`sha256:ea7b22cdc8c52e61ff64e2f10be845670cdf887d29b901f10c72588b476c2989`  
		Last Modified: Wed, 07 Feb 2024 17:56:05 GMT  
		Size: 13.5 MB (13523149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c528efca7cced59fc53e8da836c2faabea7e320fb313b3556954fd01ab8a2763`  
		Last Modified: Wed, 07 Feb 2024 17:56:05 GMT  
		Size: 24.0 KB (23975 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:3e4a66aa181d8b2acecb8fb4662de235eda0a355997019b87bae3c800f2d22e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348862802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9f9f803e42d82d86ac59211e25380dcc09947cc7ea4851bd581869ef560ec98`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:05 GMT
ADD file:662d1555034de39f7c527248308e476bb336d5cde0f55c434ebc0b110e1fab18 in / 
# Wed, 31 Jan 2024 22:44:08 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:11:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:d1441b7e67f844fc0744453b48904316fc03e3b9e0cb5e36123e151ba78f6062`  
		Last Modified: Wed, 31 Jan 2024 22:47:34 GMT  
		Size: 47.3 MB (47342752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8244bd760e660bc987264c6deab8438f5e868c5307cfae0ef411e9e0ed34bd`  
		Last Modified: Wed, 31 Jan 2024 23:22:30 GMT  
		Size: 22.7 MB (22728429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df1a167e079cd949ad7b4f684f2432665fe744b2c6a9f302d896dc02b719184`  
		Last Modified: Wed, 31 Jan 2024 23:22:52 GMT  
		Size: 61.5 MB (61517372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbad25eb5c49c8ee60b2f9c576ab52c62fdeeae27d9d0aff4526469c55fa65ac`  
		Last Modified: Wed, 31 Jan 2024 23:23:36 GMT  
		Size: 184.4 MB (184421840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acd992195bc01c0bd4b8bffbf0873f0931b9ed80418aac2286491eb00ad1b99`  
		Last Modified: Thu, 01 Feb 2024 18:18:19 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52b8e83ca56fbf917fd5de139fddaa7f11a8d7860be1d383f551ab78e948562`  
		Last Modified: Wed, 07 Feb 2024 18:23:20 GMT  
		Size: 32.9 MB (32852065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9be7110dc87b65514f883943f1f2c8d31fc7b4c5ee2f915af1713a41195f810`  
		Last Modified: Wed, 07 Feb 2024 18:23:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:6d2f72e83bd588921679a6803b7eff8d5bc48cfc532d0402aacb8eaf9e9a5f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13371788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1552fce5b244de9688abf6eb48491e7cf68b07040928cf6e5e687edd316b92`

```dockerfile
```

-	Layers:
	-	`sha256:e0d4790a5fad49f626b1a2cff21db724be07237257d645954830d254027f19c7`  
		Last Modified: Wed, 07 Feb 2024 18:23:19 GMT  
		Size: 13.3 MB (13348347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:999bf30940b9eae80bcdd3d4e607ceb34cff013a278acbdaf20fcc3c04e16a41`  
		Last Modified: Wed, 07 Feb 2024 18:23:18 GMT  
		Size: 23.4 KB (23441 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:b0acd7df95e1a01a4a72a2cbee4db00749bf5b038e9d1baebf5e7b83c1395167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334150730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4244643f9e8eca24e32338715b8676885248932042d763fc38de37846d4a5715`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:48:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d88bc19189eb4f1105881142f65d20f20c62599e816c26cb5fab6c266f89b80`  
		Last Modified: Thu, 01 Feb 2024 02:59:25 GMT  
		Size: 175.1 MB (175081910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3d116356ba300ecff3cb21b4e5603a4d03cb979b44cb0a73603c68a2760f76`  
		Last Modified: Fri, 02 Feb 2024 10:34:23 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bc5093c37167feb895fa7cb5b4b74ad524d5399b4ceb6ad9b48418952f3a4d`  
		Last Modified: Thu, 08 Feb 2024 01:20:14 GMT  
		Size: 32.7 MB (32720134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ef5d1d3e8c94b10a7418ff4048f9831a4f1a9715ee42efc959f6a1f955a15b`  
		Last Modified: Thu, 08 Feb 2024 01:20:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:6c6c499276722576c166b109e1711297d941cab2c09cdde86492f02c319433ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13377261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f8a2483d79cf99e1ec71c87dc864d5443b2d9431bd42141be4bfa9ec743c78`

```dockerfile
```

-	Layers:
	-	`sha256:6feb8517eef852da25aeb50cb4f90330d3401d925b4a87369848876cc5cfcf5e`  
		Last Modified: Thu, 08 Feb 2024 01:20:13 GMT  
		Size: 13.4 MB (13353821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56262f5315d1c6c754b33a3cec030109715be57133d9e36b3199de9a60a97957`  
		Last Modified: Thu, 08 Feb 2024 01:20:12 GMT  
		Size: 23.4 KB (23440 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:35b802cf7c78b6d5768c67353203595e6643da357385f72d22b3446a0d5642e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.2 MB (376151767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad457130a9ccd3bd1f6e4830ded06ffcd51719e68224f701e13ede83c12835f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e4299bb649220caaf79678771b6f57f97122a0a5b638fff83400a663d282b3`  
		Last Modified: Wed, 31 Jan 2024 23:52:55 GMT  
		Size: 202.5 MB (202505949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dfa9cdc9e63c2d404723b0234a21def0d8ba30fddc9e5d688b59818715cf04`  
		Last Modified: Fri, 02 Feb 2024 18:31:39 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed21283c0da995898d2f72391e1c390841aeba1cf35e5e5fb921ade04570bd9`  
		Last Modified: Wed, 07 Feb 2024 18:28:30 GMT  
		Size: 36.4 MB (36448924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30abfeef8e75f3d0386e972bb0ac9a12307553b8e67957c094619f899ff5d20`  
		Last Modified: Wed, 07 Feb 2024 18:28:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:ae39f45554dbc67b6b930d8ab1d9a0d1a6480ecbbea6607ed0347600626f0514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13571713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:728bc7b0b7d32be551e700edcadba3706f1983ccde2debeb292c33764815196f`

```dockerfile
```

-	Layers:
	-	`sha256:83720f2bb4ffc3c4ff0a20cdbafc2f4794171d818026fcf1e7138252530ef976`  
		Last Modified: Wed, 07 Feb 2024 18:28:29 GMT  
		Size: 13.5 MB (13548382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bac65fcab9467b02149298cd29d8d5c5da4cf8c22fe07e2f471f0c2c079530ed`  
		Last Modified: Wed, 07 Feb 2024 18:28:28 GMT  
		Size: 23.3 KB (23331 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:c94e740154c3901cdd5d2303dba4c3faa1c4c2a6917b82d20715352f16f50217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384172232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9456cfe44bb8716d42be83ad8e6eb48e8ec0f6c08a4112cecea5a138ebd491`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:38:50 GMT
ADD file:185b752162445ab4f6f919d4279c3e0631e6ee605698ec61317458546cb121f3 in / 
# Wed, 31 Jan 2024 22:38:51 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:32:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:34:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:4ea3f2a7e82bec0cc3c3005b69be76f8931170968478e9b540091cde5dbdf791`  
		Last Modified: Wed, 31 Jan 2024 22:43:19 GMT  
		Size: 50.6 MB (50603415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee967c27b9c941dceae087384959ba6b8e9de11c54505fd91905d98eea18baf`  
		Last Modified: Wed, 31 Jan 2024 23:44:47 GMT  
		Size: 24.9 MB (24888772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342d8ebbc02bcb8071e4594b56892d4ec04d2bdcf0ee0283d75d845023c1c9fa`  
		Last Modified: Wed, 31 Jan 2024 23:45:13 GMT  
		Size: 66.0 MB (65989049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff5d662d773fea816c984a59d6fe934f5dcb9f01d11c39e790439b20ef367af`  
		Last Modified: Wed, 31 Jan 2024 23:46:03 GMT  
		Size: 210.0 MB (210044410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360de68eb0b4db61b7f85b5d427a05d41ebd228c9580917a33da1e630b271665`  
		Last Modified: Wed, 07 Feb 2024 17:55:54 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94f192328b9ce88e130d4256aa625cc132a10a34bd721b13ab2190ce060b514`  
		Last Modified: Wed, 07 Feb 2024 17:56:03 GMT  
		Size: 32.6 MB (32646243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5c2b81c89dcfb14f24ba228f1538e8f87bb958e29846995de318076b0b6ba0`  
		Last Modified: Wed, 07 Feb 2024 17:56:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:833ec589e45d20fe7c476341b83bad0052fdbd8200cb2070c6009d2c34fd856d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13527486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177555c0367570a1d16d7129d641ab4173c07d01ea016f5d15978a3e9ab7841e`

```dockerfile
```

-	Layers:
	-	`sha256:368efe4f4c01eede7a7add1961888088bf2b381894a0a302ae285d1c982d3e87`  
		Last Modified: Wed, 07 Feb 2024 17:56:01 GMT  
		Size: 13.5 MB (13503563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb412d854e96a751ec432f3685c60f6697a6bf8eac9ba677324797bc286bc08`  
		Last Modified: Wed, 07 Feb 2024 17:56:01 GMT  
		Size: 23.9 KB (23923 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:daf5a8340ba4feae2df7bd2c1c6f470938a9255303ea025ead51fc72f6acfe11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.5 MB (359541039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db27f0f9b5407c3cfea9f61213f50c1d38575594c21f601a29e01d0b2ce188a0`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:26:24 GMT
ADD file:eee6c048a0eb51959b7cb7d3c4efc6652decf19517bcb25076f8ef9fc376ce48 in / 
# Wed, 31 Jan 2024 22:26:30 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:10:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:15:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:07a56ca79640510bd74a49ee96c70117fcef80d3a54a0b75ab30e3c06c58abff`  
		Last Modified: Wed, 31 Jan 2024 22:37:38 GMT  
		Size: 49.6 MB (49574061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9396b75608be0bb38ec0e5812806b60c77abc5f3118ac99b6d0696cfb6d142d`  
		Last Modified: Thu, 01 Feb 2024 07:45:23 GMT  
		Size: 23.4 MB (23438036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ca92fd224410a9f84732731a0d2db9a52407b7ca33a418dd08d3d679826a0a`  
		Last Modified: Thu, 01 Feb 2024 07:46:21 GMT  
		Size: 63.0 MB (62968385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bceaccbccba92f2c5c0591cc9226b540f9fd129c4928fda2a1eb8aef24755a25`  
		Last Modified: Thu, 01 Feb 2024 07:48:29 GMT  
		Size: 189.7 MB (189695618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1254cfae411e7b8d0e239dea4b40bde85fd0a505e126862750ceacb4b4ab2895`  
		Last Modified: Wed, 07 Feb 2024 18:14:23 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74a6e35094924d16a252d5c90b7c04ddd272a30930aab0088441ddd6d2c3ff`  
		Last Modified: Wed, 07 Feb 2024 18:14:27 GMT  
		Size: 33.9 MB (33864595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71dd605541c161b4a56d75c5d32e825b9a35b4eb81572e8ea32a73c64a2b560b`  
		Last Modified: Wed, 07 Feb 2024 18:14:23 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:e618268da81f51efbd65e7ed75858819588c54d8402faf3a0ae65e79076bea8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 KB (23860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa37e9fcd9139a4cabfb96975a12b169a811de3c9a8bb1d404d174a6ece3255`

```dockerfile
```

-	Layers:
	-	`sha256:6d8782168b61a9ab8557dadea0dcbd4ac6a49d9c6851a51eb31ba6c427aaae28`  
		Last Modified: Wed, 07 Feb 2024 18:14:23 GMT  
		Size: 23.9 KB (23860 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:34d0e6be54079daedc012b45b93bbc77646387f1e2c9a816cc308be4e806591a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 MB (397252487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a38ee62e2cd41a5263addb116b1de8b0936aaf9d69afdd4083120ee6e92ef68`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:30:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd5edc8501c8ac210226c299c64633308c37f4d32ef7d6bcea2583f769270f0`  
		Last Modified: Wed, 31 Jan 2024 23:48:41 GMT  
		Size: 214.1 MB (214143709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8b1ec461782130df7e849886d617f8a4ce8bab2257a397fe588b5492b25c03`  
		Last Modified: Fri, 02 Feb 2024 11:35:34 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8367dd53b05b603d5083e7c3bfa6de54c3454b78352a174faf76e216695d360`  
		Last Modified: Wed, 07 Feb 2024 18:17:38 GMT  
		Size: 34.2 MB (34246407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df757a15415c057aa4d51f284a414c4df273675eb2cd4f5eaa510fb7daf2822b`  
		Last Modified: Wed, 07 Feb 2024 18:17:37 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:ca995f525ff759e2fa21370e415c9bc2435dbbae787a148c85a0bdea8228f9c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13527912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19fc2ba5dfc662140993476cc678eab4d8d6a0a69a1096d4ae52ec684ac141fe`

```dockerfile
```

-	Layers:
	-	`sha256:14cc8654f8c88c5ffcdc591f56010b5e7dad59bc5b94277e4d4502f18e0a6560`  
		Last Modified: Wed, 07 Feb 2024 18:17:37 GMT  
		Size: 13.5 MB (13504533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca03b10eea9cef7e78db83a8cdac37f0e0002c8c69b4c16b03bb2cd8875227f8`  
		Last Modified: Wed, 07 Feb 2024 18:17:37 GMT  
		Size: 23.4 KB (23379 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:91366bcb72eb9a2e193455c5303142006113b25c795f3e02d12f9d854ba4bf32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351761909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1e8d760a402dc9c83c5d9fb502aa1844095f7cd345acbca2dccb2efafeaf9b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 31 Jan 2024 22:56:21 GMT
ADD file:b1c0200d0f8b6070dfcbbadb831cbd04bd8d1b15c3c1f8e6e13c467f6c3f2879 in / 
# Wed, 31 Jan 2024 22:56:23 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:21:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:24:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:0241650ae38ec8570f9718818b3b516c90697c5cd5686d5dd89306ae5f8e4657`  
		Last Modified: Wed, 31 Jan 2024 23:28:45 GMT  
		Size: 47.9 MB (47940767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1461a92bfa612443d019b6fc535db5abfd3639e66c1c5f41a511bdb1a782f00`  
		Last Modified: Thu, 01 Feb 2024 08:18:52 GMT  
		Size: 24.0 MB (24046914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bc22d156c3113277b2a400b2b60e0ea00f6f62f339de493144008d5cc58796`  
		Last Modified: Thu, 01 Feb 2024 08:19:08 GMT  
		Size: 63.1 MB (63130267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e9ee69e7f405307aed24012667e5bb90820e6d392951de2b5b22485ac9567c`  
		Last Modified: Thu, 01 Feb 2024 08:19:38 GMT  
		Size: 183.1 MB (183147992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524037dcd5bf8c6c5abd25a475163b2f75b640910f414d3822f9806706c04f98`  
		Last Modified: Wed, 07 Feb 2024 13:23:09 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9260ad01dc45cf7d87ec18c5b77dff627220c754b0ad92b87c034ac13bb1fbf4`  
		Last Modified: Thu, 08 Feb 2024 20:27:08 GMT  
		Size: 33.5 MB (33495627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b608e5f7834d2b96729e299746b0cf8218ae360724dfaec359818f86a692fc27`  
		Last Modified: Thu, 08 Feb 2024 20:27:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:7714d1cd96b89f3a2aee620046159f46882f9de1ac74e3bb261a4c1f4a6bab05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13382562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc94e1e27c97e45e8b41a858ceae66a2c6dbac1567624a157cc6a4c7fe0b9bcf`

```dockerfile
```

-	Layers:
	-	`sha256:ebade19e4598ba2e1479823bad8626ab95f07a7668e1492570b3529a875ce58b`  
		Last Modified: Thu, 08 Feb 2024 20:27:07 GMT  
		Size: 13.4 MB (13359249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7e7a6224f509791e72a7fbf3f2203f5d81e7c2facce9c3f161eab92aba7e1a`  
		Last Modified: Thu, 08 Feb 2024 20:27:07 GMT  
		Size: 23.3 KB (23313 bytes)  
		MIME: application/vnd.in-toto+json
