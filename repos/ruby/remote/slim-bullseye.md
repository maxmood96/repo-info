## `ruby:slim-bullseye`

```console
$ docker pull ruby@sha256:dbaac5ddaf98e68304660f5d93a678f5759eeb976708a47169d214e1d7da115b
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

### `ruby:slim-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:db652b25f25c7e8d1ffe78b29eac36a0c45efcc264eba99e6c5a58271ed78fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77676613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c3bcfd1fe6ce0c4e01502124b329ff526cd212ce23affa2bb51758b8690eb0`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["bash"]
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862cc40affcc5a1ab1435f4804bf0797f0b5b788d5313518e51fdad3e07ecafb`  
		Last Modified: Tue, 02 Jul 2024 03:30:38 GMT  
		Size: 10.0 MB (10019564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0caf832ba72fb30a722bf9f407e9c209ba2a2e3a85ab2cadcb416d793dbda118`  
		Last Modified: Tue, 02 Jul 2024 03:30:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c3ac92c312539c89e4a2ba6ab72ed16babf986a8bca09466a3b0f87d583076`  
		Last Modified: Tue, 02 Jul 2024 03:30:39 GMT  
		Size: 36.2 MB (36234423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6819bc3d2d7eaec158d1a7aa0ea296b7a8a6bee55b26adf696399e1e1ac97976`  
		Last Modified: Tue, 02 Jul 2024 03:30:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:6c5a849cd39124af6fc92ef18bd5eb1a8724b2bb41d4ea42cdb5e5d298d66725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1f0e9261c58625dc3d4df7b85848e5016ad4dcfe41e731dc684f1aebc63396`

```dockerfile
```

-	Layers:
	-	`sha256:905dc3dc12dec5fdcf24998e2701f4802675a0b15051756c1722f2657197b56f`  
		Last Modified: Tue, 02 Jul 2024 03:30:38 GMT  
		Size: 4.1 MB (4060031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f4481ace7dcc54bb92075dc47fec82b8558a5378f1f207ad0b732b8e1dcaef`  
		Last Modified: Tue, 02 Jul 2024 03:30:38 GMT  
		Size: 23.5 KB (23518 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:7876edc4923ea8bd11911aaeac564a829119d38046366e976a5f86c79f15b067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69863660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6186574014474d9ec859a405b5560609270a0cd3b62df616abf2c90a93070862`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:7b150e5fe9a4f014196e0bfb8275f3406ad543dff58b049264b54e2e00f392b5 in / 
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["bash"]
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:63678471745dce46512f823fc94716da7f08aa84c931dde61ae18c67b55c3085`  
		Last Modified: Tue, 02 Jul 2024 00:52:13 GMT  
		Size: 28.9 MB (28924714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303e9e27178d568cebf51718ed4ef0e6616173fef317fae326e9e30d90ca7341`  
		Last Modified: Tue, 02 Jul 2024 23:34:12 GMT  
		Size: 8.6 MB (8632834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fab8d45bc0a1d9eeb96cd0e784112bf7d922ab5dd76ccad11cc56cb7d03800`  
		Last Modified: Tue, 02 Jul 2024 23:34:11 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f81a329ead025e82581dac5af86eec99c43762033daf59377dc82082104462`  
		Last Modified: Tue, 02 Jul 2024 23:47:05 GMT  
		Size: 32.3 MB (32305770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2def445c53671359265ebbe558ac2e6ad417c17f1cc9f6703ee65e9cf72093cd`  
		Last Modified: Tue, 02 Jul 2024 23:47:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:3cc604b83bab22c58f8eb341f51ac6483a0983708ee271d4bffd572b8ce8aeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c8be5069b34f285a77c6ec432d121929048a887c5bb1328db8e40a47811f63`

```dockerfile
```

-	Layers:
	-	`sha256:0240c6840b30a6f37604195c861c60054bd0cf1d602c58fc59abe18857c3b90d`  
		Last Modified: Tue, 02 Jul 2024 23:47:04 GMT  
		Size: 4.0 MB (4031259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e24756c74f80b3b8c95a453ef9044eb239c90ff4cb6e2d1b21037b031864bb40`  
		Last Modified: Tue, 02 Jul 2024 23:47:04 GMT  
		Size: 23.6 KB (23624 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:7ee02d89ca8e9755e01ebceb420cb67f480e726ee22fc074434987c625be2835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66936129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b9a219177d53b81d7486f47f1cbc0e4717644bb63f9289ecabf84e54fa871c`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["bash"]
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a78c23d393ea924c668a05b9ae2c57d199028ca1a464cf7d80187614f05b7f6`  
		Last Modified: Wed, 03 Jul 2024 00:38:19 GMT  
		Size: 8.1 MB (8141146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1009a8822628f0f6d9bb49258a4da2505b2287658a487efcbac1aa91d6dedf65`  
		Last Modified: Wed, 03 Jul 2024 00:38:18 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3b47c05a1fc42bf3c02ff09f2b356529e3ee6498c8b7e53eaf86a9939af2f1`  
		Last Modified: Wed, 03 Jul 2024 00:52:04 GMT  
		Size: 32.2 MB (32211935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b13be0fc61be3d655bdd25695f88e24f8eb0769328eb98f2963b2e44b05490f`  
		Last Modified: Wed, 03 Jul 2024 00:52:03 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:ae200bcd82be614352360034a4bb9855e6181fc656d343d8d7203a878ac68601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72436d60c6fb218d6bceb7bc492da96e6e1d7ab78604a13a4a5fe2a923cedefc`

```dockerfile
```

-	Layers:
	-	`sha256:404f4f404d4a6ed024517481494b4846423040de97ee307c9fd47965cf87ce41`  
		Last Modified: Wed, 03 Jul 2024 00:52:04 GMT  
		Size: 4.0 MB (4034023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8cef0b5870c22881b56e95f1c6cb728d6c9ac73316624aed0ca781d29d53d58`  
		Last Modified: Wed, 03 Jul 2024 00:52:03 GMT  
		Size: 23.6 KB (23624 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:f9c3bb2ddb00e56517dc07398be2e8e6e76d0f9eb871f0d9748b238b123a3068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75460175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3ee0aad369196bbf908e77fc5ee0a6e3bbc1b453e4016e9adcf0144a8f19fa`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["bash"]
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfe0945ade03ff6b5653d84625b27432b9b9cb42b6d86995e3de65cf582a7dd`  
		Last Modified: Tue, 02 Jul 2024 23:17:33 GMT  
		Size: 9.2 MB (9240898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42eb876ded1c6ea91f841895858bce7eb4914405fa3969bc8f7d845dd366b11d`  
		Last Modified: Tue, 02 Jul 2024 23:17:32 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed42046708a93b7a341858a752a267750fab61175f7716e2af57f5b1fbf5e263`  
		Last Modified: Tue, 02 Jul 2024 23:28:39 GMT  
		Size: 36.1 MB (36149320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ace7ccf212d481c7286836ed4e2f7463446761a43eb43e3cbf4049ae7b485e5`  
		Last Modified: Tue, 02 Jul 2024 23:28:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:686ff1726082d2c5864f6ccfa2ea7bdadf7566d096387dc204d4daf1de95cb6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4058239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbfb3159cd8914c6f01274c68dbbf002f4d2631712f133ce19223dd1e510728`

```dockerfile
```

-	Layers:
	-	`sha256:415eec109fd1930240687a34bb47fedf4d5b2f8f1bdcd1ba29a7b8652bcdc5fe`  
		Last Modified: Tue, 02 Jul 2024 23:28:38 GMT  
		Size: 4.0 MB (4034415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dff6227a60af2de47db474e899ee7f404add2ce02ae3185da3462a5e60d3b2e5`  
		Last Modified: Tue, 02 Jul 2024 23:28:38 GMT  
		Size: 23.8 KB (23824 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:f0c80a491431fa768b533e71c8632458ce140530595e8094ea661e7ebf15172a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76690507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794bdb199f3df05e742cb5990f3ba341f6609c12393fa6997af1ea3e63ea09d9`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["bash"]
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56087391d0ade5104fed2aa9424a3ddd3282dc7e1ad08fda85d0718d4492ceb`  
		Last Modified: Tue, 02 Jul 2024 03:30:38 GMT  
		Size: 12.0 MB (11994756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c7231669981588d7eb4697f9209f488d594a22142ae73d199023718b653d88`  
		Last Modified: Tue, 02 Jul 2024 03:30:38 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b0ff124c48f25142cf4abf8a7ba7b5a0a7afb52943a06b2575c2e116baf5f0`  
		Last Modified: Tue, 02 Jul 2024 03:30:39 GMT  
		Size: 32.3 MB (32286958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6819bc3d2d7eaec158d1a7aa0ea296b7a8a6bee55b26adf696399e1e1ac97976`  
		Last Modified: Tue, 02 Jul 2024 03:30:38 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:acaa7b0faca830b22b1aa53a8cb28ee0772d4d1c3f67aa0145f468e3ec103257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19ec3120f7b2e5b1c40aad03984c19d6426e495e76275453208a40f1cd3fc5a`

```dockerfile
```

-	Layers:
	-	`sha256:dcd60e26a79a76e7d644f8d9eb7411ea46831484a4955bd2bc8f915f70ed21b1`  
		Last Modified: Tue, 02 Jul 2024 03:30:38 GMT  
		Size: 4.1 MB (4064233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375a852c2c3e1f2d0e5a72ff315d31ff0c41f671e9a564ffd1764f32b91d9ef8`  
		Last Modified: Tue, 02 Jul 2024 03:30:38 GMT  
		Size: 23.5 KB (23483 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:a1783036a93a80c0d35c41a8bef0cfb1200d68b1e80f5ae648e9dec5c73470fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73105134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cbe872e48cb4e3db74a2ea2cf3a3ccac0e980b6a14a5c7d0a3bafe618b3a53`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:791d05eca72cc81080afbb76c7f3f02a74893142203b6aada9e3170404049223 in / 
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["bash"]
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:59602b870d8ca1e13dffda9de0c5f866f86ff35c1e595ea481bb1b2c48c18b8e`  
		Last Modified: Tue, 02 Jul 2024 01:30:52 GMT  
		Size: 29.6 MB (29639850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7da5214119b7d09fd13b84a6d066a21a9a7d8ee6a07ac47506f0c8378cd3ab`  
		Last Modified: Wed, 03 Jul 2024 18:43:31 GMT  
		Size: 9.8 MB (9834354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1576bb1b267bea0d4597197e323d872af466fe3b066ae351019c199047ecb3`  
		Last Modified: Wed, 03 Jul 2024 18:43:29 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8647d8d37e9b8eeb1b73f1638c4d83a89d5544e6ef43d8b8fed7939d0278e2ec`  
		Last Modified: Wed, 03 Jul 2024 19:14:22 GMT  
		Size: 33.6 MB (33630590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b65d7031d697df798da0d8b45de7dfbae38951d803f06eeac328f78d3cc7dbb`  
		Last Modified: Wed, 03 Jul 2024 19:14:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:6bfee1653a8eb7e9288cc72b2f7e77751459bb0f1af165fa8fea1064d11b895c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144d800a2201ca825e940f62f679f1329a862e1a42badaafbc11821232a94b34`

```dockerfile
```

-	Layers:
	-	`sha256:4ac4d50da91330cd6758b8da731092d6891e214c719c65e3a7571592a2123c37`  
		Last Modified: Wed, 03 Jul 2024 19:14:18 GMT  
		Size: 23.4 KB (23361 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:d0a7dd4308dc5bb6a1ed75e95ae98b8bfb6ca4ab1b8f7adb1c571b419cd8c32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79758607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6444e302a7175e7aa0b12b38941b73a44d793e98038edb9e594c5711c25c9a4`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["bash"]
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3d2bbd27581eb1942a494baf520bf68ed3c4eeed2e77b664164d4c1e70ba3c`  
		Last Modified: Tue, 02 Jul 2024 20:29:05 GMT  
		Size: 10.5 MB (10479627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476f763ef9c30a9739d75d4c2600107a3cd8c2d3c3c7583008d03c1fd7045eb0`  
		Last Modified: Tue, 02 Jul 2024 20:29:04 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74ac5ffa017281d917461091a6df4c168968599fd8bbabde63f0f8d95b7ab57`  
		Last Modified: Tue, 02 Jul 2024 20:41:43 GMT  
		Size: 34.0 MB (33979450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82a02bd6aec886d1b065c4525a2ee7bbd7c2b772df7c7b4f8b7e9c8f4a0042b`  
		Last Modified: Tue, 02 Jul 2024 20:41:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:04380180544415e62ea092c9c6c10e89ad4c07f7b193c453b4982153999cbd5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4072486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b653af178bca3ad7218ac4bdee08754ef19c0484b3af5f2117d2f56458f272`

```dockerfile
```

-	Layers:
	-	`sha256:7d027199906f2370c3c431be2aec8b1f7eca7f3d39eaa71a95f5e37367502ef7`  
		Last Modified: Tue, 02 Jul 2024 20:41:43 GMT  
		Size: 4.0 MB (4048923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d225b9708a4843b7dee593c52861374e4a63689f10e20793a4489b1e873b2b24`  
		Last Modified: Tue, 02 Jul 2024 20:41:42 GMT  
		Size: 23.6 KB (23563 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:c395bf05df66cc0e0515493b72fa572822bfbad730bcbcfaef4ceace76d68f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72093677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bcbc0186acd29e60e8478a7166cdb568a7216dc1ec0c99ff3e5826406b107f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Wed, 12 Jun 2024 05:03:19 GMT
CMD ["bash"]
# Wed, 12 Jun 2024 05:03:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8285b210ae9849c2c26d40ca702e259845918aad06a005fa257cdd6a3477f9`  
		Last Modified: Tue, 02 Jul 2024 10:36:47 GMT  
		Size: 8.9 MB (8860891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff2f6484101a040e02881d6c1ee03b7b440f5d8e8b93b2eefc1408a5912ef75`  
		Last Modified: Tue, 02 Jul 2024 10:36:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7d718803a7699627fa7f2f0aa7af206691a92f166e46200e7cf97d2860655c`  
		Last Modified: Tue, 02 Jul 2024 10:42:11 GMT  
		Size: 33.6 MB (33570094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c62e91c9cc2427569f49636fc4ca1311e570475f2ddd1e033eef9436fca8a0`  
		Last Modified: Tue, 02 Jul 2024 10:42:10 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:f79885b4d62cd01227221de946b470b94d0f5864fba2ce773c5a3cac241a093d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4072225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc9f532612501f8004158683257c369564faf0245116d7ef7424902a61170e1`

```dockerfile
```

-	Layers:
	-	`sha256:7dd7c4631459dfcc25ccb1072cf468fbae4e99a7c76fe83f856c6c7448455691`  
		Last Modified: Tue, 02 Jul 2024 10:42:10 GMT  
		Size: 4.0 MB (4048710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb384727672474ecb1335e4cb4295cbb03ecae0caacc87785108a3178c1e9db`  
		Last Modified: Tue, 02 Jul 2024 10:42:10 GMT  
		Size: 23.5 KB (23515 bytes)  
		MIME: application/vnd.in-toto+json
