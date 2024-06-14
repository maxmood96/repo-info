## `ruby:slim-bullseye`

```console
$ docker pull ruby@sha256:7fea6dff19e10bc990f12cb55c8f6de484bee54515b6a6565cf833deca2546e7
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
$ docker pull ruby@sha256:d886b1cc9182a53f9c975c77d34e6a57d880ee5dd6a580ba053f04820109edad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77484495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfe2b17afb56246d837b2e5d8a6a29e435ae14681e3cd38d62c46d87f435608`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
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
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1fbcca8efe02e382b170c087dbd8fd555412cea0ede6b7e06f6470bb843187`  
		Last Modified: Thu, 13 Jun 2024 18:37:12 GMT  
		Size: 9.8 MB (9815815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00f71ed4a269384524c785154f45b9ce16c18e4d93aad466e778f0cb736100a`  
		Last Modified: Thu, 13 Jun 2024 18:37:11 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf2109f375de2b7f00410da07a53e1942e1abfdf57fd7abf79d7220684c83d99`  
		Last Modified: Thu, 13 Jun 2024 18:37:12 GMT  
		Size: 36.2 MB (36234298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930c3bf0f1e8522a84838fe2f75a93e49503f97ad6920505ef9ea10d7745575b`  
		Last Modified: Thu, 13 Jun 2024 18:37:11 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:506f1abaea7aa59d977d769fa53830dbfb1f426841d1998ea8682b54c0f77f3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fdcb083003205dbe6d6646428324245fa7a1f278afd68da21b36a502485185`

```dockerfile
```

-	Layers:
	-	`sha256:d7d3f0114199c8522d5b1d48f358f28fd222e980cb6af5184a3a2b6db02088f8`  
		Last Modified: Thu, 13 Jun 2024 18:37:11 GMT  
		Size: 4.1 MB (4060028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff44b8b2bf60aefe29ffc9578d1f4d9fcedd42a7276970f9ff9fea289a90966`  
		Last Modified: Thu, 13 Jun 2024 18:37:12 GMT  
		Size: 23.5 KB (23515 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:55884c02f0d85553350cdc8483b30a44a211fcbe22459bb6d837f3bfd75b659e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69671516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f88f4ee955da5ac21ccd8021a56c4d0c542d8491891420b209533991c75d4fb`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:78cff0ed53bbaaa1d7680e733d50b8fc9042e257b78718ad822f9ac57a5d1dbb in / 
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
	-	`sha256:f8a34d14f57d3fcf2d97b9fc0fb4439a2d00afe9411fdc788629eb4074186288`  
		Last Modified: Thu, 13 Jun 2024 00:52:21 GMT  
		Size: 28.9 MB (28936731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8299f45d60e6b9cce82f969894c4ec97c38df320136cc867af9804a22aa2593`  
		Last Modified: Thu, 13 Jun 2024 23:37:10 GMT  
		Size: 8.4 MB (8428996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d828ba615c8d8da958a3f083f77e8997b2c08d24cf57f1812caead7bb7cc2cab`  
		Last Modified: Thu, 13 Jun 2024 23:37:09 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9838f54bda525b445df6b4d562c1a10259e453566f1fdfeb9a8c6ebbc559319c`  
		Last Modified: Thu, 13 Jun 2024 23:49:43 GMT  
		Size: 32.3 MB (32305449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9259a4b1ad47a06c30d945790f34f6806eac691255266ddf448d8930c8940d`  
		Last Modified: Thu, 13 Jun 2024 23:49:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:ee4d595364abb8a68cb196e288681968e673d3a06f1769df8de0f25da4a64a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4556d6c94767dac292eb90083915ed4967e3f7c00488aeee2e8544bfd6b5ddc1`

```dockerfile
```

-	Layers:
	-	`sha256:c1a699eb6cb4fe399e033fd34caaed34b961e22f40156af45d68a9ada4540866`  
		Last Modified: Thu, 13 Jun 2024 23:49:42 GMT  
		Size: 4.0 MB (4031256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d19565a48fece626cdfeafc7e6f4b1311bd6d9d7313feff6bc14438ea22c29`  
		Last Modified: Thu, 13 Jun 2024 23:49:42 GMT  
		Size: 23.6 KB (23623 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:795cc069eb2b90046d2917248e45c752f503114c7ea6527b0c03efa0c2e416fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66743515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423f1d48448c7abf3681166c4e5d7475da8739272e32dd8909accbc1711b7ab1`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:b23992f77c1f22e7bf9048641d6da1d6ef922d78b4118f6d513e183ae6de7e34 in / 
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
	-	`sha256:4873d96591a32d2d686ff6c86338fc9a63b9d60639482601b5402eb76e56a566`  
		Last Modified: Thu, 13 Jun 2024 01:02:22 GMT  
		Size: 26.6 MB (26594507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bc2547e347dc15d2b6260f7cd1a925fa3560742fbf6e1eb2cf13a5c1fede50`  
		Last Modified: Fri, 14 Jun 2024 04:11:23 GMT  
		Size: 7.9 MB (7937123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8219c22d0b9649f87d3438b9f9b65ade0591ba08541a678bb6a8169a442e0ef`  
		Last Modified: Fri, 14 Jun 2024 04:11:22 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5604d7bb6a4a8d9f049bfe6b449037960edbc64dbc592833106e1f96a78cc950`  
		Last Modified: Fri, 14 Jun 2024 04:22:29 GMT  
		Size: 32.2 MB (32211542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf09b6db099e79469af002c5cce99e949407a805fc42526e3e4dfc2f9c865f25`  
		Last Modified: Fri, 14 Jun 2024 04:22:28 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:9dc1b2775d735bb8b56c62ddcab868924b60e8257197a921127f4bfe3b19eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461fd6fe20c07cebe711dd0b8c2c01041278f7ba0be47e604dc01f016a04082d`

```dockerfile
```

-	Layers:
	-	`sha256:91f2cd63def2a3bfc33b965d795695a870aff7bf7901be613d014b2b0c932d30`  
		Last Modified: Fri, 14 Jun 2024 04:22:28 GMT  
		Size: 4.0 MB (4034020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7967732038a38d17c6709ca546d8ca6d3001744ebf523eef07acecde50fe003d`  
		Last Modified: Fri, 14 Jun 2024 04:22:28 GMT  
		Size: 23.6 KB (23624 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:8a9ba616d4197962e795a13b49290984a307720bb0e79d7359c1787941504a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75273019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fff7cf9c80640d6aae3799bc95792eba2f4a879da71ed9ce36cc41ae5bb3ac2`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:55edb70d595bba9782144ef15994a2ae5c40adeb65f6c3acd6570a0c148ffa96 in / 
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
	-	`sha256:ca4da1869379178993d4f7abc946f75e7515789ff7e15c7ccfedfc8e2bfeaf6d`  
		Last Modified: Thu, 13 Jun 2024 00:43:54 GMT  
		Size: 30.1 MB (30086973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f893867e0d79074f980f3f1c85aadbcaae8bab3d6178d0b162541be5bed5d2`  
		Last Modified: Fri, 14 Jun 2024 01:32:40 GMT  
		Size: 9.0 MB (9036959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d472a5a993c4efbaf3dc267d4376793594e2743e2845b7a0a1e23b8131f1fcba`  
		Last Modified: Fri, 14 Jun 2024 01:32:39 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ebbdd9484cd991b56d13e42d975a58c39e838466efe4c7c312ca2c4b122367`  
		Last Modified: Fri, 14 Jun 2024 01:43:00 GMT  
		Size: 36.1 MB (36148745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26a8a1594410da5f722befafcd9f061a166449eb01733ffcbef46e6bc2d09a9`  
		Last Modified: Fri, 14 Jun 2024 01:42:59 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:1826005e4e8caa2e695d5863a096be998247fb09af8fb5dff147affed8f56618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4058236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b53d346b8c9dc341994390c60d87846189b7e364d9eebfc78025acfb4ed36da`

```dockerfile
```

-	Layers:
	-	`sha256:e6c1ff8e590039fc503db8be1a357362245fb2e61446200b4fde5b6af13fb051`  
		Last Modified: Fri, 14 Jun 2024 01:42:59 GMT  
		Size: 4.0 MB (4034412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8faca171bf993cd4a1781d248d7bac289bfbeaa7b99245e7c6ab0456f5aed27a`  
		Last Modified: Fri, 14 Jun 2024 01:42:58 GMT  
		Size: 23.8 KB (23824 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:b29cfd0c2962cc788da05968f1ed58e80c733915757cd96b2848e2391be551a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76501988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14af20e08523503a4708efc0b66ed9bbab79a3bd923c700259974254af5825b6`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:ef80ad838dee1f170442a02f8d0808e624e7c317df766c49aec042c1f3ac4732 in / 
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
	-	`sha256:71e749b27156c50e0706f9267afd1ca9fb38d6272a353964948602fb62336fd8`  
		Last Modified: Thu, 13 Jun 2024 00:44:08 GMT  
		Size: 32.4 MB (32424179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faf0af941144e29053533d728fc69416ebbb932aaaf489469e94e65d44f9fce`  
		Last Modified: Thu, 13 Jun 2024 02:12:44 GMT  
		Size: 11.8 MB (11791097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f7d3309e7bfc0ece99cb9dbd0abfc51ec066d2e81fb1741487c888e5b672db`  
		Last Modified: Thu, 13 Jun 2024 02:12:44 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0710d024c374e48381fa6015a47a12459434aa8c11e144664b57209c8a26b1`  
		Last Modified: Thu, 13 Jun 2024 02:12:45 GMT  
		Size: 32.3 MB (32286370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c4242478f44d1f8fdbbd5f81c3d55f49f6635e1302749620f15ac8e02187fe`  
		Last Modified: Thu, 13 Jun 2024 02:12:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:02e1d76ff4b752e3050a424f13224ce8406a7c96e811f6b317fd5de29531f361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4087714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ff63913d16bfa56c6368e4517b3995f97118527ec1d7c86bc1f5cf234f6bbe`

```dockerfile
```

-	Layers:
	-	`sha256:03bc17c146f2c68562ea675e904f76a39d4593b62c84606dc68124cbb341c22d`  
		Last Modified: Thu, 13 Jun 2024 02:12:44 GMT  
		Size: 4.1 MB (4064230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:303f3aab940b86a6dc2291a175efac079874c40f6f68da44a3e8597391beea19`  
		Last Modified: Thu, 13 Jun 2024 02:12:44 GMT  
		Size: 23.5 KB (23484 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:f0d59a6288d52c374ca6fe710a7c7a6ba4fc7b2764d8c0b76e7d8550cc0b38a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72913151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b16c4d4c6c78060fe9b443d2336cdab480f96015c1f45b91ba67abf12b1ede6`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:12:23 GMT
ADD file:ec3acf4bc32b149c2b67d1b2c5f3a6d1f16fbae266ac16c115e1fca276b970e7 in / 
# Tue, 14 May 2024 01:12:27 GMT
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
	-	`sha256:38917083d8284ce1ec7533351600bab5d64f8295f3edc5dc651be130fb9a4bd4`  
		Last Modified: Tue, 14 May 2024 01:23:44 GMT  
		Size: 29.7 MB (29651870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9bdeadc8276262e72fbab8c3530e91d025d182fb2a7c686bbcae99a64de5b0`  
		Last Modified: Wed, 12 Jun 2024 18:54:59 GMT  
		Size: 9.6 MB (9630737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0c375bba0f73ee4ef571a7bfd7df132982e9a8246f843d0fc68a47f35fe64e`  
		Last Modified: Wed, 12 Jun 2024 18:54:58 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc1ba9bc152322e0dbc320effdb6f1a7ab0389856be6de4a10226b6f6b2afc3`  
		Last Modified: Wed, 12 Jun 2024 18:55:02 GMT  
		Size: 33.6 MB (33630199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3773e9ff73197939d10747094b76076cb987c5666522da799df9d2f17f879532`  
		Last Modified: Wed, 12 Jun 2024 18:54:58 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:d3de1b13015cc49a6093429b1411f8815d618445dffd0fc164994832c2c1ee9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 KB (23362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812ba2b48ce1dc00d7009b1b2f708e4c6972f0c7f5cf9afbb74f180f3a8193d6`

```dockerfile
```

-	Layers:
	-	`sha256:e5fdbecb365b59de56ea590f691898061b3c25c960d128c024fed3734f149154`  
		Last Modified: Wed, 12 Jun 2024 18:54:58 GMT  
		Size: 23.4 KB (23362 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:e8b88eec3f0166f1215f22179658923eeb9b8d8dc2ede31580d57bb0a3b1c076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79566561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66e25a8dfcd8682da73ac64b152b1fbeb858c823a687fa2148513bc97376096b`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:a150537fc528657f8fa98f90c4629e38f111c3c3ef60bd40c28205959899c1a3 in / 
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
	-	`sha256:64741f366161eb41a5c86810e08ceabb9f4e4b69ac16c725aa2d48f19486e1be`  
		Last Modified: Thu, 13 Jun 2024 01:22:19 GMT  
		Size: 35.3 MB (35311302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76664c812ea54b660db03b982268031fd87f29408d08f77c6acd0537f5dde08a`  
		Last Modified: Fri, 14 Jun 2024 05:38:11 GMT  
		Size: 10.3 MB (10275993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0422e42a5209fd25bff3f940a4b936ab01c5f150f5b0302a609d5b7f2aa863e3`  
		Last Modified: Fri, 14 Jun 2024 05:38:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff82e4460a6457449023e71cd013821c646e33d36a4ccde67499bd81a7d6d19`  
		Last Modified: Fri, 14 Jun 2024 05:52:14 GMT  
		Size: 34.0 MB (33978926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4eee6c8e5924d926a7cccdcbcb9e83bad46696ed5416af73e0e7afe681282f`  
		Last Modified: Fri, 14 Jun 2024 05:52:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:28d1e2afbc9d5cff02ee99c6683051bf57e72c113143cf35399a0aafc3381937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4072483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d36a1cbcb72d6106d38b27bf03071b7be364c60d3a408654a07be6774ad4f7f`

```dockerfile
```

-	Layers:
	-	`sha256:b8888817653433423f5a054fe6b9a99cc3a8b60662d9a7de1d3eb92f3049c54b`  
		Last Modified: Fri, 14 Jun 2024 05:52:13 GMT  
		Size: 4.0 MB (4048920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f6398b9c632056415a0b99e023475e21c87735cddb079ede11805cb85cab948`  
		Last Modified: Fri, 14 Jun 2024 05:52:12 GMT  
		Size: 23.6 KB (23563 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:ac1ab576a6da0125e996b91a37554da95aa5df1da19173969e3b49bf9ee2506a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71900926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555245728a2860aab297996f950223c4f5cdbb355e704fb488358f34614ff94f`
-	Default Command: `["irb"]`

```dockerfile
# Wed, 12 Jun 2024 05:03:19 GMT
ADD file:dbc45f2c1dc4ae2fcf0e05b8c9401406afd0f7aa3623659e470bb7d0fb97f9ec in / 
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
	-	`sha256:b9966e11fe1c4138e9aa4f0356568463c21e36009b72062413bb596e0e57738f`  
		Last Modified: Thu, 13 Jun 2024 00:48:17 GMT  
		Size: 29.7 MB (29673762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301146ea7051b99e6b924f901f423e75ee55cc6f351dd74248bf9a4bd2dffe68`  
		Last Modified: Thu, 13 Jun 2024 12:52:58 GMT  
		Size: 8.7 MB (8656782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c93da59e7383989c4eed52045c36eb5b9c6edd3cd57d9fcfa3d85d9d08705e`  
		Last Modified: Thu, 13 Jun 2024 12:52:57 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461fefb16d5b123574cab4c0fcb8031ce896a661d8a71608d44cfa4a1e4f2cd2`  
		Last Modified: Thu, 13 Jun 2024 12:58:35 GMT  
		Size: 33.6 MB (33570042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bac5a5774a5a9dd2657ddae9dcba365300edc4159c8b278cd0a1f530d75582`  
		Last Modified: Thu, 13 Jun 2024 12:58:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:4de3bccc2d021f7fb842802007574c947e86b81f6d9c289d0510d7b69453b0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4072222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57a2180c1b6c65bfcc26691f43e17d9ee457e2c70dedddb29b1db6583e7ef6a`

```dockerfile
```

-	Layers:
	-	`sha256:80b1037e31abdc125b2c2b57c197e541c19229fdba5a1790b0d28fd5fd2b39da`  
		Last Modified: Thu, 13 Jun 2024 12:58:35 GMT  
		Size: 4.0 MB (4048707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da22b8dd7aaaaa74f77e066d4ac402f62c6cbd157395fadaa58f975ec49b815e`  
		Last Modified: Thu, 13 Jun 2024 12:58:34 GMT  
		Size: 23.5 KB (23515 bytes)  
		MIME: application/vnd.in-toto+json
