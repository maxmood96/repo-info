## `ruby:slim-bullseye`

```console
$ docker pull ruby@sha256:5f39a14263b82b369d7e975a55aca0f4895974860da57c20dbda48f257145f3b
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
$ docker pull ruby@sha256:91c333d8cd9581bdfe19815924c24b616b2456ee3fba538702dd6568bd06cd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69671695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2773bdc97ab6e3ae4a51261e82eb7d65490f58e642de46730c237d25a76e6c2`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:48:50 GMT
ADD file:7a63cf2b5d16adf102fbd2452be219224667c4ea55981247f398a4a867ef96c4 in / 
# Tue, 14 May 2024 00:48:51 GMT
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
	-	`sha256:b6ea79e472ea80a508a2732ddeb0e19de51d3f0aaf8f0fd18c1cdd1c939d49de`  
		Last Modified: Tue, 14 May 2024 00:52:17 GMT  
		Size: 28.9 MB (28936721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4775b5487b931add102cd449830f14c321481b5fad469f5db0046f27f86c8e`  
		Last Modified: Wed, 12 Jun 2024 18:10:10 GMT  
		Size: 8.4 MB (8429153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a36ef1011a85939389048ebd59c9db0ee7f85e47a42864a1e62d3a027b48f`  
		Last Modified: Wed, 12 Jun 2024 18:10:10 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b570d01468980fb8ee1ef8b410bde45734be85862ff7d20794ce1399998274`  
		Last Modified: Wed, 12 Jun 2024 18:10:11 GMT  
		Size: 32.3 MB (32305478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e769d24ce2ff1c0ff0b0dacc26388367bc7ff74ee183f018b2a735c9ec3578af`  
		Last Modified: Wed, 12 Jun 2024 18:10:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:8332771e9aa9f7051349a175018006addfd4d8743b90cd6a9366a802eaa6e74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327666152ffec6993ef38e2c62d3505de53e3f21c1474bea9bd92fd7657b98a1`

```dockerfile
```

-	Layers:
	-	`sha256:5b779bcc6ac900c63d962601e89dcddcc01ff39e5802504b2f5ab6c5e8ec95aa`  
		Last Modified: Wed, 12 Jun 2024 18:10:11 GMT  
		Size: 4.0 MB (4031256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5033dc33d4815c3ff4017bc9111fde2d1a0707b5f234bf8664b45607d1e7abc1`  
		Last Modified: Wed, 12 Jun 2024 18:10:10 GMT  
		Size: 23.6 KB (23624 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:75a1cc702baec137605e9d7827a4839109d1ed36bb52cb93ccd0ef400bb581c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66743706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5595f450a1eff982a405da80c30e1fce0bde1c7470fc3ade8de102af60794787`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
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
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5519f639b8f90b81edb88bf425fab2cc8d4d42adc0006fd3cc78261774ecf3a`  
		Last Modified: Wed, 12 Jun 2024 18:11:46 GMT  
		Size: 7.9 MB (7937192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbf0d671afa0a528c4f969180507bff7a928f574581070fd5649f622bd74be5`  
		Last Modified: Wed, 12 Jun 2024 18:11:45 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38d3e98fcffae491e41ee857e00476c540f40b5e046a490c6b8f8cf3e8830ec`  
		Last Modified: Wed, 12 Jun 2024 18:11:47 GMT  
		Size: 32.2 MB (32211678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a0ae75b6580d4d5c1a88470a2c3213529be60eb486a41ecb62661436cd8c3c`  
		Last Modified: Wed, 12 Jun 2024 18:11:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:0a08ecbe04c6dcf0874e4794a5170576d596cb7e7b77cc78843597416db362ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7318c4469a2afe7067276de95491c1f78585ac05ab429e8f242734e852f1573d`

```dockerfile
```

-	Layers:
	-	`sha256:a7da23595793f166505b97f3b9cfa2b00a0135136f50173cbb8736a59d8e6f99`  
		Last Modified: Wed, 12 Jun 2024 18:11:45 GMT  
		Size: 4.0 MB (4034020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a6b2f598d7cd6bfa5f59c7a6d71d34cec8445506f4d10734c8c94ef44d4a64`  
		Last Modified: Wed, 12 Jun 2024 18:11:45 GMT  
		Size: 23.6 KB (23624 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:728fb02bd9187d19192f6a145e749ace356b165decca39095c44327ba8a9c5b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75272955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37401da11feaf4efbe590cec517c33fd4f58bcd7846810d51a1d06f55a6c98e5`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7042777c70cd233b8ce6406413e7054dee0ae48535bab3e6dd01a0347f6774ec`  
		Last Modified: Wed, 12 Jun 2024 19:03:29 GMT  
		Size: 9.0 MB (9036889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c840ec813ec9980064a3144a8569fd10f0b9d5c13eeae04ba582251bfd574105`  
		Last Modified: Wed, 12 Jun 2024 19:03:28 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c984252e3710165604815fc335378aeb2673bfbbc35f08a56e709da9b799f549`  
		Last Modified: Wed, 12 Jun 2024 19:03:30 GMT  
		Size: 36.1 MB (36148815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419315ebe54bc01a60e321930a662a967dabe09e4d5a5b3955da876ea1d23e42`  
		Last Modified: Wed, 12 Jun 2024 19:03:28 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:a83a46a359b3cb6e3ca6f1ab7a02c5c33f8c8d122a6e7f2c0adddefed93e16ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4058236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e603fb74d863358046074756dcede02d4bc879e6df3ba095a9beebc98f229d`

```dockerfile
```

-	Layers:
	-	`sha256:a238843349398b304ac0d111bfb8cba83fd2da4dc817cfdd26ab2e4857442a8c`  
		Last Modified: Wed, 12 Jun 2024 19:03:29 GMT  
		Size: 4.0 MB (4034412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae05c8a03f25e7df70427091ddf2cc3d0f510d04f18a56be184802cfdad4f2b6`  
		Last Modified: Wed, 12 Jun 2024 19:03:29 GMT  
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
$ docker pull ruby@sha256:f185a618abd73cd5d96b13935ee10a961d086e0f3b3629cbb53b802fc47fc5b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79566445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eedbcdfb38618ee94568a8637707c1fcddb3f6ff2149a696463f04e4a9953fe`
-	Default Command: `["irb"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
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
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed24fddc7169e3bb21b39e934bbdc7b7e189903934eff3483ca1338725b46377`  
		Last Modified: Wed, 12 Jun 2024 18:11:18 GMT  
		Size: 10.3 MB (10275985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63afaf0592085a07ba4cbc2ddb7378330947eb4efafc13a4c0c80eae7d61d470`  
		Last Modified: Wed, 12 Jun 2024 18:11:17 GMT  
		Size: 200.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746e47ecac356736ed3549a1ada210d3171f88f44174c692f348103fe17a55b2`  
		Last Modified: Wed, 12 Jun 2024 18:11:19 GMT  
		Size: 34.0 MB (33978958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf85911a21d113f8ad689c3fff4ea1d2de5a3d237688673fd2e6fbc185c5ca7`  
		Last Modified: Wed, 12 Jun 2024 18:11:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:2ade64f127ea541d1522ab51efcc9d9942bde1bdaf0018804d2bfbf2df9b5c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4072483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bf1a11cf721bf35b3dcfe96b5607e1997d9646ee16843cb78aa41802bbd2b9`

```dockerfile
```

-	Layers:
	-	`sha256:c416643a6616db2284be82789124d53b1c82ce865e4c14a9c318f14a10754145`  
		Last Modified: Wed, 12 Jun 2024 18:11:17 GMT  
		Size: 4.0 MB (4048920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60d308337ed3148603e955c3e631ebe4819170cd0ef127e263819c8d577859b5`  
		Last Modified: Wed, 12 Jun 2024 18:11:17 GMT  
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
