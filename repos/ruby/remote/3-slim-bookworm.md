## `ruby:3-slim-bookworm`

```console
$ docker pull ruby@sha256:2f01f2025a993a5116a6e984de0ce126f5e40e83bf9537715ba121ab280530b9
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

### `ruby:3-slim-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:dc1b3167644c703be3b902c3503fe77b62644640de526a60bbe7ba4fd5df27f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80839004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17afa0efcad98752ecc86a184207eeccde53b9f1666a49b7ddfe9213775af07a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e802048eeaf1776078dd0416bd8350febc99354d2af769de1df5f8b33c890a1`  
		Last Modified: Thu, 17 Oct 2024 01:19:37 GMT  
		Size: 13.9 MB (13861855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b78745c2c7ee72f554a9dcddfecc3be421981045a7e8d3da703e56119d694d`  
		Last Modified: Thu, 17 Oct 2024 01:19:36 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c16f61da99713e921a458a30ffa46cc4608bd685239e5aa8e6d2c91209979d`  
		Last Modified: Thu, 17 Oct 2024 01:19:38 GMT  
		Size: 37.9 MB (37850519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0792d96dde405cf15f55db93e4c3460bf3b9cc63fb221cd499611e4d6a625a`  
		Last Modified: Thu, 17 Oct 2024 01:19:36 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:2ee817c5cf1ee00b44ab350cdc874dfa4b7cd5195a323a3bedcd2345b9fc42aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892403ea5de29554555868a06b824019735a25982c03d30eb42c56bd3f7e6f26`

```dockerfile
```

-	Layers:
	-	`sha256:917d1df39dcb1a7fa9a1c98af87a6ad7c6acb6e41b18a70ca8fb317a0a6a87f8`  
		Last Modified: Thu, 17 Oct 2024 01:19:37 GMT  
		Size: 3.9 MB (3898470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df28a95705456f7b5cffa1a11398c98096603b00cf1075d0e4c1f29cf77d53ad`  
		Last Modified: Thu, 17 Oct 2024 01:19:36 GMT  
		Size: 24.9 KB (24862 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:06d8d3e10d7d156dfe963e0570de08d18cb77fdae33e93c374675e2682826457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72697775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a49f1a8b48241b0bfde35be7c5ada6cf96c28b3426bb30ba3c11f8ddd6bd48f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45845df8f6f470d7a059a7929530fe5fe9f9c235b398cc7ca33942bb8a61880`  
		Last Modified: Fri, 27 Sep 2024 16:15:32 GMT  
		Size: 11.6 MB (11619729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dafdc7b73c599d0ee3cfa9f4b5a540c2c1046536633de446f2f2e502766b47d`  
		Last Modified: Fri, 27 Sep 2024 16:15:32 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3234126023253534f2d673c74699128b882c2e2c95cf416fe1674c95b97688f`  
		Last Modified: Fri, 27 Sep 2024 16:21:31 GMT  
		Size: 34.2 MB (34190407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7726724c1b52a3b16fe7d9b594652bb5f46b28bf4840c9b160b1f805bb3c1f1`  
		Last Modified: Fri, 27 Sep 2024 16:21:30 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:2a0684b38d36c99bcfceea4b20ef7d13f0708ac8c2cfd1ffd3b930004331ec6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3893876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fb7edbfc2ad23888a14006faf9d39fc62dd1977c38a65484fbbf5bf620ae70`

```dockerfile
```

-	Layers:
	-	`sha256:af785516c8c21757a577b12869ec63ab0a4093a31e525a7058e29f45a82cb2e8`  
		Last Modified: Fri, 27 Sep 2024 16:21:30 GMT  
		Size: 3.9 MB (3868911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6647afe1d2ef4c5d18314b42f9cc6ab32ea31d96622fb2281cc652e3e11d1f32`  
		Last Modified: Fri, 27 Sep 2024 16:21:29 GMT  
		Size: 25.0 KB (24965 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:15570207943863a3c23cd1b5457be173fcedaf4fd2ec1c43c8bb547334267081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69744467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a4c1e54a6c1f1a56ea452ede8c7b07e82658f698d12cb429fb18f521e4dd2`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2005f2a876bff1ca6153e9909b25938fb86673586af00dbd8d16eb6781a3be0b`  
		Last Modified: Fri, 27 Sep 2024 18:17:59 GMT  
		Size: 11.0 MB (10959430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784a99331e9d3b665abd563c84ab3ce402febb0735ccc148da2ff4054e0350a2`  
		Last Modified: Fri, 27 Sep 2024 18:17:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593ec9affec018f115b8aa76645eb24d33491c9aa662450fe1d68c8d6f5b72fe`  
		Last Modified: Fri, 27 Sep 2024 18:23:57 GMT  
		Size: 34.1 MB (34066554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51d8c93ddc47548f096565118a8120a027b2559bac86244f2711a9d82a660e2`  
		Last Modified: Fri, 27 Sep 2024 18:23:56 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:ab468a69ccb5ad52cf9e8078796e747d3cc97d7cd8ce0a6c364f9377f848f246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3893529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4da4424c37cd76a10f9999a54ecd1221913780d2c8286ec4d185dd39a4fdac`

```dockerfile
```

-	Layers:
	-	`sha256:a48a73d15e1dd1c7187496b7dec2eb7fd9d41df75fff9cd9eed93a6b538aaefb`  
		Last Modified: Fri, 27 Sep 2024 18:23:57 GMT  
		Size: 3.9 MB (3868564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:661bd3d9ac40eba7e1d6e80ede794598f8d90575cd5c2dff4a71de4dc207a6da`  
		Last Modified: Fri, 27 Sep 2024 18:23:56 GMT  
		Size: 25.0 KB (24965 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:4ac6592ed168b89c894028c35baef41a322694dd323410c3e5674fb498e41aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79783184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:137ca6ff3afbf77d593ccf12f754d7d0119ee802c751c3ddc5dce9637c8a74a4`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b94787adb8320baa3fe59801066b99684da9616d417863e36c8872528b750b5`  
		Last Modified: Fri, 27 Sep 2024 22:50:09 GMT  
		Size: 12.7 MB (12705350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0ae70a92988259064119f85dfc37f2050ebfb8f74934c72a724141eef6d242`  
		Last Modified: Fri, 27 Sep 2024 22:50:08 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e782c23f70040cba08d6cf6a137a33345cb5f1260ee56d557bdf9947fb5569`  
		Last Modified: Fri, 27 Sep 2024 23:01:34 GMT  
		Size: 37.9 MB (37921125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97adfaafd5f9f3ecd24ff6d32d544da5b5f1975c788c2d4873c9c4b6f3e623c`  
		Last Modified: Fri, 27 Sep 2024 23:01:32 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:8b8fb71ad09181ced3641b536c14746719ca29841981b4c02d7970d262fd5685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3894917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bee871a573d69955481cb3ee58428c8eb9ce8299f0d0ef7b0f19cab1a8f14b`

```dockerfile
```

-	Layers:
	-	`sha256:59ab1a0621ed49ee31410b91203d1b2482b096920a5158d61b967f06fdc71416`  
		Last Modified: Fri, 27 Sep 2024 23:01:33 GMT  
		Size: 3.9 MB (3869736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c326fb9c3bf0c6abd4e4ae64586474cc0867ef6fd7c21d85eb529e7a92a4f2c6`  
		Last Modified: Fri, 27 Sep 2024 23:01:32 GMT  
		Size: 25.2 KB (25181 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:8a628a4d2d82625258a46250870b04f3871365be215a8116604e23fdb0f30936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77542412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98459eeefa944e7b95a130a2245774dfec29d3dc5b132d09a77690355b1eaadd`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:9e1e244025374c1ce772075845b1331852635a8eb7d29e206c37cd9de6ad8617 in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:f1bcef69cca27061b771e6bb01a051f6879c730ec30ed4661fef463e7d798d9c`  
		Last Modified: Thu, 17 Oct 2024 00:42:33 GMT  
		Size: 30.1 MB (30144267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6fdfc981b3433ef764c5d57adbffc025a585b9a063341e0556c5540d48a35a`  
		Last Modified: Thu, 17 Oct 2024 01:19:26 GMT  
		Size: 13.4 MB (13417068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d90136c650417dc3ec21cc8b633306e8934fd78b28dfb35a81c5e83e8adb3e`  
		Last Modified: Thu, 17 Oct 2024 01:19:25 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f697f24e49084c1dc59723ed7803d11e4163053b60d26b4239b25049988a46`  
		Last Modified: Thu, 17 Oct 2024 01:19:26 GMT  
		Size: 34.0 MB (33980738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd9fb1857d67b698ff546a4a967e2d22d957abdfe5ae11bcd5ab2f074e1d46d`  
		Last Modified: Thu, 17 Oct 2024 01:19:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:ea621afacaf97832c9dd74479b4a39c21480eb65afc66927a9ffb2ff740a05ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6ec9ab595572ee156b49a789ec672b768efafec0f8ca80f59ac341e7b77e20`

```dockerfile
```

-	Layers:
	-	`sha256:95b0ed6717172973a3bc8abe55a99de3cc3f989a16d5740cc5a2128513a36e02`  
		Last Modified: Thu, 17 Oct 2024 01:19:25 GMT  
		Size: 3.9 MB (3892308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65407e5c6c5160b22c53bc4d807a0a579b179d0bbbe72ac884d561a7bd5b886b`  
		Last Modified: Thu, 17 Oct 2024 01:19:25 GMT  
		Size: 24.8 KB (24807 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:03a95438b35cc9d54dd8d3d11e6fe88f367b48bc736f89561ea36d27b4af7891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77357916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a264e1ced9bd7f3402f3728cec18fd24c16ee65475e05ab28546aaff772c9409`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973ca4e59b6f607fd5817ff3caff9ef37dd952fb7190d6b2d3a9c378f3bcb3e1`  
		Last Modified: Sat, 28 Sep 2024 12:04:33 GMT  
		Size: 12.9 MB (12885763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca6c1a56215eca648c2a2e92f655983629e33d37c13eb5f2b9978f85421f839`  
		Last Modified: Sat, 28 Sep 2024 12:04:31 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8c00be0c0e65d845bac0a266f35e9113f312e4b84f55e52249880053f527aa`  
		Last Modified: Sat, 28 Sep 2024 12:20:02 GMT  
		Size: 35.3 MB (35346957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3a7651b14e17d84e58e601528d7863fd16f4de13f4b499e5d3ffc24f7e27a8`  
		Last Modified: Sat, 28 Sep 2024 12:19:59 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:d06f3900711acb93794cd7f8ac4064644e1e425bdf8326b01449f7054f409298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277437e7800870978dabdcb0c008725836453c3ef136773936dda94979614def`

```dockerfile
```

-	Layers:
	-	`sha256:7041fd1d4fe8d3c39533f4e412b85de15bc936075f60123ccd313be7d7dcca44`  
		Last Modified: Sat, 28 Sep 2024 12:19:58 GMT  
		Size: 24.7 KB (24707 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:22cdf97b53b473a26c4fdfd64093a5e101ad55cf9dc487873cda493df4dc509e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83419389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff8e0bb632504df4a0e1efbc2a4c9b70e10d03a7681f9537dc48ec6b4dab229`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e944decc6c885a3cfb18414f7007b22fc8a4b77f4b16c9d881f26c07c4a59167`  
		Last Modified: Sat, 28 Sep 2024 00:51:13 GMT  
		Size: 14.6 MB (14590506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69529784e0f3b0b65d2ec424cdcd4b6997929a1e9900af7d5be09782809f4888`  
		Last Modified: Sat, 28 Sep 2024 00:51:12 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5091a0d4f1c32493c509f5747cf35d4973256ece4da921519cd1052d0c1101f`  
		Last Modified: Sat, 28 Sep 2024 00:57:39 GMT  
		Size: 35.7 MB (35706381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:951d160f32c529993e69f6106a6bcb64e297aa8c295f69e03b0f7ffdd8afccaa`  
		Last Modified: Sat, 28 Sep 2024 00:57:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:4bc47b90e03634a42c2309703a5e1fcf4e7bae5c1a39bc3d9cc7a8bad5b26599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3909186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f1958ac4f796afd0b67a5155b2b7253436c925b9e39aec6204ca7372099e7b`

```dockerfile
```

-	Layers:
	-	`sha256:af5af315fcf69112639b4863605915db5114cc1259c368a2926db77f83f6bb78`  
		Last Modified: Sat, 28 Sep 2024 00:57:38 GMT  
		Size: 3.9 MB (3884294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d70cde7325b1dd122283a399259a976d5fd9eb3be3a0a96d4dbc37fef3c7dae`  
		Last Modified: Sat, 28 Sep 2024 00:57:37 GMT  
		Size: 24.9 KB (24892 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:e7b68f4c698cf14e96929f83092886311de5f7933a5cfa115ab36c52b2ae2e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74515028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662e79a4b77a92dec61db41e57de1e8ea8e3f4c8cb3df55a3897a0004de50496`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 03 Sep 2024 11:03:18 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["bash"]
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_VERSION=3.3.5
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.5.tar.xz
# Tue, 03 Sep 2024 11:03:18 GMT
ENV RUBY_DOWNLOAD_SHA256=51aec7ea89b46125a2c9adc6f36766b65023d47952b916b1aed300ddcc042359
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Sep 2024 11:03:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Sep 2024 11:03:18 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Sep 2024 11:03:18 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f4964b44d90bb8a258c7d0da09e47f2bc08c5a6a6e0f8a115ee932af6c1846`  
		Last Modified: Fri, 27 Sep 2024 17:20:30 GMT  
		Size: 12.0 MB (12040811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e9c9b4664bd84b47f7aeb29e34ee545ddc3509c2693234ac7d0748eec301d2`  
		Last Modified: Fri, 27 Sep 2024 17:20:30 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9bf23996451d644379875131bfef8f575d51b2b6ce71cfc59b30233652c2df`  
		Last Modified: Fri, 27 Sep 2024 17:26:10 GMT  
		Size: 35.0 MB (34983854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3912bc9bccaabb454d936f8d01c6af9bc472f428e79d9432f87af11e2cadfd`  
		Last Modified: Fri, 27 Sep 2024 17:26:09 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:114fc41f0acb6b6a9fa1fc99f35609802dc04921ea0bb6ec9497b67c265ac26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3911545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b070b8397854bdbd0fec4a13a78f803ed131a2ff0f12e7f3ab7874e630540a46`

```dockerfile
```

-	Layers:
	-	`sha256:4d02e9665acd6fe9bfcb91f7ae2a388f0039776033b47d61883a8a60c8dbfbb6`  
		Last Modified: Fri, 27 Sep 2024 17:26:09 GMT  
		Size: 3.9 MB (3886721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:287af24536e5f618b7486960173243efda4516bd9823e17a72a7e4bc42292553`  
		Last Modified: Fri, 27 Sep 2024 17:26:09 GMT  
		Size: 24.8 KB (24824 bytes)  
		MIME: application/vnd.in-toto+json
