## `ruby:latest`

```console
$ docker pull ruby@sha256:b115187645c80fa80a7b23dec345debb7bc4b03f34d27573a87ede7bb5dd43f1
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ruby:latest` - linux; amd64

```console
$ docker pull ruby@sha256:81d9588176ae2d584c753d3896a84190db8158748266b54e31445a888a72fbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **420.9 MB (420910202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25e0f5a8be804b9b2a9df6877717b6a95e1c6450f495a224d8ac1e734cd0108`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:07:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:46:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:08:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 02:10:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 02:10:42 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 02:10:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 02:10:42 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 02:10:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 02:10:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 02:10:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 02:10:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:10:42 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 02:10:42 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22766554d6bfa95c7325b00ee002f2705a7b8605908c3eb43dbe729c412422c`  
		Last Modified: Mon, 08 Dec 2025 23:07:43 GMT  
		Size: 25.6 MB (25613863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2d358b447d091790c5ef0943550bbcf57bac46c4b8bfcfc3e6dacf4cb7969`  
		Last Modified: Tue, 09 Dec 2025 00:06:46 GMT  
		Size: 67.8 MB (67778647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd420cee8193b72cf70974a80e88896c8e58d925edd1cdc515b203ff7aa65550`  
		Last Modified: Tue, 09 Dec 2025 00:47:38 GMT  
		Size: 236.0 MB (235974801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d09d7367aee8488fafdf2bc69282ccabcce7b3f69450e7af73a4133f9e9e05`  
		Last Modified: Tue, 09 Dec 2025 02:11:08 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199c12f82a826dba09a41b69ff6622edf75583316ea9d6d7a17ea804e574b40f`  
		Last Modified: Tue, 09 Dec 2025 02:11:12 GMT  
		Size: 42.3 MB (42253041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403c80142a706b95d7936d88cf48da117bfb2917a6a497bcb240d7b9f43410ee`  
		Last Modified: Tue, 09 Dec 2025 02:11:07 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:5f42dd302cb1a046a7a3f8ea7e28714549b82f1f7f8049204fd10d1e0372aa60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17348747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d8f1e502a582fe21b7346fcc84012e2a46a09a96511129dbea1e89c3df3dcd`

```dockerfile
```

-	Layers:
	-	`sha256:94eedd396348bec46a14f763ba14e65c3cd87e3c1d7e309eed6f90ea1b15f617`  
		Last Modified: Tue, 09 Dec 2025 03:57:45 GMT  
		Size: 17.3 MB (17325831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656e9c11c089ab2908de7324b51ef4c8c06c81473735fb020fc0d5370404ef8b`  
		Last Modified: Tue, 09 Dec 2025 03:57:46 GMT  
		Size: 22.9 KB (22916 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; arm variant v5

```console
$ docker pull ruby@sha256:dffdae3199e1c667830d4f804bcb329987c13b8582473b93beaec297e066b452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.9 MB (380922551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13aaef559292b2624f2b1b932da9775ee4493455160713546705460cd15fe0d3`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:08:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:31:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 07:16:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 07:22:26 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 07:22:26 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 07:22:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 07:22:26 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 07:22:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 07:22:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 07:22:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 07:22:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 07:22:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 07:22:26 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:d5c9e476f1b8d1f67ce6ab99ac45c57bfe3b7cbada7b61c1dbd969f0656bfff9`  
		Last Modified: Tue, 18 Nov 2025 01:14:11 GMT  
		Size: 47.4 MB (47448757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6a9b3c9a263aa4b01f8e95a9864f401b11f5c835e6ef84b9a950304c2fcaf86`  
		Last Modified: Tue, 18 Nov 2025 03:26:45 GMT  
		Size: 24.3 MB (24345818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3022b8716a9c6d6658073ff4323d54625cb7957fc65a6802c9c4662674ae4d`  
		Last Modified: Tue, 18 Nov 2025 05:08:56 GMT  
		Size: 65.3 MB (65318586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08963fe75e5bc1bc3c1d6b56076383f72f771556c0ab8447c3c248e622fd91e6`  
		Last Modified: Tue, 18 Nov 2025 06:22:02 GMT  
		Size: 205.7 MB (205708022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:716d60bfa3a7f9f91e88640208a062dc38ceb5559a173e4c3a016c899bebb4ee`  
		Last Modified: Tue, 18 Nov 2025 07:19:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127763d9c9b8e62a753dd37e3b1cc3e74075ab102af4e824a9f671aa5148a81e`  
		Last Modified: Tue, 18 Nov 2025 07:22:57 GMT  
		Size: 38.1 MB (38101036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8474c5ec739ceca925c3c945f30aedff84c38e74fa3325db32a46b99f1dcaee`  
		Last Modified: Tue, 18 Nov 2025 07:22:55 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:3edaf602703bf4d0fe5325320de7056d232c749050ab9066fff0f1e682f42db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17111087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecab0c0cc9ae08b63cc90e7f0bb9eb48d5e0ded3daec931a9998a8b924833e7`

```dockerfile
```

-	Layers:
	-	`sha256:74bd43c68398f7d9dcc79ed4bbbcd7cd4ead58c7b539903d658f5fc185e5c6c9`  
		Last Modified: Tue, 18 Nov 2025 09:58:29 GMT  
		Size: 17.1 MB (17088033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e48ac25f6e9efbd861026894300b66afb74f7c87f8a948e044b02038a68485f`  
		Last Modified: Tue, 18 Nov 2025 09:58:30 GMT  
		Size: 23.1 KB (23054 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; arm variant v7

```console
$ docker pull ruby@sha256:4a09a143ca53446ff63b795b2884826ab6fc169bd638a7348614c173f4a8844b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363284844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d4f3de2ac1ea649cb47764446263715abd5cb2e7ef544ed78a9d82b3de40d1`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:28:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:23:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 08:33:42 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 08:35:56 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 08:35:56 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 08:35:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 08:35:56 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 08:35:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 08:35:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 08:35:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 08:35:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 08:35:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 08:35:56 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7fcec123a6a2e24d64f8dd8d3ff01f16ba0839656e71d971698d0e8151a28a21`  
		Last Modified: Tue, 18 Nov 2025 01:14:26 GMT  
		Size: 45.7 MB (45718279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebfeb92d3792e2087594f2ee9ee695fe97cc51ccaf846f755d71e0b58f7f78c`  
		Last Modified: Tue, 18 Nov 2025 04:00:39 GMT  
		Size: 23.6 MB (23620000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c45847805af09aa76d6ba7f34b42945f6767f5c3049e5027681335f35a18d5`  
		Last Modified: Tue, 18 Nov 2025 05:29:07 GMT  
		Size: 62.7 MB (62713438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7c26bb97a26732bed23444656e3bde850306d3b4a5d98a0b63b2f0257a0bb3`  
		Last Modified: Tue, 18 Nov 2025 07:37:00 GMT  
		Size: 193.3 MB (193256632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb94095e1e8c7b0f43d4578cf2fec42cb4ae6a4242c2873d21c3c670540b955f`  
		Last Modified: Tue, 18 Nov 2025 08:36:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751ba95e7e3a9b2329fb67498cf7a309f2899861ea0d178abe7ecdd29c4dcc78`  
		Last Modified: Tue, 18 Nov 2025 08:36:25 GMT  
		Size: 38.0 MB (37976161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9cd87648c743f05b513f4b3d2f8a4859d0848ac0f82f475699a34576742b62`  
		Last Modified: Tue, 18 Nov 2025 08:36:22 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:1bd0134c6a297fe2fb33fdb7bc33d0854d5a688df5c1b8ae000da4345f39e76e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17116877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370fa48ca61816b7f792d84866d76c50e2f305b75244413bcc7f3cc96e9bf2bd`

```dockerfile
```

-	Layers:
	-	`sha256:c3eee6b6492528c937b0da4a5fbcf56ee60ebac07d14a5d587d874e85bbc4306`  
		Last Modified: Tue, 18 Nov 2025 09:58:48 GMT  
		Size: 17.1 MB (17093823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8abdd61e3a0ff71b1f538b4481f03f8823ebeedf5b7dbfbf96a6f4eae32f721b`  
		Last Modified: Tue, 18 Nov 2025 09:58:49 GMT  
		Size: 23.1 KB (23054 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:0331f01417f893919923d5c90c79fa6c11ba0f2a145c65b39f604f631a606328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.6 MB (410607856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffe76a81442d76d4193cfd63829c1865dabf7f47f575a3645ca7cc0f6faeab2`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:16:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:58:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 03:03:25 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 03:03:25 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 03:03:25 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 03:03:25 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 03:03:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 03:03:25 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 03:03:25 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 03:03:25 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 03:03:25 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 03:03:25 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097d536d3c26abbb49039062f8d8e471b0c97bdfcc2ecfcfcf56545161524fb`  
		Last Modified: Mon, 08 Dec 2025 23:11:17 GMT  
		Size: 25.0 MB (25020941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb13e64d383cee6a152ac57ad29b9b1116554b1c9daab0e94464d674f3804db`  
		Last Modified: Tue, 09 Dec 2025 00:12:25 GMT  
		Size: 67.6 MB (67585014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2b4af09d0743acafc293109ad1b191f5a03a36cd1dddf8454458ced3631f5d`  
		Last Modified: Tue, 09 Dec 2025 01:17:36 GMT  
		Size: 226.1 MB (226108094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ce7e1716fe84c021676a4e1414e3352c7a40b4883da35f70f4ea7fa29d2ee3`  
		Last Modified: Tue, 09 Dec 2025 03:01:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1beb64269414b31eab789e2850fdd516c2a29b1d3287e8addb5db91895e5ae`  
		Last Modified: Tue, 09 Dec 2025 03:03:58 GMT  
		Size: 42.2 MB (42243250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dca12bde2f91a16ab4638084c73e2eff3ed316e2acfb46390b75255d89b585a`  
		Last Modified: Tue, 09 Dec 2025 03:03:54 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:f61c21d14ee133542d9b678c47af4e951fc9caf2d860a22187666778b0a9775e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17433283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8091b92823cf1030075bf62f36a21f2e7e2aa2ebe3e8ac41fa2675763149fdc4`

```dockerfile
```

-	Layers:
	-	`sha256:f7f78ee2df14bbe386c00b5c3f98ba6441806c23cccfdf347b29b8fd2fc4ef5f`  
		Last Modified: Tue, 09 Dec 2025 03:58:17 GMT  
		Size: 17.4 MB (17410185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afefaa2dd6fab379feae9a6c9c1fe04d014ea030623424a4fa839257af3e933e`  
		Last Modified: Tue, 09 Dec 2025 03:58:18 GMT  
		Size: 23.1 KB (23098 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; 386

```console
$ docker pull ruby@sha256:aadb9df8312bd2d792bee269bd97e75ef3e05536a09d93ff517da0d281dde2cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.3 MB (425285170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b13de573cd69b7bfbac0c022b9064642162e907b1b1eb33d789b766c38b358e`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:14:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:24:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:17:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:40:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 02:42:06 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 02:42:06 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 09 Dec 2025 02:42:06 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 09 Dec 2025 02:42:06 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 09 Dec 2025 02:42:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 02:42:06 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 02:42:06 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 02:42:06 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 02:42:06 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 02:42:06 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a63ab7a4f8b10d53e108dbe1e04ab9e369b75bfa91be99da84bbdfb688a906bc`  
		Last Modified: Mon, 08 Dec 2025 22:16:00 GMT  
		Size: 50.8 MB (50801649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d798fea9bbf98ef639c9ca23d745bec44c0d7b28fbd93792d4578fc5b43e7569`  
		Last Modified: Mon, 08 Dec 2025 23:14:38 GMT  
		Size: 26.8 MB (26776300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d1731e98c6e5aff4c28a002263af9a4fc5c06d23cbc860d258dafbd603ef2`  
		Last Modified: Tue, 09 Dec 2025 00:24:53 GMT  
		Size: 69.8 MB (69794656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f9ce1752769ca8894b138e7f67dcb0e328629def6e6854ee6c1fc3ea4e6dac`  
		Last Modified: Tue, 09 Dec 2025 01:19:01 GMT  
		Size: 240.1 MB (240068858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c15dcbc3c43fca5c8ebf2ccfa8b05cbcff8f79faffcec554423e284198648`  
		Last Modified: Tue, 09 Dec 2025 02:42:31 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e2cefcc79103484d5322e8a9c7fff7258daa74881be326f7a3d7a2d8083f13`  
		Last Modified: Tue, 09 Dec 2025 02:42:35 GMT  
		Size: 37.8 MB (37843375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60aa58d07d9d91c955150597bc28f0cb2bfea11be71a0844eaf0ea05d813e87`  
		Last Modified: Tue, 09 Dec 2025 02:42:31 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:bd6a3c67b528f570be47eec587905e734108ae22177485bffc6f00dce14b876a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17318259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280cefdedc2f8a2b1f208fb41fa39b7affb152d6aab7bbdb9f3ccd3231f8046`

```dockerfile
```

-	Layers:
	-	`sha256:ff8c208bf795e7d3aca9b30f1251bcde9e8ea6606e58aa0a6d458a42eaf2358b`  
		Last Modified: Tue, 09 Dec 2025 03:58:28 GMT  
		Size: 17.3 MB (17295399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:097ba42917963aba08bcb31b07ae826a7299787616df0af6c688a030f3724360`  
		Last Modified: Tue, 09 Dec 2025 03:58:29 GMT  
		Size: 22.9 KB (22860 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; ppc64le

```console
$ docker pull ruby@sha256:add55b93dd298267f04a5e2087aeba2ce0ed35966363b25931da67c34cfe09f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.9 MB (423928918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7878069baa1a3570694d18dacaa2e82577491105c4f39ecc0ecbfbebfd391186`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:53:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 08:22:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 19 Nov 2025 00:24:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 19 Nov 2025 00:39:36 GMT
ENV LANG=C.UTF-8
# Wed, 19 Nov 2025 00:39:36 GMT
ENV RUBY_VERSION=3.4.7
# Wed, 19 Nov 2025 00:39:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Wed, 19 Nov 2025 00:39:36 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Wed, 19 Nov 2025 00:39:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 19 Nov 2025 00:39:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 19 Nov 2025 00:39:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 19 Nov 2025 00:39:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 00:39:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 19 Nov 2025 00:39:37 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ae38687874ad4b2ca525fe856d3d2a658b265c8f3cd684d6e8c1efb9f28a6bb3`  
		Last Modified: Tue, 18 Nov 2025 01:57:18 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a859b52534a1e3522c593c1835bd1bee34ff20a865f32f140257d45048a18099`  
		Last Modified: Tue, 18 Nov 2025 04:09:23 GMT  
		Size: 27.0 MB (26996919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba2b1a22ff6e7093fdd1dd2648adedf5202ef1304de7d17f711c19601d3a80e`  
		Last Modified: Tue, 18 Nov 2025 06:54:27 GMT  
		Size: 73.0 MB (73021903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8c7b0e7e39934178ce53a9a8f734eb91b249eb1d93ae50bc043579a195efbe`  
		Last Modified: Tue, 18 Nov 2025 12:40:13 GMT  
		Size: 231.1 MB (231098714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8532be2ddad34aea8551944548281480294358bd0d4d5c29246bec25fe4ca587`  
		Last Modified: Wed, 19 Nov 2025 00:28:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af957144670a9c2dd7e8cdb69bbe836a329a7681a95d673ab11db9b9e888f1f8`  
		Last Modified: Wed, 19 Nov 2025 00:40:48 GMT  
		Size: 39.7 MB (39702564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9367111199fd470f345542940337c30fca3485a9634fd6f1c8e85212a629ba`  
		Last Modified: Wed, 19 Nov 2025 00:40:33 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:fea826a8da10a9f46a51d0c8e3183fd3bf23c66d28f7a08d2dde92e1ebed2b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17334362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5027efcb4897296bf5bbe832db3320bcb3bede8539a00ed421ade4dea81d8296`

```dockerfile
```

-	Layers:
	-	`sha256:fe266c7e6126076319b334eb73332b6f27ffb8e4e3071c5c8251f4926f241d36`  
		Last Modified: Wed, 19 Nov 2025 03:58:27 GMT  
		Size: 17.3 MB (17311374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfa842643431b651b9b80960f4d01a2ea4c3c415f62bab98a085219dcea1e83`  
		Last Modified: Wed, 19 Nov 2025 03:58:28 GMT  
		Size: 23.0 KB (22988 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; riscv64

```console
$ docker pull ruby@sha256:235c48cd0f70f4cac208f0ccb8672fd483c67b5a58bc7940d7fade741482a944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.4 MB (500387232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8bae168862a0961195f6fc00516a36d34d53e4604cf923bb9504b5835a1942`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 19:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 22:28:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 22 Nov 2025 21:51:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 24 Nov 2025 08:33:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Mon, 24 Nov 2025 12:38:58 GMT
ENV LANG=C.UTF-8
# Mon, 24 Nov 2025 12:38:58 GMT
ENV RUBY_VERSION=3.4.7
# Mon, 24 Nov 2025 12:38:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Mon, 24 Nov 2025 12:38:58 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Mon, 24 Nov 2025 12:38:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Mon, 24 Nov 2025 12:38:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Mon, 24 Nov 2025 12:38:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Mon, 24 Nov 2025 12:38:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 24 Nov 2025 12:38:59 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Mon, 24 Nov 2025 12:38:59 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ed0507b92b5f6d1bbf086936336ca6e85b2d0afbbaab333064cc752190ce52b9`  
		Last Modified: Tue, 18 Nov 2025 01:45:17 GMT  
		Size: 47.8 MB (47771195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccc0dcc6b4231d5f1f223a1330c6630cb9406136f8e738cb2b0e628d1b35022`  
		Last Modified: Wed, 19 Nov 2025 19:38:34 GMT  
		Size: 25.0 MB (24953736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e592ded610a658bb788aebd62d933a07876ce0d2dff630e8511ac1eda3d0dbb`  
		Last Modified: Thu, 20 Nov 2025 22:32:10 GMT  
		Size: 66.7 MB (66660961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0946283142630ddc0be55b717109fdc10f4f3806b47ec32301b162ca5d92b2`  
		Last Modified: Sat, 22 Nov 2025 22:12:30 GMT  
		Size: 322.9 MB (322888286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5aa251c207dbea3eb243b066e293aa12e8b8633d8ef87c101ec112378adba7`  
		Last Modified: Mon, 24 Nov 2025 10:36:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896b80ba76733f95ce5a04c66ff729c44ff16db2cdd28a78b5e26788138d767e`  
		Last Modified: Mon, 24 Nov 2025 12:47:33 GMT  
		Size: 38.1 MB (38112722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bc8d16944a427e3f4f5c2b15c4d9061c725073665c92cf173f46124cdba151`  
		Last Modified: Mon, 24 Nov 2025 12:47:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:e0ce30f098dc0fe63a8a8cbead6bb0494d9290407ae71c417fdd00db6e011d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17404950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97bc1b25e08ccfe6f4211831cb46b0ac5b401fc61e90f76f87c7a5306a2be2ba`

```dockerfile
```

-	Layers:
	-	`sha256:120ea964c56f44bf51fee1998f66d586b41ad43a9c421e5cfa6c9096cbcdc4bf`  
		Last Modified: Mon, 24 Nov 2025 15:58:37 GMT  
		Size: 17.4 MB (17381963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2efd2ff89a65510e4eb54a453454317f6eb8aa334426e9002316abd9b3b0dc3c`  
		Last Modified: Mon, 24 Nov 2025 15:58:38 GMT  
		Size: 23.0 KB (22987 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:latest` - linux; s390x

```console
$ docker pull ruby@sha256:8ca002518c154d2351b36f1cf7baec04727a8e252c10c502f04e694eeb4eb8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.6 MB (390631148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4844123e25f85c5e666e2ce09ccc4d74ba928154d43b0644772901cb5f9ca4df`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:57:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 07:29:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 11:38:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 11:44:36 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 11:44:36 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 11:44:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 11:44:36 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 11:44:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 11:44:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 11:44:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 11:44:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 11:44:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 11:44:36 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:af4c50a2cf2848edb9e1797defa12d9a203416cf14b67469a37a418b1d0bb175`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 49.3 MB (49346014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f811fd500c593f696ff4afefd96c823d7f8788d50f510057207bfc40b4a405ca`  
		Last Modified: Tue, 18 Nov 2025 04:06:46 GMT  
		Size: 26.8 MB (26786539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4530c943529730620c01f6bab681e114e8a52bebc697a9164bab0bee08dc992`  
		Last Modified: Tue, 18 Nov 2025 05:58:03 GMT  
		Size: 68.6 MB (68624056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac50f1d81c5e7e8663edcaac3894486402190c64a8bddf0d22e71c268724934`  
		Last Modified: Tue, 18 Nov 2025 08:14:52 GMT  
		Size: 206.5 MB (206473602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898fc0fe5baf1f9a31064638fd5d66e03134ce6ce30cdb53018c7c674ea2530b`  
		Last Modified: Tue, 18 Nov 2025 11:41:09 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e582f2b3dd9ab9cae7868668228fa5dd2961ec74bc853a04dd739425e2e84eea`  
		Last Modified: Tue, 18 Nov 2025 11:45:30 GMT  
		Size: 39.4 MB (39400606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7358e8c8ddd20a9b5c98063350c0e589c671dedf7dd34841ac90044f806f48d6`  
		Last Modified: Tue, 18 Nov 2025 11:45:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:latest` - unknown; unknown

```console
$ docker pull ruby@sha256:75de8d04f5b4c77a526ef24c4357eb26836fc64a94d25acfb7a5b6edac63a37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.1 MB (17125944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb47d7e1f5654d7766f85f706a5efa057fc710052542d04723a041ff3ef620b`

```dockerfile
```

-	Layers:
	-	`sha256:7f44b9b44e5bb114f22b45cc7afebb996dacaaec930cdd7082ec6132fc735868`  
		Last Modified: Tue, 18 Nov 2025 18:59:06 GMT  
		Size: 17.1 MB (17103028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e750b901971bcde6e0abc5095fdeac1b070c36cee4d532810e312b2960e323`  
		Last Modified: Tue, 18 Nov 2025 18:59:07 GMT  
		Size: 22.9 KB (22916 bytes)  
		MIME: application/vnd.in-toto+json
