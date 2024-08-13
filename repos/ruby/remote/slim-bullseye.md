## `ruby:slim-bullseye`

```console
$ docker pull ruby@sha256:2caa8e956261b24ad02aff1149fa4a0706751360c272d9b3669edd7ba9f75bb5
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
$ docker pull ruby@sha256:12e0413a81e233010552c50aef0c08272082d29bf6d156392152f3dd68a46450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79147801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db431767a3f10e8f066b3f9a25a45b006e5f15e66b5754018a98436a4409272`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bc3f8153c3197485f14bcfcebaf497c17f98fb9011ed7cff1d2c3e4efde4c8`  
		Last Modified: Tue, 13 Aug 2024 01:16:59 GMT  
		Size: 10.0 MB (10019000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e2562ec60c1267327ddfcfce19314ea421e8a031ac825bdea21a76c3057ad0`  
		Last Modified: Tue, 13 Aug 2024 01:16:58 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6fa7096f33da5dee9e1c14063c616ea17aa6136b07179ee5fe0922afe68c941`  
		Last Modified: Tue, 13 Aug 2024 01:17:00 GMT  
		Size: 37.7 MB (37700175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4eb4f73bcf0a1ee666308528270dd640d9c34d56a866f9d63ca8bb8146209e7`  
		Last Modified: Tue, 13 Aug 2024 01:16:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:6ef3b26452ea3da74deb1508dd898ad92b3d8a055a91590594faeb5e020f4f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79b7aecf17ae14a69727b668a5b9a460b952d8e6189d02375df938e2383fa14`

```dockerfile
```

-	Layers:
	-	`sha256:1bbcc28b0cd857dd0fa6af233ba18c3296fbac224d340d91f851354194a50789`  
		Last Modified: Tue, 13 Aug 2024 01:16:58 GMT  
		Size: 4.1 MB (4094652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc3894d86ef4f220bc39b39fd5f07bbae56fc3165c8fe9f7c4171fa8bf6f022`  
		Last Modified: Tue, 13 Aug 2024 01:16:58 GMT  
		Size: 23.6 KB (23643 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:27fcc470c59c20184c98aa50d7732cf6ff05c9ee9b1b91b8ccdb0058be22e51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71236770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df24fe693c851a01cb10360914d1c708d2edd8604b2e9218a516d09910f2ebd`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:56b9d2d0e0360f64ade3cbe073b446e10c8e6bd253b761c16b5f319a8103d181 in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:5b04226d50f1c00a6c8950192ad70a2038016868ab6ffb162ad447e35e67a3cb`  
		Last Modified: Tue, 23 Jul 2024 00:02:06 GMT  
		Size: 28.9 MB (28930588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5f59786ba63eb00c04e911b0991da04bdef531286555a77f7f3361ea460015`  
		Last Modified: Tue, 23 Jul 2024 16:05:26 GMT  
		Size: 8.6 MB (8632281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be595030c4fc8ffdca7bda7f661063c550c76e7bf262987af9369d44cb8ae1ca`  
		Last Modified: Tue, 23 Jul 2024 16:05:25 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c31a07dc8cd54b6afd1a902c1d8b2a381bab3f1f97c8d371c6dd7e366b61cb6`  
		Last Modified: Tue, 23 Jul 2024 16:11:13 GMT  
		Size: 33.7 MB (33673559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ff0c640f480a012c4b285f5c2ef2ceea22fc5ff2b147f5fa4d0d2c8ddc53e2`  
		Last Modified: Tue, 23 Jul 2024 16:11:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:832e950ff13ea84f545ec90b1c38ad3c744a9660a7a9d939f5357c401f4bce63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4089629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36195ff87e0e7af1842fb861e66c47abaf65a95dd020f9a98b3fc6a50b5d8c4f`

```dockerfile
```

-	Layers:
	-	`sha256:f253c02900d2b0e5ca690fbe21a17e41260b114b5408b86a8dcfe5a2f4db93b6`  
		Last Modified: Tue, 23 Jul 2024 16:11:12 GMT  
		Size: 4.1 MB (4065880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e8da8c49871e1680673f06a1080356379e25fa479bb113bdc5b39690e48aaf`  
		Last Modified: Tue, 23 Jul 2024 16:11:11 GMT  
		Size: 23.7 KB (23749 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:19ac4079f2afd6179a2cdf69091bd1d3fc5f1afe7b870a091e32567f49a39b6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68313722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9508a884884177af3315989a728480f5a707d92d29590a9e354d97bb9e3ed824`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43114de5f8b8d5545f9061c9e899d4fe5f0cbf8fc4690b870705f85a6777eb3`  
		Last Modified: Wed, 24 Jul 2024 13:36:36 GMT  
		Size: 8.1 MB (8140522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b67caca18357d7cff7fb963e06c28765f50b59f287584f3c3d9da660b88350a`  
		Last Modified: Wed, 24 Jul 2024 13:36:35 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab50714be5a6fbe9666c82067c3b3c41dcf98cf7da9bf2bb06699178ead4bfe6`  
		Last Modified: Wed, 24 Jul 2024 13:53:16 GMT  
		Size: 33.6 MB (33583728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6060f1cdc283869235edb5d595901213b505a818586baf34405f76dcb93482a8`  
		Last Modified: Wed, 24 Jul 2024 13:53:15 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:41d06c88436d9d0c7b2a5174cb2a83ee91e3c51c49a9cc9ae58b6616b115b56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c04059ae87137bea2ffec97bf3753c900c968a6dffbae8cd146b1c7a849cae9`

```dockerfile
```

-	Layers:
	-	`sha256:f65df3b46b071adcb5311fea6131d2ce80c7ff08b5cd74a2e408c7fe84eff375`  
		Last Modified: Wed, 24 Jul 2024 13:53:15 GMT  
		Size: 4.1 MB (4068644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46ae9326e59876d1840a676f7f7c05a4db514f7325bf7af2fe369d8d5d3a8806`  
		Last Modified: Wed, 24 Jul 2024 13:53:15 GMT  
		Size: 23.7 KB (23749 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:b36eedd4830836822daacbd7bfb3bdc4e115962f29f36d9b6aee2dcd33db7f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76940630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a53a415237a6e296ff29f687ce2ad8a9a15acde645cb93080f121e442f3a7a`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65095a76595c098f51a1451e2c982d1c0e0750c252a19da132bddf26deac5c05`  
		Last Modified: Tue, 13 Aug 2024 11:29:39 GMT  
		Size: 9.2 MB (9240144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fa682d908cf54d2eae96bc4d249122a14ab22a24cc0c26ce4ab9909627c947`  
		Last Modified: Tue, 13 Aug 2024 11:29:38 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209663c4667b255a91c0b9da811fb3ac81f770a22df9ea772031a1196699bd0a`  
		Last Modified: Tue, 13 Aug 2024 11:35:12 GMT  
		Size: 37.6 MB (37624058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84302206cfb426a520983b76e6ba6561143b73979dae460caa7b2d455ebe2988`  
		Last Modified: Tue, 13 Aug 2024 11:35:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:fe926b67723a9a6c5085f259368dde44c23cb207950542c385b80707826891b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca2977558eb7e2e3a80c718f4e1499c51ec7b189b186f96a2e7407e1f49b329`

```dockerfile
```

-	Layers:
	-	`sha256:5d5ddfdefe5d40176b97a013022317e51bc05f03286449d4868a4d87f939ca35`  
		Last Modified: Tue, 13 Aug 2024 11:35:11 GMT  
		Size: 4.1 MB (4069036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11173eb20de1bd4bf9b399decfd1cffc77b88ac5a30acc91df1d3578bab4f67e`  
		Last Modified: Tue, 13 Aug 2024 11:35:10 GMT  
		Size: 23.9 KB (23949 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:dc0ae533c8b5fd2572e10031b85a30dda69f07ee6de84d8357fa2a065f450aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78052364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48eb06a4ebce6ebc9879f33a28b5126509fefe9c7d716b5c4f486823edeb39bf`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf516d52feb8b4ed9f351fed707750e3c84b55559a9bb3dfb58a81af173c74c9`  
		Last Modified: Tue, 13 Aug 2024 01:16:41 GMT  
		Size: 12.0 MB (11993708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165281ce4e5ca148365e1e6fa11083441add245495dadcd2542f3cf702ea9733`  
		Last Modified: Tue, 13 Aug 2024 01:16:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa25cd6e7675dc5fa004d9be9545616ceea92abb8d4056de1a7e0ff7adc896b3`  
		Last Modified: Tue, 13 Aug 2024 01:16:42 GMT  
		Size: 33.6 MB (33644531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5921ea3632274ca83042d389fe7413b1547a97966fdc284634a9ec3c2fde7844`  
		Last Modified: Tue, 13 Aug 2024 01:16:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:9fa64bd0fd83f6a27e14cdfed936eddc2ef5232be757d413ad629d43c1596971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011a62bdb677d50b5a9b512a680ca8e429f63869ac2f880a089ec7600e6b483d`

```dockerfile
```

-	Layers:
	-	`sha256:9d206644da9c3e099c862f87766fdd65d7f03d89339a09659a4957837b857dbb`  
		Last Modified: Tue, 13 Aug 2024 01:16:41 GMT  
		Size: 4.1 MB (4098854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eddae94bea785af940fc202b3c7683bbfb830e82fb6cf73856f9de83367ccaf5`  
		Last Modified: Tue, 13 Aug 2024 01:16:40 GMT  
		Size: 23.6 KB (23608 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:3baf4f41a47bcae341aae02469a972de932ada2872c599bab9c8a52684d979cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74621430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9271b7c81fbbb0240d99d23b13eab92a3eaa252d6b51692fcbabd73dc8b41159`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:aa937b31fe693810c8c6e110de59ba07264dbc020fabac9e1ac045df57efc0c3 in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:83b27ea307774a387b0a5203cb6aa8f117e44bb5321ed6c8de8b0a0c43d895ca`  
		Last Modified: Tue, 23 Jul 2024 00:50:32 GMT  
		Size: 29.6 MB (29646085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68440e17bdf0c7b0bfe48fbcf3e9b91a82783ec497547af5d341ae128849c008`  
		Last Modified: Thu, 25 Jul 2024 11:34:18 GMT  
		Size: 9.8 MB (9833632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719274c17126c40734e72c39c6d6ae46af7835faa4cfa1e6823443c340ac7670`  
		Last Modified: Thu, 25 Jul 2024 11:34:16 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e99d1f32c8e2b9bf421fdaf64cbd99913bbad0eee6f60706065ba0cb681b1dd`  
		Last Modified: Thu, 25 Jul 2024 12:30:51 GMT  
		Size: 35.1 MB (35141370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c39152dd8eaa6e096b6b447faab980079afe7d020cf8c57eb0ea72706778d4`  
		Last Modified: Thu, 25 Jul 2024 12:30:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:8d5a001f1ffa8761786811a098b5abf12fc4851cf494328f7ea67da5cb26c012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 KB (23486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebc866c19628d028ec26576ee56b4bf1c69d18981325b2c224d7adc619dce84`

```dockerfile
```

-	Layers:
	-	`sha256:dfa1f57b2fbfe672fd38cc05265a4a119738edb0162c01eb30c6e4edad3eb122`  
		Last Modified: Thu, 25 Jul 2024 12:30:48 GMT  
		Size: 23.5 KB (23486 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:af689228f49180b857d2c468dc520bb9512b4314a199f0bab1325c4c0f3e85b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81247789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051c92483aa5cd32003816e80e137c39fda0d7d262813f9570e7ebee2a2b5057`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d057b2c883aa3a33aa2a62665c02cea10c37d6c57295e3d23da6d27c85ac024`  
		Last Modified: Tue, 13 Aug 2024 12:22:06 GMT  
		Size: 10.5 MB (10479764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c597a73d5ffa72d425f5f11f7dc5d650a7acc74d0bbd7e75c2b3bed2408ace3a`  
		Last Modified: Tue, 13 Aug 2024 12:22:05 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ee54b2d13498c32c9727be0c76266b60b332f5a83360e70b1e5f206343fdeb`  
		Last Modified: Tue, 13 Aug 2024 12:29:07 GMT  
		Size: 35.5 MB (35462551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f58059918bb04f4b59b37318aa95d87091de4d0db38dd9425f53f1a0332536`  
		Last Modified: Tue, 13 Aug 2024 12:29:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:3d7ec79e48eec5ba046dd964468000066dbd80f13cdf9bb2df6590d3b067c2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4107232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bc11dc4900cbca5042fd8f4d8702625b3261f7a115f690d73f7a9060bf9dc5`

```dockerfile
```

-	Layers:
	-	`sha256:2a8629621b2ea43ab4633ccd0cd15d54781dc2c701bfacae5eed876d0435911c`  
		Last Modified: Tue, 13 Aug 2024 12:29:06 GMT  
		Size: 4.1 MB (4083544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb430b4b84bacb3937861f183f6dbf7004e1e76903eec38dc034bdfde9607ad1`  
		Last Modified: Tue, 13 Aug 2024 12:29:06 GMT  
		Size: 23.7 KB (23688 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:c7c2d8779b42db73ffeaa560e0ac7bbfdfc658870f476e6193615e670cd189da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73597077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22bda841ba7a4b8dc844f2d88b63e33537b11da03e312dcab4c614a4254f20c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 09 Jul 2024 05:04:38 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	{ 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_VERSION=3.3.4
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.3/ruby-3.3.4.tar.xz
# Tue, 09 Jul 2024 05:04:38 GMT
ENV RUBY_DOWNLOAD_SHA256=1caaee9a5a6befef54bab67da68ace8d985e4fb59cd17ce23c28d9ab04f4ddad
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Jul 2024 05:04:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jul 2024 05:04:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Jul 2024 05:04:38 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0182c224c41f8d32f3c8e2da1d120c2f02910a40d0471f4eea9addc19e776cfe`  
		Last Modified: Tue, 13 Aug 2024 09:50:53 GMT  
		Size: 8.9 MB (8860394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1802f9bede91c22c8c46b8d03a0777748f8d16c9287c60e50b789ebb3f7e26e9`  
		Last Modified: Tue, 13 Aug 2024 09:50:52 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c85045582662342ec90cc6ffe4be4acb31746e028cac54713df7c75fc673c04`  
		Last Modified: Tue, 13 Aug 2024 09:56:45 GMT  
		Size: 35.1 MB (35067377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b185343bc1442808f15cf1ebd7ce2be4b55e0c954940eb013ada1b8e39b9b2c`  
		Last Modified: Tue, 13 Aug 2024 09:56:44 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:5f0d6ed02ba866f09988afa378df54b953ee7a35174240dacda2530613867a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4106970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e72500589488f7320795436acac2a799550ff16b0795e234ea56067ba747970`

```dockerfile
```

-	Layers:
	-	`sha256:6fc08378f52ab2b6cbed075535c47b70abdcbd6fdbabfff6b56567b05cb0a278`  
		Last Modified: Tue, 13 Aug 2024 09:56:45 GMT  
		Size: 4.1 MB (4083331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f008fcd70390c55a6a55217ea8ca29f1b098862d585738fa3569ea32f5196b`  
		Last Modified: Tue, 13 Aug 2024 09:56:44 GMT  
		Size: 23.6 KB (23639 bytes)  
		MIME: application/vnd.in-toto+json
