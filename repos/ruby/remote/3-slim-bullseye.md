## `ruby:3-slim-bullseye`

```console
$ docker pull ruby@sha256:188ffd25a9ac1d835ac862e3610f2e89126b21add4320ea2dc22253096536275
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

### `ruby:3-slim-bullseye` - linux; amd64

```console
$ docker pull ruby@sha256:e65af99e0e4c1ff6ccb3094c1294969c1a6fc3c8a81e8fe1029402f53081be8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77635390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9207f5862cb8245a8545096926c9afd9b3a0272f8da909f0a3d90258ab1869`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d818156d6dbf3335d1eb79804544f5f6328c2d132729f349cc5da34ecb9fa627`  
		Last Modified: Wed, 10 Apr 2024 02:58:24 GMT  
		Size: 10.0 MB (10019329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c43f25b030bde020f0c4aee70be2d6bc1d2078b084bda6b1e8aca332ac726e3`  
		Last Modified: Wed, 10 Apr 2024 02:58:14 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ad4c7998710b36fb2d6f9d77d06dbb235fdc1d1841da253473742ef97b0261`  
		Last Modified: Wed, 10 Apr 2024 02:58:25 GMT  
		Size: 36.2 MB (36187982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e360f6f60f8d383a22aed28aac6fb390210a468a64982f1f082596ff07b15f3d`  
		Last Modified: Wed, 10 Apr 2024 02:58:24 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:8042ee9cbd88b19c0a98826a3cdc0cb72ffbfbd721ec5a40781592608dee5840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4084715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4377459023c33f9d80ee46939201d50aebeed2d18d0bb31ccd802941006a5dc7`

```dockerfile
```

-	Layers:
	-	`sha256:a5426117bb68c2cc2cbbcb34e235ab94b135ed1ce986d7fcd17947b7f28391ea`  
		Last Modified: Wed, 10 Apr 2024 02:58:24 GMT  
		Size: 4.1 MB (4059822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e188405ae1e93b0a03e9d7966adff07d5945d15892a17e138d64e0deceb629`  
		Last Modified: Wed, 10 Apr 2024 02:58:24 GMT  
		Size: 24.9 KB (24893 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm variant v5

```console
$ docker pull ruby@sha256:f63c8032e9bc08c7e995e5a16bd08d021930c7c08c8b4f9875303c8d4c431285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69814457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307decdb857030cd0bad5ce367f195c0ad253db58ced343206792d5abbe32d1d`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:aeb4c3fa8d40bc17d70f21cc12bb887fee25ce28edd7cac250e250253b8d2819 in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:a106aa5ccf7f6fa63e0c6a2a69c3cda22393d46be963a8867a2894dab3644cc7`  
		Last Modified: Wed, 10 Apr 2024 00:55:28 GMT  
		Size: 28.9 MB (28930200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d5509abb4dfb9552f0960fbe4b736be3cb3b9b48e629a023adefbe8d09d446`  
		Last Modified: Wed, 10 Apr 2024 22:51:00 GMT  
		Size: 8.6 MB (8632590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31226bf863061307244d631dc1c14ebf1b3482201e18b328ab563454e9f48def`  
		Last Modified: Wed, 10 Apr 2024 22:50:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9083ce4d55f7e19a529b3dc5edefe54b26e0f4cba038870813a6cc2e91efb02`  
		Last Modified: Wed, 10 Apr 2024 22:51:01 GMT  
		Size: 32.3 MB (32251325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd48fd9a6f98cc73420f3e625650cac0dbaa2cc47244ee11db1b31bd097d51b`  
		Last Modified: Wed, 10 Apr 2024 22:50:59 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:e5728393793fec6d6aac72abf4c3ef25943ef7ddb3d02d14581ee9cfcb68b8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85985fd75d79c255ec5f964103f506c75e76d8e3dfe0905f50b89ab8d3bc39ca`

```dockerfile
```

-	Layers:
	-	`sha256:c053aea5fbbf09e9a3a579bb03fe8022c9d78a3b8170b864ee48c883adc16bf4`  
		Last Modified: Wed, 10 Apr 2024 22:51:00 GMT  
		Size: 4.0 MB (4031052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96535f83b9ac144c6a61d7b7b149e0593387b0911822039c29317a78c0bb5b5d`  
		Last Modified: Wed, 10 Apr 2024 22:50:59 GMT  
		Size: 24.8 KB (24831 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm variant v7

```console
$ docker pull ruby@sha256:66d57b30e8434af7792e38850be2045727ca4da01b8906b5b9ee9f0fcf628795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66893056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359cb221dadc814006d2db994d758d3f091ea47d9779dc2166596e602126d997`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8fdd169573f27730e9294d26e032f35ba1de7a60bf3263eb4d8e57ca4f05df`  
		Last Modified: Thu, 11 Apr 2024 10:26:01 GMT  
		Size: 8.1 MB (8140942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ee0e0ab9d47ac17629b55735b1121c9be3d42fba1d27877ca4b717c3f37128`  
		Last Modified: Thu, 11 Apr 2024 10:26:01 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4760e029c153bdfe4c5da9ff6c5bae2f54b178ea8f80e9512d31610589d7afd7`  
		Last Modified: Thu, 11 Apr 2024 10:26:01 GMT  
		Size: 32.2 MB (32163298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e65fda2862b4e0b09ca40e46c433b1defd8b1958a42f11b41105a7e3bc1ec9f`  
		Last Modified: Thu, 11 Apr 2024 10:26:00 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:93cdee3da69925ea6a9fddcd4ebb86c389796fa0ee565b50ff183f8451f27d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4058647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5615758854e146a135af83ea616d52b7998254af0eec675e17489c84df79a21`

```dockerfile
```

-	Layers:
	-	`sha256:7cf3db45c9e5efca8e54569d0198e65e638c1d6bdf7517c83673c54c20fd7b12`  
		Last Modified: Thu, 11 Apr 2024 10:26:01 GMT  
		Size: 4.0 MB (4033816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa2faa58a545e67d736069ac32570820794ca9109472dc84b4bc16ebdc17e4ee`  
		Last Modified: Thu, 11 Apr 2024 10:26:00 GMT  
		Size: 24.8 KB (24831 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:ec090dcc54d137c0f134906d45e4782335c5c96a7551f6a46b642a3a640e7f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75411268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d59e01eea5aa8f00378f3298d1a8b20ca5462f1ac993c4c809f36eb22934ffe`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21153df6adaca06011d1a0ea43e39f2490bcecceb2628110e9345c4dcabe712e`  
		Last Modified: Wed, 10 Apr 2024 21:03:03 GMT  
		Size: 9.2 MB (9240916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ae8750a207f9f45627d0397af3230d237fc97e42d48196565d0b36008c1738`  
		Last Modified: Wed, 10 Apr 2024 21:03:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:302fb7afb0137a33f63d0dc0338e815b2d36bb2a58599638e461bcd9a5dbb1ef`  
		Last Modified: Wed, 10 Apr 2024 21:03:04 GMT  
		Size: 36.1 MB (36093706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579f8f7c50ebeba887cda15afda7f90a143e2a45d12e1e6ad0036d420975e7ed`  
		Last Modified: Wed, 10 Apr 2024 21:03:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:8fd95b805d66fbca9f40ed9c0c9d9fd19c7ea8fff8ce5c4fab0bb4ef50bad178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4058894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc2e09b43dca93e25da035f3db5aa90d50a21fd85cc6f31b53112d69b827692`

```dockerfile
```

-	Layers:
	-	`sha256:f701a7e3113f89e25d0371d568b69460aee044284dd6a3977ae58561a936e4ec`  
		Last Modified: Wed, 10 Apr 2024 21:03:04 GMT  
		Size: 4.0 MB (4034163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30020d45b43ae93cc4c32afaa1a959fb62ac64325c56e612b02f11739c0324be`  
		Last Modified: Wed, 10 Apr 2024 21:03:02 GMT  
		Size: 24.7 KB (24731 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; 386

```console
$ docker pull ruby@sha256:d1ae910549abc851f57f0b27da03005d3e962beb1416b90f4bdd700b7ce89425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76644310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee662f9cdad6cef4fb0765c28103a008a9749b441cfc97841afd4e32dfed0d1`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923a1d1744bf83386f72e8d3bc4a69c41559e013a4dfd6cf770b86e0d5db7fe`  
		Last Modified: Wed, 10 Apr 2024 01:56:33 GMT  
		Size: 12.0 MB (11994415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a5217c26cb2fcc8e98bd176bae5d548d23bc926d8dd0120c4ecd4072beab8d`  
		Last Modified: Wed, 10 Apr 2024 01:56:32 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8542f5a4e3c21a4519fec7d669005ab35f9ff3341110a418e6730be84e8b2ac8`  
		Last Modified: Wed, 10 Apr 2024 01:56:33 GMT  
		Size: 32.2 MB (32236136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22700572d642bb9ff72529b2ddd8136ca538b65b3e01569fd7a8ef1a2c2175fb`  
		Last Modified: Wed, 10 Apr 2024 01:56:31 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:3002bef93f1e43b3e6b6112ffd382ef491bbfdb4ca214e8bfa402f739ea2c8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4438fbc681390893f3f105e0c61dc12627ce35150ca768394ad586fc6234fa8e`

```dockerfile
```

-	Layers:
	-	`sha256:618c8eec23677eb22998d43ea21dcf2d19985f284b925420e5e4258fb7695e0f`  
		Last Modified: Wed, 10 Apr 2024 01:56:32 GMT  
		Size: 4.1 MB (4064026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91ee2113276e04a7847faf5e790f7c1300325dff659da535f66906b13fe27488`  
		Last Modified: Wed, 10 Apr 2024 01:56:32 GMT  
		Size: 24.9 KB (24858 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; mips64le

```console
$ docker pull ruby@sha256:a9e1f57298d65baaa205a4b005dc8c32640f9d04f30f568acecb22440e353ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73046904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2eb0134f12f93fdba28c72460af04bf17f09ac20f59208624f801713b0b1f5`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:5a3b2305df619d313e2592819c382781fd774d11c3f687bc9ca004eba259694b in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:94315f37c06e4616cd911d9cfbe5597a620ca0249447454791c232fa7b1e2724`  
		Last Modified: Wed, 10 Apr 2024 01:23:22 GMT  
		Size: 29.6 MB (29645932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815e1ebdd6e16b5b461c70154140f5e163f2b52166380328861308513453339c`  
		Last Modified: Fri, 12 Apr 2024 08:36:05 GMT  
		Size: 9.8 MB (9834063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d809c4f31c9985a2fa4e231de91920e6ce547b6399ea33c4a986147f824d78af`  
		Last Modified: Fri, 12 Apr 2024 08:36:04 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb18d0b6bbe069c5ad23d68a82cbe77489311e09c899616736e2d9d8c6b2947e`  
		Last Modified: Fri, 12 Apr 2024 08:36:08 GMT  
		Size: 33.6 MB (33566568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed582661af7849ef2f35257e03ad88925dd91b1129274d45beff9544da3f6ad5`  
		Last Modified: Fri, 12 Apr 2024 08:36:05 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:dae344f3e0e28d84af82829918793e5f83bed4db23642b84d24da79c1516082a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 KB (24572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058acc31e25e4d26f8345b10c2b1a44d0b9b26296223f38b46779d67b2e9142f`

```dockerfile
```

-	Layers:
	-	`sha256:37cc1b5775f487a39005751c6e476aaaa1eb138c5c348868d130bb91d6d829b6`  
		Last Modified: Fri, 12 Apr 2024 08:36:04 GMT  
		Size: 24.6 KB (24572 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; ppc64le

```console
$ docker pull ruby@sha256:42f1b009542457d81fa1d89f9aab3b4711007644bd51ca8d3324f59a6317a312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79708369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d44d8d528aac42f8096f384494aaa8294e631cd2653dbd43ed3367ea0acf9e4`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c3fea527506aff79b9879a30987450769618807c92c1578f10ab3b96e69f93`  
		Last Modified: Wed, 10 Apr 2024 22:08:44 GMT  
		Size: 10.5 MB (10479565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab72c7a06c7e93562f5cdea858f877c9d96d5c61d1f9b31ed184de490c1650f0`  
		Last Modified: Wed, 10 Apr 2024 22:08:44 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe0eabff0c772bfc0316afcc55909f9d40673c229b3787bff8f2baeec63a366`  
		Last Modified: Wed, 10 Apr 2024 22:08:45 GMT  
		Size: 33.9 MB (33924373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2674992ea6e11ebd7af4d32b6569a6b884f46b4d7b62739ad4cc9b00c2da49`  
		Last Modified: Wed, 10 Apr 2024 22:08:44 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:984766d1233a41ef65d99d85a473e5b7ad4ce8e11b98db7253ba1f58ff2d0a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4073486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e6606d4ed6b6867ddf656e8a6b94bdcac5df03059499a6e29a1ccdae1c920e`

```dockerfile
```

-	Layers:
	-	`sha256:932b650f3cf6f1de17aff150eaf9b398af84c22f2fae07d17b32e2374a18ad3a`  
		Last Modified: Wed, 10 Apr 2024 22:08:44 GMT  
		Size: 4.0 MB (4048716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce797361a7ab15c213f3ccc6a38dad591204170a24b4b6498006d9b46f30fbce`  
		Last Modified: Wed, 10 Apr 2024 22:08:43 GMT  
		Size: 24.8 KB (24770 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:3-slim-bullseye` - linux; s390x

```console
$ docker pull ruby@sha256:8b797bf6bbbcf3d7d8ae568b37e5d5b7ad3ddefe68f064b7687da1e1dc95b1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (72039678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935379305dd9fd4078fd8ba35cc8b9bfb0d7bf8e654e20d94249268c77267ea2`
-	Default Command: `["irb"]`

```dockerfile
# Fri, 05 Apr 2024 21:54:06 GMT
ADD file:173b309178d19f7fccea713c7c575233510e5f065fd2d92a5378f001a1d33846 in / 
# Fri, 05 Apr 2024 21:54:06 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:54:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgmp-dev 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		g++ 		gcc 		libbz2-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libncurses-dev 		libxml2-dev 		libxslt-dev 		make 		wget 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='0b2f6c8f85a3d02fde2efc0ced4657869d73fccfce59defb4e8d29233116e6db' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.26.0/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='673e336c81c65e6b16dcdede33f4cc9ed0f08bde1dbe7a935f113605292dc800' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.74.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		{ 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new; 	mv file.c.new file.c; 		wget -O 'arm64-fix.patch' 'https://github.com/ruby/ruby/commit/7f97e3540ce448b501bcbee15afac5f94bb22dd9.patch?full_index=1'; 	echo '86bc65415fd62cb2272a4df249f39fb79db15617ad05c540e05a22f02eae73b3 *arm64-fix.patch' | sha256sum --check --strict; 	patch -p1 -i arm64-fix.patch; 	rm arm64-fix.patch; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
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
	-	`sha256:499f72f2d94381b6df4b58d8ad4918f9e03fc5d140cb0704842fd78e2e63e391`  
		Last Modified: Wed, 10 Apr 2024 01:49:00 GMT  
		Size: 29.7 MB (29666840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ceeccc633762f833fcbcb51166724f814db9d1cb533fa8d990825b0f5e78a2`  
		Last Modified: Sat, 13 Apr 2024 15:31:17 GMT  
		Size: 8.9 MB (8860631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493626a4436fe89943dcd15ddaf594a71631a7386637d006f363ea8dbde82208`  
		Last Modified: Sat, 13 Apr 2024 15:31:16 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f227e3e3c8e057f634784208d313f04378fd0ea729b9869607088a43ce5089f6`  
		Last Modified: Sat, 13 Apr 2024 15:31:16 GMT  
		Size: 33.5 MB (33511865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eecb466adbc45e6099658127d21826283e814761a5c06d42bd22eddc82f7873`  
		Last Modified: Sat, 13 Apr 2024 15:31:16 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:3-slim-bullseye` - unknown; unknown

```console
$ docker pull ruby@sha256:4d6a5fcf3b0178888862a1921d8c7465cf21ef23dd4d27b59ed47deda58bfefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4073225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019eed935b4f6a17b7a9a2ba682cc530b91b35459038a5a31a11a304933a8533`

```dockerfile
```

-	Layers:
	-	`sha256:1bba0a09c31b4ad9850424770a90fe4d39968b48ac0222265a0d96b9dc7ba407`  
		Last Modified: Sat, 13 Apr 2024 15:31:16 GMT  
		Size: 4.0 MB (4048503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82587cd71d51f6a41a5cb4d4c6866b8ca89d499c439f6154bd72908bff7784ed`  
		Last Modified: Sat, 13 Apr 2024 15:31:16 GMT  
		Size: 24.7 KB (24722 bytes)  
		MIME: application/vnd.in-toto+json
