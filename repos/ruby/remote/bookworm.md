## `ruby:bookworm`

```console
$ docker pull ruby@sha256:543886cca6a12761a27a3d2da392a36b0771e2503dc98149e08a9af72af95b3a
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

### `ruby:bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:090961e372013fd63a0de53f414e5f6cb81d77836234e68832dd95f2920d3f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385454739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514e1196556d44969fd13be9886f60533dd95aa5064956997a283c1874185126`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:54:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:55:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_VERSION=3.3.3
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.3.tar.xz
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=83c0995388399c9555bad87e70af069755b5a9d84bbaa74aa22d1e37ff70fc1e
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 05:03:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891494355808bdd3db5552f0d3723fd0fa826675f774853796fafa221d850d42`  
		Last Modified: Tue, 14 May 2024 03:04:06 GMT  
		Size: 24.1 MB (24050100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6582c62583ef22717db8d306b1d6a0c288089ff607d9c0d2d81c4f8973cbfee3`  
		Last Modified: Tue, 14 May 2024 03:04:25 GMT  
		Size: 64.1 MB (64142371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2c3e352f3d2eed4eda4feeed44a1022a881058df20ac0584db70c138b041e2`  
		Last Modified: Tue, 14 May 2024 03:05:02 GMT  
		Size: 211.2 MB (211207185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0034e4e6001692bbd9f76afd3f7b3c9363f9b5dabf08c05ec769eb49c6061f`  
		Last Modified: Wed, 12 Jun 2024 17:59:43 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef6d5ae589b77c035e6f59bc76397804b86c70561278f1346b83ff4bfcae651`  
		Last Modified: Wed, 12 Jun 2024 17:59:43 GMT  
		Size: 36.5 MB (36478351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3866893b9c74560599d4128e83e550d6955da7e72f957195037cfdf664b4e49d`  
		Last Modified: Wed, 12 Jun 2024 17:59:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:8c6bc2159edfe99584f342d3d00e1f8b870ecf1aa194fc5e28b72c16543f9532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15485650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a35d9dccec36629d6cb43989231c2317a7439a7f2f01878f7a221347bc5233f1`

```dockerfile
```

-	Layers:
	-	`sha256:fde140127dd17dd5c82beb1747bf30e18af29d80a0927f55525a8eefff6b45b8`  
		Last Modified: Wed, 12 Jun 2024 17:59:43 GMT  
		Size: 15.5 MB (15462259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a254e79e6a59797818ae74f021491bb3a1ec9e77bb2906a56aad2461597d397`  
		Last Modified: Wed, 12 Jun 2024 17:59:43 GMT  
		Size: 23.4 KB (23391 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:249ba95c1133d57a6437eddc94c5301efc11779b78d88f9eda0f15f5e2e08cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.0 MB (349015049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241d4c72f838608fe6bb7902796c5718d4b2430603966f9f18b067ad1f0c0b08`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:48:25 GMT
ADD file:cd62e5a70676cac6ab9314bf7583f7ed4056908c492f302f1243edbd35066bfd in / 
# Tue, 14 May 2024 00:48:26 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:13:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_VERSION=3.3.3
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.3.tar.xz
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=83c0995388399c9555bad87e70af069755b5a9d84bbaa74aa22d1e37ff70fc1e
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 05:03:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ec3129b1f3b893a7412a0ac12044f811ed32ddf7028d374141819005f9d4699f`  
		Last Modified: Tue, 14 May 2024 00:51:10 GMT  
		Size: 47.3 MB (47338294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8516852dedc6ef6e011322d36853e449786d3c2d43553864edbb79abbe0ca5`  
		Last Modified: Tue, 14 May 2024 01:21:47 GMT  
		Size: 22.7 MB (22728407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f71408c4e77f143b3e9d4c1401b7c778766c63dc79d80a05870500825e7c8c`  
		Last Modified: Tue, 14 May 2024 01:22:09 GMT  
		Size: 61.5 MB (61517869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779bb0cc1f42107df5966cbf82ca7be2fb113ac0edf35633f10fbd5d5cce3ada`  
		Last Modified: Tue, 14 May 2024 01:22:47 GMT  
		Size: 184.5 MB (184522613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f8b51aa244ef3947dd448a80bd8d6c5abd4bf04f971fe43cb6300c9421e703`  
		Last Modified: Wed, 12 Jun 2024 17:58:44 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8fcdbd15171c5c0ced19d802760586d673f4a10bb5e91f54d7d467c14060eb`  
		Last Modified: Wed, 12 Jun 2024 17:58:50 GMT  
		Size: 32.9 MB (32907525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fce86e8dce3d316edc7fef50b50bff693c1580417b04a1c91ef4968d796f0aa`  
		Last Modified: Wed, 12 Jun 2024 17:58:48 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:6ba2186740da1ce659e8f356594ec3fda56110f923a02b737fdd2901208faa65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15286172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ac968321f281454907f3fc85f08ee3d0f59e09eb3ef254cc9b53c45545f059`

```dockerfile
```

-	Layers:
	-	`sha256:c7b7229e6b0551e8d8abc6c3841398acda8326cf9f83cd952740ec7c19cd5286`  
		Last Modified: Wed, 12 Jun 2024 17:58:49 GMT  
		Size: 15.3 MB (15262653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9e8cef025c4857d58bd3f03318f9033e9e0dff62b9e23f1a06cc18b8a456456`  
		Last Modified: Wed, 12 Jun 2024 17:58:48 GMT  
		Size: 23.5 KB (23519 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:fe54a9720ad192f7b8f8ff19728bf73eb3b0fad60f9204b397b1605dc6d1342a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334303887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b889de1deebab76d730236d7c2cd958ed6899b328a1695f5898a6d1862c6091c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:08:35 GMT
ADD file:1e106a38a0e44ca74d4d29c6d797780e7a29ffe249e473c48ee2aea553fc013b in / 
# Tue, 14 May 2024 01:08:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:35:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:35:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:36:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_VERSION=3.3.3
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.3.tar.xz
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=83c0995388399c9555bad87e70af069755b5a9d84bbaa74aa22d1e37ff70fc1e
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 05:03:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:dfc3b4ca62816a9cbf2bdfbdd78bf692a522e7f48a280492b9f87d55b2f4aa2e`  
		Last Modified: Tue, 14 May 2024 01:12:21 GMT  
		Size: 45.2 MB (45174745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641d6443415d538c3bf0e0d6ecc0f6b7603b4caf6c79708d0670bc082e9721c5`  
		Last Modified: Tue, 14 May 2024 01:46:47 GMT  
		Size: 22.0 MB (21953893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dd085f2eef9c35615ce8d6f2e7b6340a6bcadb37fe8fd6698911eab87e371c`  
		Last Modified: Tue, 14 May 2024 01:47:09 GMT  
		Size: 59.2 MB (59217124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1ddacc8c148925155abdd912bfb78a553326599c4da7b21c01a76f7616a464`  
		Last Modified: Tue, 14 May 2024 01:47:48 GMT  
		Size: 175.2 MB (175175139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b4613b59305be7d70d7fed0abe80f93d329c150ace480e1e1c7d66c0ffa1b7`  
		Last Modified: Wed, 12 Jun 2024 18:00:57 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab3c1fac662c18bcbff23ee97ed501c07d1a923d2b73a7c5b28cf3ef41e095a`  
		Last Modified: Wed, 12 Jun 2024 18:00:58 GMT  
		Size: 32.8 MB (32782644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c98e6dde9446c961ba3b0596a48738c0037795f455a41c39811aaee6c148c9d`  
		Last Modified: Wed, 12 Jun 2024 18:00:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:37ee86572cd02f2499488e8bb6ca7ed99c2a3d936c909deac8bfadb2e6d09498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15291645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720fd93a91a8e69fe7987cf942d61c0dfd48f7b674d48a26a43a6f18d3aa1bfa`

```dockerfile
```

-	Layers:
	-	`sha256:741ecc9ce92ce8baf9443d80d29df231d91c6694e138078b07d399afc3c72794`  
		Last Modified: Wed, 12 Jun 2024 18:00:58 GMT  
		Size: 15.3 MB (15268127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bc437dab7c6ae6b178da686d26d8ee4bf5a2a5becfc741aa0f06b4ae1071f4`  
		Last Modified: Wed, 12 Jun 2024 18:00:57 GMT  
		Size: 23.5 KB (23518 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:059e200e30d3dd50c11b0009ab31ebea1053860ab5ed452bb7e3e2e575e3432b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.3 MB (376301820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f816f252123347e780f0643a7356fc6016f31d6fd8b754f33bdbf071d3c53d`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:44:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:45:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_VERSION=3.3.3
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.3.tar.xz
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=83c0995388399c9555bad87e70af069755b5a9d84bbaa74aa22d1e37ff70fc1e
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 05:03:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15856ca26414127b85cee6d10acbc4cee6eba9070f3f5a04b9cc72ce95abfa7f`  
		Last Modified: Tue, 14 May 2024 01:52:50 GMT  
		Size: 23.6 MB (23586610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30ed4c12791345d3f20f66024e1f22275ce507868c508509b83dcf231b1c9adc`  
		Last Modified: Tue, 14 May 2024 01:53:09 GMT  
		Size: 64.0 MB (63994370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb30c5ba2d151512d29ff4b92109a740559509ef6f3072a86c5006a1379397b`  
		Last Modified: Tue, 14 May 2024 01:53:41 GMT  
		Size: 202.6 MB (202593312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d632dffd9e751efa94231469f56b8d0b5c392d36ae8d7353b1ef01ccc9a1a0f`  
		Last Modified: Wed, 12 Jun 2024 18:44:07 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5596f5c9a16ee3b64d50f3c6f5c135325b4696730df04ddd657f8f975d625b0`  
		Last Modified: Wed, 12 Jun 2024 18:44:08 GMT  
		Size: 36.5 MB (36513797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba3a46e953e86a39f47e6091b5780accd9283b9d319f5aedb14d13e3b612754`  
		Last Modified: Wed, 12 Jun 2024 18:44:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:66a2ff15715a33af5ba141191cac9d1b0d06807de072206454af0bf57786a019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15514614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d4e0196c9d4bf286f2ba0a8ff51b8dcfb01459f07f4821b201935edb7332d0`

```dockerfile
```

-	Layers:
	-	`sha256:d791ed5341e70163825049428c7244031cf8ab7df6a3d5dffe36f1962375cfa8`  
		Last Modified: Wed, 12 Jun 2024 18:44:07 GMT  
		Size: 15.5 MB (15490863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4907cef612c5d423243edb1a79b2c5f2186e2750a3aea0f42c7515d04b7acdc`  
		Last Modified: Wed, 12 Jun 2024 18:44:06 GMT  
		Size: 23.8 KB (23751 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; 386

```console
$ docker pull ruby@sha256:ac25da6445432c55eb4a63a9974e89469f5fb43f60c0cf6a039c3efc589b7f40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.3 MB (384314901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc81d9c0c0e10d8dc6ac29a61a8b3ca12662ad27e6afdb1ed24032aa45b29c9b`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:47:00 GMT
ADD file:35709674a3b845511a896af16ea37a6022e7d48992d3198d0760c0c3208fe4ed in / 
# Tue, 14 May 2024 00:47:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:01:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:01:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 09:02:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_VERSION=3.3.3
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.3.tar.xz
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=83c0995388399c9555bad87e70af069755b5a9d84bbaa74aa22d1e37ff70fc1e
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 05:03:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:4f2f2f6205661e555e772749ae7fd294fb04fc0d06cbc67a50a11fbb4ef44242`  
		Last Modified: Tue, 14 May 2024 00:51:31 GMT  
		Size: 50.6 MB (50602424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d849fa81a6965e2bbc8dd9af462f55a46b59aeb701fb0a26992522fd43ce5c03`  
		Last Modified: Tue, 14 May 2024 09:13:04 GMT  
		Size: 24.9 MB (24888551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d6250e2e75fd4f1cdc533096df2c601817950e8c3f1096f46dfeea2b609cee`  
		Last Modified: Tue, 14 May 2024 09:13:29 GMT  
		Size: 66.0 MB (65988940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e0a2d5e90c1a7093dbeeaddbb7c833c828015d2e8991c1721c4a269c4faf42`  
		Last Modified: Tue, 14 May 2024 09:14:20 GMT  
		Size: 210.1 MB (210128367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c63d98ec01b02fa1aeef1a3a0fb231f96ed7187089276bfccaf76ffa7ad377b`  
		Last Modified: Wed, 12 Jun 2024 17:59:42 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38de646bc464cf808c36c90500c24c781e635213271a2b9e6518e43e2a817216`  
		Last Modified: Wed, 12 Jun 2024 17:59:43 GMT  
		Size: 32.7 MB (32706276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938b8dd8bcfb9e9989552ba13bb196af6a0a8387ca4e73b6f9dfc53ae5d4fd63`  
		Last Modified: Wed, 12 Jun 2024 17:59:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:c0b316252a57f83bfffc50b35621d1b30e3e6a05ea8de50fba48c8ca64a0004f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15464644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9f72880021337c90a31f13bde047659e84cc0cb3f75fb61114e3c699d4ff2`

```dockerfile
```

-	Layers:
	-	`sha256:fda4cf4c041fc83e962001a301d949745bf520017e5b941b59ced2872f4dbffc`  
		Last Modified: Wed, 12 Jun 2024 17:59:43 GMT  
		Size: 15.4 MB (15441306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59cdef841b6fd06a22832ab7b9cef443445c4440552940be5b5eeeb0e2670983`  
		Last Modified: Wed, 12 Jun 2024 17:59:43 GMT  
		Size: 23.3 KB (23338 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:90ad8720d6b0439ed48b4cabdef8465017e63ba78a080866d0bc80761828c07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359686353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d0bfad7755dde4e32cfa9667db2d92d368b763784454258c518407dffe9a35`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:10:23 GMT
ADD file:95717416297a85e0b38d171b3bf8d2b48e941bd725e476ee4f88033fed4ffee2 in / 
# Tue, 14 May 2024 01:10:29 GMT
CMD ["bash"]
# Tue, 14 May 2024 10:59:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:01:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 11:07:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_VERSION=3.3.3
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.3.tar.xz
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=83c0995388399c9555bad87e70af069755b5a9d84bbaa74aa22d1e37ff70fc1e
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 05:03:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0fd7e383bbed45ca14b36b1e22f1591a0b2bddc34b2b6e2b34d4cd54b528e75f`  
		Last Modified: Tue, 14 May 2024 01:21:36 GMT  
		Size: 49.6 MB (49582338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ce1d8a69726b5d3330ae01a246efbb18fb60d54fb0d08b741a960e37d8b115`  
		Last Modified: Tue, 14 May 2024 11:37:05 GMT  
		Size: 23.4 MB (23438164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3667485c8dcf18ff23740eff9103874ec0aba9a4d45bade2f98f9f85fe0f63`  
		Last Modified: Tue, 14 May 2024 11:37:57 GMT  
		Size: 63.0 MB (62968511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3514ef59a25de65d0663fc4a360de7a712214c493290dd77858247edbd0dac`  
		Last Modified: Tue, 14 May 2024 11:40:05 GMT  
		Size: 189.8 MB (189771182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033f4444faef863b4ec603023f287bbb77f89819b9287bcb98a3becb8ec5c154`  
		Last Modified: Wed, 12 Jun 2024 18:09:42 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e4afa84c5f944bfaafba6be54ec85f00dd79e71e9b67aacd36564520c165ce`  
		Last Modified: Wed, 12 Jun 2024 18:09:46 GMT  
		Size: 33.9 MB (33925816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b139b1794f06616748b32434a25df82a543949701473b33a2c12900493c1e1e`  
		Last Modified: Wed, 12 Jun 2024 18:09:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:1b5974457aa99d99fa3aa0449e090e40baddc23bcf1d58e203d6aacb131fb3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 KB (23270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718200d37c294f98155ad7012860ac96668ccd6c29de208e9a7ebf2b0b61fd00`

```dockerfile
```

-	Layers:
	-	`sha256:f926507f1ca401069c494701dbfba845429f42aedfb8b1e6d5483aa2452d6851`  
		Last Modified: Wed, 12 Jun 2024 18:09:42 GMT  
		Size: 23.3 KB (23270 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:c4424666c61ced9ca776d5e88c3628b6c47225e4f461b2ca67ca25683f38acef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397398418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4278a04e6c89d6c9864ed900909cf6800330799f0c18c4ce029b3f0a7f127374`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:19:48 GMT
ADD file:fdb5c89e2970bd3b21a7b4e39491c1719b957f54babefd52ad455ea72a77bd3f in / 
# Tue, 14 May 2024 01:19:50 GMT
CMD ["bash"]
# Tue, 14 May 2024 06:55:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:55:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:57:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_VERSION=3.3.3
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.3.tar.xz
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=83c0995388399c9555bad87e70af069755b5a9d84bbaa74aa22d1e37ff70fc1e
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 05:03:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:9027b64136d8b1ece1ad24cca3199e496689a33f47b8d112dbdd112c682e665f`  
		Last Modified: Tue, 14 May 2024 01:23:40 GMT  
		Size: 53.6 MB (53579748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e147daa0a988c77940b565d177a661a73270a0e821c65283b9e531ae38ebc4`  
		Last Modified: Tue, 14 May 2024 07:10:25 GMT  
		Size: 25.7 MB (25699676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88d9ff0405bb000dedfa15a3a34739370c3daa10367599bff02a57fd19a3564`  
		Last Modified: Tue, 14 May 2024 07:10:47 GMT  
		Size: 69.6 MB (69584088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b80be54620660eb7b908f8c79a7ad14bedcac29ae46f620f4ede820441dc65d`  
		Last Modified: Tue, 14 May 2024 07:11:29 GMT  
		Size: 214.2 MB (214234653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f8b51aa244ef3947dd448a80bd8d6c5abd4bf04f971fe43cb6300c9421e703`  
		Last Modified: Wed, 12 Jun 2024 17:58:44 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9291adfb1cc4853b9ba26d7c0ba9aa3084731ce5252110ebdf6a25f68975f303`  
		Last Modified: Wed, 12 Jun 2024 17:58:45 GMT  
		Size: 34.3 MB (34299911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be787cb3344de5eb6779bdb100fc61c6b9b80329d2b489d2479ab595aaf8b896`  
		Last Modified: Wed, 12 Jun 2024 17:58:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:7245ad87a32d065b65b6d41ba5f86300a4bfb9954f721e569d1e16b79a0fe80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15462413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bfd1a8ef830139b06eda1f4f9e4d4a7ebf40e6222ba252a49befd172d9438df`

```dockerfile
```

-	Layers:
	-	`sha256:b2db1eefa8e470987d421ec735627b87d2c577c3bdda0a158c3f234e3846b7fb`  
		Last Modified: Wed, 12 Jun 2024 17:58:45 GMT  
		Size: 15.4 MB (15438957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b75aa69a7306f188a66755bf617cd304e217670d93d15313cf91ca14a6da32`  
		Last Modified: Wed, 12 Jun 2024 17:58:44 GMT  
		Size: 23.5 KB (23456 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:cf1ac60b6bb6cc170a00b8a0d59419980b182537e2b6c8131b2d714b346978de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.9 MB (351910228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a422cb9d89d6cf4cad223b17ef3638012b0992cbf96003b153cc956564149ee`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:42:19 GMT
ADD file:d24c16f113416f94273813df324360fe934245f0f7f2973b6def2799e5605f1f in / 
# Tue, 14 May 2024 00:42:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:19:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:21:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV LANG=C.UTF-8
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_VERSION=3.3.3
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.3.tar.xz
# Wed, 12 Jun 2024 05:03:19 GMT
ENV RUBY_DOWNLOAD_SHA256=83c0995388399c9555bad87e70af069755b5a9d84bbaa74aa22d1e37ff70fc1e
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 12 Jun 2024 05:03:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Jun 2024 05:03:19 GMT
RUN mkdir -p "$GEM_HOME" && chmod 1777 "$GEM_HOME" # buildkit
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b9285660d64168cd1c05bdfee5186da3634a289a06300d8ea12e57df80e4648b`  
		Last Modified: Tue, 14 May 2024 00:47:17 GMT  
		Size: 47.9 MB (47942190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c304d55d9ae47fcef54a6044634995ffbdbd5e4d3e409198127615b4043fa8b`  
		Last Modified: Tue, 14 May 2024 01:29:23 GMT  
		Size: 24.0 MB (24046857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943219d44d0b66fa3c53413ccd4b689951925725722eba1e47eec984778d3640`  
		Last Modified: Tue, 14 May 2024 01:29:39 GMT  
		Size: 63.1 MB (63130182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dd19c695c401ade3f0a1af6a11007c474b68b17b925095492dbfc5a8f2a538`  
		Last Modified: Tue, 14 May 2024 01:30:07 GMT  
		Size: 183.2 MB (183236787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bc1551e7ba19517cf19dea14e83583ebcbc34c8b4c8fa34d7a3fe4bf056aeb`  
		Last Modified: Wed, 12 Jun 2024 17:58:22 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984dc4526b8c9d0adf543edc4188413a7b4d83f9b66d75324ba9c9e525a119b6`  
		Last Modified: Wed, 12 Jun 2024 17:58:23 GMT  
		Size: 33.6 MB (33553869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f08852cac3d407c6824b72c7cab32fd6be8510ec71043dfe7711a09b4633f9b`  
		Last Modified: Wed, 12 Jun 2024 17:58:21 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:bf98c2356be2c3ca5cefe1c99cfdbca5daccc7828368eb8ed2959185ce8c3ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15300332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc334cfb11206f2b22970505a9be39ccc7ed94fda9cf7a063741b6064684894`

```dockerfile
```

-	Layers:
	-	`sha256:67b8c156abb6031c85f2a68517207c0b33c111c71398713751857c2a17ee66b7`  
		Last Modified: Wed, 12 Jun 2024 17:58:22 GMT  
		Size: 15.3 MB (15276941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:405ee36d186eb6c2c5eef03f1ea4512981219729081cb45dd14aba228ab264ce`  
		Last Modified: Wed, 12 Jun 2024 17:58:21 GMT  
		Size: 23.4 KB (23391 bytes)  
		MIME: application/vnd.in-toto+json
