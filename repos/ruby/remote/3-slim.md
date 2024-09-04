## `ruby:3-slim`

```console
$ docker pull ruby@sha256:46493509128b8592c7f52504e9ab545327ccea855ca6e2531e7dea4a40b26cf0
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

### `ruby:3-slim` - linux; amd64

```console
$ docker pull ruby@sha256:eb8d57272af4153997e3448998034983e7fed33423ac4a47544519c4c093f5f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86637762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b5d85a680baa60fe650922d3bb7c28d7b3c77607098fec7bfba0a390ab79c3`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:20 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Tue, 13 Aug 2024 00:20:20 GMT
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
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109c9c81e69241c2d69b1017b5158be0c9961ba5a02c2677129e8a296e37b465`  
		Last Modified: Wed, 04 Sep 2024 18:01:41 GMT  
		Size: 19.7 MB (19660250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972dbfa9faa82c33cec01857157f656aea488df8388a369ec58da0e3ecc08bc8`  
		Last Modified: Wed, 04 Sep 2024 18:01:32 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4ec5f21b669b696a7e22d1ae3fd38a6c56ee5ee5c3a948cda4a7a49696f0db`  
		Last Modified: Wed, 04 Sep 2024 18:01:41 GMT  
		Size: 37.9 MB (37850937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8657d8b18b620783963a8c5c8e2f130d9a4f1ad34e82b7ca506f83fac22d07`  
		Last Modified: Wed, 04 Sep 2024 18:01:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:67fb8326f43b237990b01aa60db637a1b08a0c443e727e91ab59214048b0d2ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466e8a09cb29abe1f8da50f48c76335f0b103e4bde73aac6c56baef8e2d764d5`

```dockerfile
```

-	Layers:
	-	`sha256:9d44fe16b8293fb07f722a279d01e128de308027303a39b7d7e496c43a140105`  
		Last Modified: Wed, 04 Sep 2024 18:01:40 GMT  
		Size: 3.9 MB (3898457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1241c2b37ebcd6715905a2164a4569df5bd8c9a052f30043bbd4d95d4999fe3f`  
		Last Modified: Wed, 04 Sep 2024 18:01:40 GMT  
		Size: 24.8 KB (24824 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm variant v5

```console
$ docker pull ruby@sha256:91c4663bbc22421c8c623e3e3447e357cceaa7e44189d97d7d190e401f9087f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72695367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4039922757ecf025596c8afe0df43723d79e7faad1bdefd854e033b1ae27f5c`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:29 GMT
ADD file:0a38a76ef88f0bc858f9663f2ec636121970b50fcd7a62192be7a7eba71bd6b4 in / 
# Tue, 13 Aug 2024 00:55:30 GMT
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
	-	`sha256:1bc90b37f777aded897944b0ce596c103432c1b84f7b626b9fd4a53356f006da`  
		Last Modified: Tue, 13 Aug 2024 00:58:27 GMT  
		Size: 26.9 MB (26887303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b960e7fcbdf0fe6a8f21767c9ff06d14602e6fb7ef0c1b9ebafc337877422d4`  
		Last Modified: Tue, 13 Aug 2024 22:26:01 GMT  
		Size: 11.6 MB (11616583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5ccd2a6f24fcfec3b462bf2c1a1bc99d30be0fbfc225e5d0541564cf3141e5`  
		Last Modified: Tue, 13 Aug 2024 22:26:00 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f382b56d1da535243e63e7bf2a979b1b8f5456d96302d29120dced44b853d3d`  
		Last Modified: Wed, 04 Sep 2024 18:08:09 GMT  
		Size: 34.2 MB (34191139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da926c2834534231518ea8856167b2eca56ece1ee8ffa0975c5af94efb5daa`  
		Last Modified: Wed, 04 Sep 2024 18:08:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:dceb7686e784299cb63ec104641c45f091290d0e5213edc35583f807d48c4a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3893859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685c5b36dee18acf5aa599a3db4308f4984185dbd398e9037cf99a73065251f2`

```dockerfile
```

-	Layers:
	-	`sha256:77d551098c6a26681a8160f8f567472f82deaf9e080cc508b9ffd8c6818d6597`  
		Last Modified: Wed, 04 Sep 2024 18:08:08 GMT  
		Size: 3.9 MB (3868894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e185b011910169dbd532a4167b71fdb9b21878666aa6a43592a031712e3d1f82`  
		Last Modified: Wed, 04 Sep 2024 18:08:07 GMT  
		Size: 25.0 KB (24965 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm variant v7

```console
$ docker pull ruby@sha256:96dfe319f4de51b886029feaebeb4ed80fbbfcf34add58f23a2f46b5e4f8a593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69736214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b624ffca205e1c4693a538886612b31f356cd22f26103cb5379f464a0d09fbb`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:36 GMT
ADD file:452463dee9ffb3b2caafcf6c3f48a08dc239b49a5caf21d3da0d28de4df4fd38 in / 
# Tue, 13 Aug 2024 00:57:36 GMT
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
	-	`sha256:cf43e4280314547b69ae6040ab5c16458259478e27c46528b9d7898d69f26d84`  
		Last Modified: Tue, 13 Aug 2024 01:00:55 GMT  
		Size: 24.7 MB (24718142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd3673264628d68026a5c0114f0622395677b4901726ce493fc623dd29bacbf`  
		Last Modified: Tue, 13 Aug 2024 23:30:15 GMT  
		Size: 11.0 MB (10952449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53686910b94bce05337ffb25a090902de9667a3388330d35300a208c6d8c5477`  
		Last Modified: Tue, 13 Aug 2024 23:30:14 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefb7b6b557dc885d4d6d6ead63c0ba751b2c42968e3691f8b9ea015f938cd76`  
		Last Modified: Wed, 04 Sep 2024 18:10:18 GMT  
		Size: 34.1 MB (34065283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd49ece3c02f2b7e80566e354a33180de2234db79efb77c18076101ddc6106c`  
		Last Modified: Wed, 04 Sep 2024 18:10:17 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:d1aa1f7e5855efa1157bc9c35ff05eb8d384cda33e282262d296406ee1cb6a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3893512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a145c4edc676e24a8c1b0dd4205fc12758223dd38fe0afb41b1680d83e6f0a8a`

```dockerfile
```

-	Layers:
	-	`sha256:824edf6b0ab5a88114d17b1154e655089fa109f93a84c0e48bc262a61765cb60`  
		Last Modified: Wed, 04 Sep 2024 18:10:17 GMT  
		Size: 3.9 MB (3868547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe67db253e289e7c53def1467201d4bfc4260bf31fe0ae471372719e8823c88`  
		Last Modified: Wed, 04 Sep 2024 18:10:17 GMT  
		Size: 25.0 KB (24965 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:51dc2a0a35ec440ce63b602b90e77980a409fff68e5a228a65ce4c0046df844e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85546778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35e23f8411a68960a43068b2179b69bf2eddc2f17fbcd8ee1bb8058c83dad520`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:51 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Tue, 13 Aug 2024 00:39:51 GMT
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
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ab775a3ea3b847d7315088021c5aa72eb936abd7b2b019ddae7689208dcc61`  
		Last Modified: Wed, 04 Sep 2024 18:06:24 GMT  
		Size: 18.5 MB (18468992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e857c378d2448889690d9f11bfb62348b505625df774457df6dac410437e366`  
		Last Modified: Wed, 04 Sep 2024 18:06:23 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0676cc5af7af6b4b81d43bfdebcb28d6a48cd022cec8e0d74a0b364afd227e6`  
		Last Modified: Wed, 04 Sep 2024 18:06:25 GMT  
		Size: 37.9 MB (37920917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ccc8fbcb0e059b9099ef3e5b09b33bde08e1de7faea0bf34632848724f35e28`  
		Last Modified: Wed, 04 Sep 2024 18:06:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:f0e01bd91b3fa2e27d5829f8db3861ec1464e8679f5066f0eb273eb23dbd5332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3894904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5b29fa3433f24f47371fe0e70490f11906af402fe1dbc7830bc588a8e3795b`

```dockerfile
```

-	Layers:
	-	`sha256:e5a1d23bfdc88c295103567fb690e4ee4180f8acfefc61d82d8e1d03d5b3b7de`  
		Last Modified: Wed, 04 Sep 2024 18:06:24 GMT  
		Size: 3.9 MB (3869723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07344dd4413a6d0090728dca504289de303a6120aad80200a876c8f01e0c0d05`  
		Last Modified: Wed, 04 Sep 2024 18:06:23 GMT  
		Size: 25.2 KB (25181 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; 386

```console
$ docker pull ruby@sha256:a65b73aa71c47c61f51415d4d389ead8c397c412e208f450b9c61dcd11a26021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82924190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:422c9bcbbb5c9fed34d0832eb0ad4ab1bd9e1acf90051155b75dea97342dd1e9`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:38:56 GMT
ADD file:6c928b979f82a9dc0b3801b97a516aaa3d17fe57cb9eecc077d202afda56d2fb in / 
# Tue, 13 Aug 2024 00:38:56 GMT
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
	-	`sha256:82c8eed510ac33a6df3a546a738b1f3806df7958ea977484d0f77eabe177108d`  
		Last Modified: Tue, 13 Aug 2024 00:42:35 GMT  
		Size: 30.1 MB (30144281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45428616c0c4b4e1c3aa2cbe8f18a3341655d753d08bed3bbc3c28516609fff`  
		Last Modified: Wed, 04 Sep 2024 18:01:36 GMT  
		Size: 18.8 MB (18798585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cdf4aa1fa8ea682adbbc50b4594718abf069eeb9e5be01deda32b8b14fbff8`  
		Last Modified: Wed, 04 Sep 2024 18:01:35 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8db08aec3b5129551260875564d3b7a5a582c933ce44ea8dd4b9c42e290d04`  
		Last Modified: Wed, 04 Sep 2024 18:01:36 GMT  
		Size: 34.0 MB (33980979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5794958b7ced2db19a64357503b0d68aec6cc08bd7859e884e1dad405558d479`  
		Last Modified: Wed, 04 Sep 2024 18:01:35 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:cb6ae81e24f295800fbeeffb6f15be0a9e910f431e0c7c229d25fd04a039450c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3917064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3962bd04abc3e0b438c4b99f7549afe313f8421646878e7f37beb01149ddd86d`

```dockerfile
```

-	Layers:
	-	`sha256:7bb1022082234857930a54af8826cbb762e833cf2fd869145ac8e8f302beaea7`  
		Last Modified: Wed, 04 Sep 2024 18:01:35 GMT  
		Size: 3.9 MB (3892295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6cf005cbf1229f89dd2f77176e3eb5da007bebc2fa9501915c736f8432d8ab`  
		Last Modified: Wed, 04 Sep 2024 18:01:36 GMT  
		Size: 24.8 KB (24769 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; mips64le

```console
$ docker pull ruby@sha256:6fd986f9720368412d595668a9c519cd91188db1951bdb87e7fcc833619cfcfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77349266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69291c7941c15cf1e50aa7a775bd58fe6f18b72bdbf2321f17dc347c2182705`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:09 GMT
ADD file:2fad80cfc89f7b624d81eb445f9c64e4cd3f190b85d89f40c33eb7e4bc562c6d in / 
# Tue, 13 Aug 2024 00:11:14 GMT
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
	-	`sha256:e8ebfef8c6b7f6250b54eec0d5d1ae5d66f60f418704f4094cb9291dc214be0f`  
		Last Modified: Tue, 13 Aug 2024 00:22:29 GMT  
		Size: 29.1 MB (29124941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29f82a4f2bd0516b307bf6bd851118bce8d79c93b70d071579584e54643c03f`  
		Last Modified: Wed, 14 Aug 2024 18:40:43 GMT  
		Size: 12.9 MB (12877318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847dd58447ca517adac4c901b301759bb9a3f4ca479627ab43194ec15f54411a`  
		Last Modified: Wed, 14 Aug 2024 18:40:41 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c71450a35771750e3d7160963acd73ad344ecdbcbfb84f551e3821e40f1dff`  
		Last Modified: Wed, 04 Sep 2024 18:37:25 GMT  
		Size: 35.3 MB (35346665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefe47ecf305cf0f5e1e3771b05fbd29bc5481298a574329324e64f27ab36707`  
		Last Modified: Wed, 04 Sep 2024 18:37:21 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:492964595e288644b6adfd5da8777287ea979eb062beabb80bad39fa6b867ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 KB (24707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9b29221c66ef3c5194fa345c633e3bfe50bca52bfb25cf5f23373f10ba5efa`

```dockerfile
```

-	Layers:
	-	`sha256:1bf18a82f17164a09dabebf320346c63570e3cd27a40b4deb90338a9cc36858d`  
		Last Modified: Wed, 04 Sep 2024 18:37:21 GMT  
		Size: 24.7 KB (24707 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; ppc64le

```console
$ docker pull ruby@sha256:bf9f30146eaaab19ab87a50c62e0c9c3ab4a5a5171d56147259cc47e64acd71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90059656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:527676759bb978e538888919eb0ccfd0b668d9cb1b0b64e57b9af5cec3810c6f`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:03 GMT
ADD file:2fb9d7e332d1c4cadd8151a8485091fce600b230987f3b306d19efc82ed0ac9c in / 
# Tue, 13 Aug 2024 00:22:05 GMT
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
	-	`sha256:36f5dfff311b1880d6202ab548fb824c9591bd1c9a04f7ab677235edddf9ab23`  
		Last Modified: Tue, 13 Aug 2024 00:26:22 GMT  
		Size: 33.1 MB (33122300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f51417af2e718ad1e0d09984d95d8b77353f507393827d24a145817649a30f`  
		Last Modified: Wed, 04 Sep 2024 18:11:21 GMT  
		Size: 21.2 MB (21230536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd67867d1da1c240a241b7101edc74eabf356fa4b34255b1b9b7bb2115a139c`  
		Last Modified: Wed, 04 Sep 2024 18:11:20 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa415179f4dfef75948b2a05b91a9158dd9587998587f5f72ac6f68ccd2cfdb`  
		Last Modified: Wed, 04 Sep 2024 18:11:22 GMT  
		Size: 35.7 MB (35706478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412e8ed82f27102a4e8127e1268d3e31387c6d2337ac2d4c6e3e6f23b18aad59`  
		Last Modified: Wed, 04 Sep 2024 18:11:20 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:145ea8a97e192f3aa3b605b9d2eb6ce9eaef44f215dd2f5f3ed4b1526b429e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3909173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216debd2541635d855d57533cebe9c9a973d900b96d3dfce8e8c157e4b678999`

```dockerfile
```

-	Layers:
	-	`sha256:ef08192539747bf4d3c42be84235684feb9dcce972aa6b4fcc08bc94af07ff54`  
		Last Modified: Wed, 04 Sep 2024 18:11:21 GMT  
		Size: 3.9 MB (3884281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ceef1fb63421248eea2c5fcc4ca9e2ff208095ebc702b7395bf6df3596ab487`  
		Last Modified: Wed, 04 Sep 2024 18:11:20 GMT  
		Size: 24.9 KB (24892 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim` - linux; s390x

```console
$ docker pull ruby@sha256:d02cfca784fafd20017987aa658bb2d19e6d285cd8a84f50211e24fd5b246139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79371849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441b2e780fa0f0b65639b1115378c7d7221b88d7e3e3fe134e2d646a859c8bfd`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:39 GMT
ADD file:2e68e80c30908adf6b4b6a8ea2cb0711c5b296a8ba63e2cff3b70422a4daaf97 in / 
# Tue, 13 Aug 2024 00:42:40 GMT
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
	-	`sha256:218a263fc97fdfaefe7df9b0e23e00c5a0b71a094fd212f91621d5683c6e3514`  
		Last Modified: Tue, 13 Aug 2024 00:47:29 GMT  
		Size: 27.5 MB (27490097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8029a4e0b17250dcecb5db35569bb06d295d948ec6aa0fc5926ef0d9ca420f95`  
		Last Modified: Wed, 04 Sep 2024 18:12:17 GMT  
		Size: 16.9 MB (16897713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6819b521a504367e7de6375138433f420d96c1ffa314f60d6d5c798499747775`  
		Last Modified: Wed, 04 Sep 2024 18:12:17 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f6f58a297f4ccf66de47e7a081cdeb10df2225e8ea78a3905cde0c6bf44f0`  
		Last Modified: Wed, 04 Sep 2024 18:12:18 GMT  
		Size: 35.0 MB (34983696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ad7422d53a498055efb2d48224c3bbf751e65e31c820a24c487426531a3662`  
		Last Modified: Wed, 04 Sep 2024 18:12:17 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim` - unknown; unknown

```console
$ docker pull ruby@sha256:3b398849a6c1833cdd37e639d51cccfe33a40244d0fe563e53908adc6aa2acf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3911532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1836e0f265c556e530e6eee37204f9310930476ecb2d14dd4d067c8a2835f7d8`

```dockerfile
```

-	Layers:
	-	`sha256:b251bcf898adf04077f26e6fb681743b986c094489c9dda0e4d380b9e943344f`  
		Last Modified: Wed, 04 Sep 2024 18:12:17 GMT  
		Size: 3.9 MB (3886708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11dc57bfe564a5cdad425788ada565e1443abf978b47b73bdafeb44c58ec703`  
		Last Modified: Wed, 04 Sep 2024 18:12:17 GMT  
		Size: 24.8 KB (24824 bytes)  
		MIME: application/vnd.in-toto+json
