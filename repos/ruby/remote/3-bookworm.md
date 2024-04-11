## `ruby:3-bookworm`

```console
$ docker pull ruby@sha256:04ec83a13e34e076f08157db39e50028325b497b83fd71f6d68c64044020c720
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
$ docker pull ruby@sha256:cc5f6b6c5680f77586722b6a710a64bcebcfa13ad986607f5c21e6a3c92ee7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.3 MB (385300727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f02b6e81a7abc0e15655d7319abc21a756177a04abe52180dcca4cd08027e0`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca46406051373533f45af98d83ac1cf33aa49596b44e3270e9bc8e2eaa8429a5`  
		Last Modified: Wed, 10 Apr 2024 06:57:26 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a18246bb4489dfbf21558cdc893f6d506fc749084ccedde3ff3d9c8e078547`  
		Last Modified: Wed, 10 Apr 2024 06:57:27 GMT  
		Size: 36.4 MB (36414918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85ec4be3704a0b51bf4e60ae87ee7849bcab57a80a141793b06cf57e5ae179b`  
		Last Modified: Wed, 10 Apr 2024 06:57:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:cb1e83eb8a7ee0465ad327029cc6bff903f07533944127e63e1d153377853178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15486953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d472178828be6e7eb37993f2021556c9b2b7e5f77f589c30c422cd9b2f982c`

```dockerfile
```

-	Layers:
	-	`sha256:a7c29d8da8c51c5a40f10357a13f8740048e61578ab5d876b01a7ef176e71646`  
		Last Modified: Wed, 10 Apr 2024 06:57:26 GMT  
		Size: 15.5 MB (15461693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd2cb5778cdb4e78157d1f34f04cceba9b0a97156758aa91cc6d6fee708f5074`  
		Last Modified: Wed, 10 Apr 2024 06:57:26 GMT  
		Size: 25.3 KB (25260 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:c408d6079c8cfe5acb259d12bf3ae6465b4b4d602772f493aa2afcf0384ad312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348862829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0dc9e8b337d8ccc46f4c18c45daba140a47d365b69f6f2c626662e9e676963`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:23 GMT
ADD file:f3cc3d5f7d1cae45631ac2eb84f09f3bfab8fc50029f767a3b5004daf11e8493 in / 
# Tue, 12 Mar 2024 00:48:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:34:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:34:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:35:42 GMT
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
	-	`sha256:5dd742eb8f72c3097f9e2af2aef94f74f93738d2c08b702932dd4bcd67ceefc3`  
		Last Modified: Tue, 12 Mar 2024 00:51:12 GMT  
		Size: 47.3 MB (47312155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d0987e351155bef4267ec491fd56aaec30a57261d0559ddd961d67e1f91099`  
		Last Modified: Tue, 12 Mar 2024 01:43:12 GMT  
		Size: 22.7 MB (22724858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0f840c0f2e159cf80c44b742daea5c751f891490775e6c081415196e13e111`  
		Last Modified: Tue, 12 Mar 2024 01:43:35 GMT  
		Size: 61.5 MB (61515858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9069b8edc3144ea7c7fba8c956dedcc448fc0ba006a12c9cfe4ac23f05569d`  
		Last Modified: Tue, 12 Mar 2024 01:44:12 GMT  
		Size: 184.5 MB (184456518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6471e2934daf7c642959fdb1e86406b9510ab8bb317e2c6752ba7922ff4d1fa9`  
		Last Modified: Tue, 12 Mar 2024 21:20:40 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8244edf2dbfa78ee7f4780f83d506395a496944fb532ef70e1c6a67d3d0ae464`  
		Last Modified: Tue, 09 Apr 2024 05:20:40 GMT  
		Size: 32.9 MB (32853097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7da1082813786dd147ce10afeee7dcfb61be90e5551c2ebcf00ece22e2bc5b`  
		Last Modified: Tue, 09 Apr 2024 05:20:38 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:c721a9332c9cf5d8803c85c5e00b009c83ffb154aa9ef4ceb699d5174dc7ac05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15296753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17076c8f11eb6aa377d495b4c21041ec8a4fd411ffe9df58553dfa44e4dc2451`

```dockerfile
```

-	Layers:
	-	`sha256:943bdd8056083364e0a4347b39267f968314eed39c983657b63a4550dd1fffea`  
		Last Modified: Tue, 09 Apr 2024 05:20:39 GMT  
		Size: 15.3 MB (15272028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aae4cea70cb5c474982aafebb5085e2fe3e366ec508e52ba281e8bde5fc1f857`  
		Last Modified: Tue, 09 Apr 2024 05:20:38 GMT  
		Size: 24.7 KB (24725 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:a5c620d596ee03aaa5b8ef0d22f92db1e101105230b96ed0f4870675dcc012bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334144543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed9729976eadcad78bc0f91f84f0c0c67d8947e79b1905ab684839bc23f5151`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
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
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92f2356f131cf05fec17b9513a070521a0a0d1aa5d0f8fca63c3c35f738f9c1`  
		Last Modified: Tue, 09 Apr 2024 07:18:50 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76980e89ff1d15ac39da79d3396aa51deb5239d4987adc939d70b8a123450dff`  
		Last Modified: Tue, 09 Apr 2024 07:18:51 GMT  
		Size: 32.7 MB (32720935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a9813003d3b7c97ec67754f39d6e337435d097508fa4228ce65f7d74109bb1`  
		Last Modified: Tue, 09 Apr 2024 07:18:50 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:1b31137ec9213da71bcea34689bc220ca436adfeb8ff86d89609fd250e3b8e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15302227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e736ee9d34a1cc1af259aaf7da50454a6fc22c5c11c24e7818ce8fc2e7ad83d`

```dockerfile
```

-	Layers:
	-	`sha256:172f5f4f8b45f4a8603a2c3b3b4c2182fcab02edba3cbf5317bffdfceae696da`  
		Last Modified: Tue, 09 Apr 2024 07:18:50 GMT  
		Size: 15.3 MB (15277502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e1191503e88d8584a9c50a567a6a04829e2c8479c4562fb3f19f1de20238c09`  
		Last Modified: Tue, 09 Apr 2024 07:18:49 GMT  
		Size: 24.7 KB (24725 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:0c228a72f61b493dbc34edf9d4f00f77141493e0887797fecb66072258d8da03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.2 MB (376159361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5093dce4d7b8fc1be04ec9f2f5024990bd2afb957dcf95cfa8f20245f068466`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f0de28899caf9216dbe744a75155cbf83ed5a239a63d5882bfd3c5223ce5ab`  
		Last Modified: Thu, 11 Apr 2024 08:34:18 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6354cf9865b45f9a40b313c2e6bf6f2bcee3115aa0c06dc9404d0bad45b3086a`  
		Last Modified: Thu, 11 Apr 2024 08:34:20 GMT  
		Size: 36.5 MB (36450514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42189e8cb313263bb8251eed221059e62767bee08f3ec248e5f9bf35952e99c5`  
		Last Modified: Thu, 11 Apr 2024 08:34:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:89e47e6ac44e260d4c6d1c9b25021f99f9d3e908f8b7f28091be31a595414d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185348291603fa67e7d4c0ed2116dbbc2c92193a178f4638fc5bfb9f5b2f501`

```dockerfile
```

-	Layers:
	-	`sha256:aa9198a2a7507b36d9352b649e17cc8c2930928e6e1afbd5801373c910a1ce8f`  
		Last Modified: Thu, 11 Apr 2024 08:34:19 GMT  
		Size: 15.5 MB (15490212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d63d3e3013b6295c486a1b044582fd471895beb5e433e2062757df78dc6a67`  
		Last Modified: Thu, 11 Apr 2024 08:34:18 GMT  
		Size: 24.6 KB (24615 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:12a4192741886298c35fecf3957881e55b76617c44fea03e2bb0f304e6785459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384164433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cb12560a99549c1d05001097dee3b297604ee817b482d95283514a1a22276de`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc6831dfb1863b1be28704bc73182984488c3a9ae28136094c4b8277fcce801`  
		Last Modified: Wed, 10 Apr 2024 08:58:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226cc8847316a46fe5cd74717bbe3e15c913439301bdd19fec22e5f12af0f1f4`  
		Last Modified: Wed, 10 Apr 2024 08:58:43 GMT  
		Size: 32.6 MB (32646272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de89b2b284f25d44c65f7f3c7f3497d408a947db783c839e1d22101ccfcc4ce8`  
		Last Modified: Wed, 10 Apr 2024 08:58:41 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:e2c37eb67f2a1be8e1db3df2371742715d9e597d7619440ba1136b4c51740d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15465947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7d2e4f51c30f58df7ffb0415e853f7cacd4c0d68df444b6b7f79c39f04f39e`

```dockerfile
```

-	Layers:
	-	`sha256:9242403dd4d737c8c945e768800ce73f9ab3764922bfcc6eb71d060709f3154b`  
		Last Modified: Wed, 10 Apr 2024 08:58:42 GMT  
		Size: 15.4 MB (15440740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2198226b45541c8f59087ce68bed9ceb853c97694ffbb3145ded6e12b577b056`  
		Last Modified: Wed, 10 Apr 2024 08:58:41 GMT  
		Size: 25.2 KB (25207 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:29d17b49f00c5bad949947351a5b2adb9cdee18298e34a3ce0d331bd30492e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359724580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc743ab8dbc598667f54730cf449f8900f7662483a4fbe46e6add0fc863114bc`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:49 GMT
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
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02977c85a258d317066e5a1e6febc79a4caa2a830ee66f596c866db50d3361d7`  
		Last Modified: Tue, 12 Mar 2024 02:44:46 GMT  
		Size: 189.7 MB (189698984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec19e2f8592bb85f9350f214ece6a2fcd541ad20a30aaec9095aa258647a83c2`  
		Last Modified: Tue, 09 Apr 2024 16:09:18 GMT  
		Size: 201.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd79f6d222a8718d72d2023a091315c25494e2aed5d9b03d4586d6348ba13fe4`  
		Last Modified: Tue, 09 Apr 2024 16:09:22 GMT  
		Size: 33.9 MB (33865600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d3c9f63422bcd6c29dbdc6c7354ecc1655951922c05b1a8c14006dbc012041`  
		Last Modified: Tue, 09 Apr 2024 16:09:18 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:295f44627114b2ffe932aba047b41969ce402df139e3de49b6a2e2d26841b83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 KB (25145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4cc33f2e1f096108425ffca9b557732e9403b9ae088ed5f2ba799d7e41abc5`

```dockerfile
```

-	Layers:
	-	`sha256:4f26394ef1dd5ee3492c2b7108a65c63e640d6dd03c9027aaffa28023940261c`  
		Last Modified: Tue, 09 Apr 2024 16:09:18 GMT  
		Size: 25.1 KB (25145 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:e2c6aacfd70a5464abd97ecbdb86009d40cf1e1491f63559a2d044c5e3f53a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 MB (397260028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a5b696bc27c347b1550693d083d144bf491cc7446c03a3ca22aa7c1a790a51b`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:12519205a7ecc1a9b92b9b26c967bf9f7204f2e0b9c81cb9a147b10a29b0715c in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e6dcf23c0df5604eb9aa3050ab9c36d44dec4ab1448d2c229f4beaaf0f7fa503`  
		Last Modified: Wed, 10 Apr 2024 01:30:37 GMT  
		Size: 53.6 MB (53562477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9a49dc2918c681cd1306002e0306d198b0ab9f74366235b251cb85c930eaaa`  
		Last Modified: Wed, 10 Apr 2024 07:16:20 GMT  
		Size: 25.7 MB (25696598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7558a95a0d29869e7f316194c1d23abcbbe4d8c3340f4d3103f670b9d4af3eef`  
		Last Modified: Wed, 10 Apr 2024 07:16:43 GMT  
		Size: 69.6 MB (69581154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab0dede385435598179e3ab86d7c4094cf59880d986b82c837b42b0649d5afa`  
		Last Modified: Wed, 10 Apr 2024 07:17:27 GMT  
		Size: 214.2 MB (214172353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0abc0131b7e2c012ddc1714725038c710690a1c21b4f302561454dba740314`  
		Last Modified: Thu, 11 Apr 2024 07:28:34 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a422455d000d7cd257257a080f801a8be956506cf5d07d7b9095e2a76f6efe05`  
		Last Modified: Thu, 11 Apr 2024 07:28:36 GMT  
		Size: 34.2 MB (34247105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3de366e25f4f3f613827f05a8e20d07cb3882d9dcf336befda4ebaea9e5c955`  
		Last Modified: Thu, 11 Apr 2024 07:28:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:8566430fb5d9502f6537f57e6ebcb6751c33ea383bd467cdfc57acac52de6dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15463055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a517da488ecfdadcbbcff0f87dba4f4dc8de16595d5f25d01a5860ebc62fdaff`

```dockerfile
```

-	Layers:
	-	`sha256:eca25b4bf72c719d3cb8a3c35cb9117454bfa9c864b262b53370d0cdb70b087d`  
		Last Modified: Thu, 11 Apr 2024 07:28:35 GMT  
		Size: 15.4 MB (15438391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53cfeff4ee0c49c6b3b6a93d4572950a59d0c900cc43325470fa2c0ed8d955c3`  
		Last Modified: Thu, 11 Apr 2024 07:28:34 GMT  
		Size: 24.7 KB (24664 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:a5f937881ab58258ad034f9b3060cbc8205c8b232aea24d76df52ec617c6b784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351747485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d64fd6486b1e8f414d5c82f437aa44b6c374484338b0d924ce68e92968c926`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 12 Mar 2024 00:51:23 GMT
ADD file:78d8ac80b1cc0c1fee1055005d9481e7bfa64e2586e84feeda25de7413892506 in / 
# Tue, 12 Mar 2024 00:51:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:12:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:45 GMT
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
	-	`sha256:46730624c51b83b2a39f8e8dd2b4f779e9de6d2947a869347d866c219bf64034`  
		Last Modified: Tue, 12 Mar 2024 01:20:56 GMT  
		Size: 47.9 MB (47916698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddd8fd5b149ee7af1c46d50fe003e26464d37986964f535f7974aa281f5e5db`  
		Last Modified: Tue, 12 Mar 2024 02:47:27 GMT  
		Size: 24.0 MB (24043467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e216ccb0e83eab691c529b6b3db381ade89246b00d45b49aa74a6de8d55709`  
		Last Modified: Tue, 12 Mar 2024 02:47:43 GMT  
		Size: 63.1 MB (63126659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6654b38164df76c1496278c128a09a6fc9ea1d703322ccb6eb98f578047b2b07`  
		Last Modified: Tue, 12 Mar 2024 02:48:12 GMT  
		Size: 183.2 MB (183164991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a6e7d749c40484f15fbb938a526f95d7b03e1c201d274915c95d2aab5649c5`  
		Last Modified: Tue, 09 Apr 2024 16:12:59 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7986fcf9ec0577a111fa4893acd05794d94daf038a686357a5aa8ad86c4d4a`  
		Last Modified: Tue, 09 Apr 2024 16:13:01 GMT  
		Size: 33.5 MB (33495325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0141748d4e82c86d5154319edaf0457493feae76bb179fa11dc168969b7d42d2`  
		Last Modified: Tue, 09 Apr 2024 16:12:59 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:2bbf68f7aff8657e4e12a3182cdce39ec53e04eb884058fdfdad58def3046242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15310920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bbe240775e956f10760325b77e55e6323a753e0a146c43b4536817adeb3864`

```dockerfile
```

-	Layers:
	-	`sha256:a580b1fa64ebfd37d245394918a881be80e81f20ac8a8687d5eba0b152f90b5e`  
		Last Modified: Tue, 09 Apr 2024 16:12:59 GMT  
		Size: 15.3 MB (15286322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5858f511ca7af8a95ea49b9a0c9ec028b72c90a160a963c4382f7a3a73849034`  
		Last Modified: Tue, 09 Apr 2024 16:12:59 GMT  
		Size: 24.6 KB (24598 bytes)  
		MIME: application/vnd.in-toto+json
