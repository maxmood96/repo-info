## `ruby:slim-bookworm`

```console
$ docker pull ruby@sha256:c444c5c8f4eff4354ea80b4b2ffdec911a189cdef7328527faf74e57f66a67e6
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

### `ruby:slim-bookworm` - linux; amd64

```console
$ docker pull ruby@sha256:f37d950b1fd5742b144b1a12573dbb15e85456c858492c4c9255456cbaafd4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80711817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d1d08746835ff9047d4cc3ad9956274a99dd4518912dae799950acccf56c4e`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:44:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:44:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:46:41 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:46:41 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 24 Feb 2026 19:46:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 24 Feb 2026 19:46:41 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 24 Feb 2026 19:46:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:46:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:46:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:46:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:46:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:46:41 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a172b344bc2e2582441759f0f5aa34249a35c719522362f710a438ae8e16e3`  
		Last Modified: Tue, 24 Feb 2026 19:46:50 GMT  
		Size: 3.5 MB (3510178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2664f82557fa3198894460fab0d2ae50e54614bd19aa3f4fcdb07992c847e8f4`  
		Last Modified: Tue, 24 Feb 2026 19:46:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c9fbc0b1e9fddd1f2cc8ed3242ed0ee9d4fa903a67c30b469f7a756453ea38`  
		Last Modified: Tue, 24 Feb 2026 19:46:51 GMT  
		Size: 49.0 MB (48965028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3d942902ea4dafedffd9e43373e98201f21bed4097777c282d446f6eb913c8`  
		Last Modified: Tue, 24 Feb 2026 19:46:50 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:475f6942c318bea0c285e776c9327dbcd9c45c32a58da556a1b873a82cf0b1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2620866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c61585a54746998e4de8516511ef923609810140de38defebe8e80fb2923ab12`

```dockerfile
```

-	Layers:
	-	`sha256:dadcbff5642b8a5fe1510dd795b95a88fbc9de7563dd85cfc0483069d8c2d305`  
		Last Modified: Tue, 24 Feb 2026 19:46:50 GMT  
		Size: 2.6 MB (2597662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a2aa8e8182bf8b10aab94be797b7bc8d80e66c4dc1a73299dc7cf6fbae6d18`  
		Last Modified: Tue, 24 Feb 2026 19:46:50 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm variant v5

```console
$ docker pull ruby@sha256:f86a47ddfae2b9f3ee74de6c2159aea9db772bafe1429cee4da2f5d0c763bdfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70820641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bebfaa24f8a07f983becccd4771ca39b644e5273662194f8b1efdaef247da5`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:34:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:34:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:37:04 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:37:04 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 24 Feb 2026 20:37:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 24 Feb 2026 20:37:04 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 24 Feb 2026 20:37:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:37:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:37:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:37:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:0355804b1a863607635e8e60f82ed6fec21aeb11cd0f281ea39f54208fab3bb7`  
		Last Modified: Tue, 24 Feb 2026 18:41:57 GMT  
		Size: 25.8 MB (25765637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fa51847b13786766a20d96ac7506437d387e7a1249633e0e5bed1026ee3581`  
		Last Modified: Tue, 24 Feb 2026 20:37:13 GMT  
		Size: 3.1 MB (3081086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4ea94e70eb099d31ddff568ae4f4cbfe68c39c5671ee2c35895f3ac1f2709f`  
		Last Modified: Tue, 24 Feb 2026 20:37:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c072a5abf5afa4934ff9aa2d4143a22db13239a23a255af0d99e1b44ffe78d4d`  
		Last Modified: Tue, 24 Feb 2026 20:37:14 GMT  
		Size: 42.0 MB (41973585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21835c2d24492a501a3821d3f16686bd451edf297c400964a535184044e5632c`  
		Last Modified: Tue, 24 Feb 2026 20:37:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:581b0e27d8e6100a4e292507ce09ecf676a06faf3d2bc004438314cbdb7c9c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2624789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ba2c2bbf8e4789b7034cc9357f989b9849402dda2a4ec7fae065827c6d98cf`

```dockerfile
```

-	Layers:
	-	`sha256:304992c132ed226c0e4dae0b61f091a6244fbd16b0918ebace82d542580e6921`  
		Last Modified: Tue, 24 Feb 2026 20:37:13 GMT  
		Size: 2.6 MB (2601467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aedd062cc9ce4d456b7fcbbac5d332174c9560b83bfe68de6e40df4bfb473e39`  
		Last Modified: Tue, 24 Feb 2026 20:37:13 GMT  
		Size: 23.3 KB (23322 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm variant v7

```console
$ docker pull ruby@sha256:dc53de8d35860eb495c486ea8ca7290544a52fd0903c862bc12ca09a09523fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68632710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a41505a5353ced44c0b233539720982b623120734e4c3aeb2ef0b1b46baac92`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:06:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:06:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:08:55 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:08:55 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 24 Feb 2026 21:08:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 24 Feb 2026 21:08:55 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 24 Feb 2026 21:08:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:08:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:08:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:08:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:08:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:08:56 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8b4504f04cb6e38e6081d95037bc4350be4616c4eb55d1409d4f9be5fd8c49`  
		Last Modified: Tue, 24 Feb 2026 21:09:05 GMT  
		Size: 2.9 MB (2913739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4f0a72754996bb6cb03bf3dff5ca3ba1cdeeaa94a84ba25635ebc968647f06`  
		Last Modified: Tue, 24 Feb 2026 21:09:04 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc9838532d757aa39335babd7fbf0b924b8f1003f20234c8f5b219d986eca8e`  
		Last Modified: Tue, 24 Feb 2026 21:09:06 GMT  
		Size: 41.8 MB (41777240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaadd4b5bcc27014c522a684b6b8e71448e2f8e0f95982700a2c97261f4f17b7`  
		Last Modified: Tue, 24 Feb 2026 21:09:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:f59c0d4f89c5a6fda5e9728878561619835649e9deae7423f4b99c809285a301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2623209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d92f2e1625e8badf48aa9d55e83f0ee0dacd90d1b1b371359df0c7475575d2`

```dockerfile
```

-	Layers:
	-	`sha256:1734338e0c5af09ae2082309d156919c15141f48871ee6fb2f0c6e9610b2d4d6`  
		Last Modified: Tue, 24 Feb 2026 21:09:04 GMT  
		Size: 2.6 MB (2599886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16576382eb3cb0bf186fca077880ce2a627cbdce979728a11589c8d49c93b1e2`  
		Last Modified: Tue, 24 Feb 2026 21:09:04 GMT  
		Size: 23.3 KB (23323 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull ruby@sha256:448d441f858afaa0611b41e9a727f1858afea2984aea0c428c865c93a9b0f0ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80189007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8380d2573a852b555b2849d0792726af92a12158da1f9574195182241c4660f`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:57:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:57:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:00:03 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:00:03 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 24 Feb 2026 20:00:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 24 Feb 2026 20:00:03 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 24 Feb 2026 20:00:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:00:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:00:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:00:04 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5941d68c5c81c390132f61ef23132899f850016d68824ccbe548748bcf6e21ba`  
		Last Modified: Tue, 24 Feb 2026 20:00:15 GMT  
		Size: 3.3 MB (3341480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885f486df865143b7f07c182bce37857f63ceb83518362ce0c533b75d95ad2b3`  
		Last Modified: Tue, 24 Feb 2026 20:00:15 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dfa4df24bcc5fb584e7345357f528fd011174814e277aa7ba6a9f9efb14ff7`  
		Last Modified: Tue, 24 Feb 2026 20:00:15 GMT  
		Size: 48.7 MB (48731114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe4f46dc22210d56df89f013500be3c405e0b938c62082d49b891859f73adf7`  
		Last Modified: Tue, 24 Feb 2026 20:00:14 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:78794ee4c95ca2f04bcfd1779094d51418e040c0da9aa40d916e37b17983dc09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b33723c5e0368ddcf30939df6746d9e957eb7706989a92a631e234a58497231`

```dockerfile
```

-	Layers:
	-	`sha256:9a8d8fb4b6e0051f9665613e0ac01358230831251e36dd699a2799e46bf909f1`  
		Last Modified: Tue, 24 Feb 2026 20:00:23 GMT  
		Size: 2.6 MB (2597920 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bacc857da2ef5045b12abd00192c00729476299d5755b2ed8f56483d8ae4cea`  
		Last Modified: Tue, 24 Feb 2026 20:00:23 GMT  
		Size: 23.4 KB (23353 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; 386

```console
$ docker pull ruby@sha256:d3870be812a104b77f86b4ab1cff4262cb4844cf55a882ab96f2bd04b7e94af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74478478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02b86fc06f7387788da89145ac63b0fb618f0ff6f6cb2a81b77bc6354b40154`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:49:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:49:13 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:29 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:29 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 24 Feb 2026 19:51:29 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 24 Feb 2026 19:51:29 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 24 Feb 2026 19:51:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:29 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:29 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf344423908c055405d4b1141faa38cdd634aad2cc35571f5b051292e743cb8d`  
		Last Modified: Tue, 24 Feb 2026 19:51:37 GMT  
		Size: 3.5 MB (3512881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699365edb227693a3c4ac029a64941114a31fce22872fd41708c16a3ba9a15ca`  
		Last Modified: Tue, 24 Feb 2026 19:51:37 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8441e56cb89d591e714657e8c8106d8e77e180fac6bd8d83a7c8a450545617`  
		Last Modified: Tue, 24 Feb 2026 19:51:38 GMT  
		Size: 41.7 MB (41743560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92da984c564dc182364a7babc92bab7abaae706fc878b166cafbc06ffc1c7edf`  
		Last Modified: Tue, 24 Feb 2026 19:51:37 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:50183dc6561eaeef95d27bcee855f61390b44cc077e74d3b7b9e81202cc219a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001dd79832f83b8d7e6a17b6711c2920cc87d34d09a1bdd07916afe82b122255`

```dockerfile
```

-	Layers:
	-	`sha256:00bad012e950a540461d30f1d5fde477b5d82e7246d77c06e3061351106256ea`  
		Last Modified: Tue, 24 Feb 2026 19:51:37 GMT  
		Size: 2.6 MB (2594843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c4256dee5f682fcfce5c73b06036dc17180c9faf797c916fe1d61af27375605`  
		Last Modified: Tue, 24 Feb 2026 19:51:37 GMT  
		Size: 23.2 KB (23166 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; mips64le

```console
$ docker pull ruby@sha256:14904c33bc84379a537738015a6393cb611b9753b83d5644740d75807fc0a91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74759622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d05b3f2aac7b4921c4bffbcacdddb98e7b56af48cecc611513286afc0a27337`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 20:23:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 20:23:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 20:39:02 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 20:39:02 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 03 Feb 2026 20:39:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 03 Feb 2026 20:39:02 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 03 Feb 2026 20:39:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 20:39:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 20:39:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 20:39:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 20:39:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 20:39:03 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:1fed8ed52dc6e52b96afc1da0ccf85c92c81820372fc78b006f957e9c58ff600`  
		Last Modified: Tue, 03 Feb 2026 01:13:02 GMT  
		Size: 28.5 MB (28513693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4332e062ead88e865b900411aa84b48967521d258e5cbfdc7ffc9d3c2f5ac918`  
		Last Modified: Tue, 03 Feb 2026 20:39:46 GMT  
		Size: 2.9 MB (2901235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6084a7f4f983ef20122f8895b6a73ece2167eb7185f74ae3e3ec16b84043ec0e`  
		Last Modified: Tue, 03 Feb 2026 20:39:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2afcefd2c2ebd3f68a8dfff9fccb1246080712d89949a54e0043728158cbead`  
		Last Modified: Tue, 03 Feb 2026 20:39:51 GMT  
		Size: 43.3 MB (43344360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56928c9f7685d113aef731cfc08686ba7ba0b10c7b0f7df32f19e6ec69131674`  
		Last Modified: Tue, 03 Feb 2026 20:39:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:5d943d5a3fb33f32f087518db2d04635eec24135c8527b5efa7c76db0aa0c61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 KB (23063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2165a44f508f4133a21b7012f663a139f1bcba2572fca63c8e33aa856322c22`

```dockerfile
```

-	Layers:
	-	`sha256:63c704f1b143e33a99a29e6b0c332b9ebf8855250c7cb0f06f7e8e53cb32aea5`  
		Last Modified: Tue, 03 Feb 2026 20:39:46 GMT  
		Size: 23.1 KB (23063 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; ppc64le

```console
$ docker pull ruby@sha256:f404c3da8b158cd534e1c60c5242e78f1aa337291b7f278d04a37ae11729837e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.7 MB (79651794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1200acc1e986f3abdc4b82b38fe5a11ff9cbd6592476f9025c374d74a20a312b`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 08:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 08:58:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 09:03:22 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 09:03:22 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 03 Feb 2026 09:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 03 Feb 2026 09:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 03 Feb 2026 09:03:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 09:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 09:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 09:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 09:03:23 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c3d9cb55a066104b1ba7cf09b8f805f3174026efa22e6dd179a5f9eee82c19`  
		Last Modified: Tue, 03 Feb 2026 09:03:42 GMT  
		Size: 3.7 MB (3710783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe566f2a9f2db8460b64aa1fc27eb55a1566d211ca67a8470c61cb12931acbc`  
		Last Modified: Tue, 03 Feb 2026 09:03:42 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600374587f3c7991041a05f1e654606e07c5c49eed036602f3e0fea18fade13b`  
		Last Modified: Tue, 03 Feb 2026 09:03:43 GMT  
		Size: 43.9 MB (43871964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed94a6db53d53fdafc715b3b100721e6105af681fa83968edfbc535dbf9c3acb`  
		Last Modified: Tue, 03 Feb 2026 09:03:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:95d9a42b58b76302814d120878eed94c3821db004c1c84cc0d3e2c1e3cde3084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f12db36d77994e9c18c5aa36e006e0387f8abb5409e91583899ac6c6506c48c9`

```dockerfile
```

-	Layers:
	-	`sha256:06272fe946ef0cd9bcba6e24377b7ef40f5f7297ee2ab4b445f0898b9623ac4b`  
		Last Modified: Tue, 03 Feb 2026 09:03:42 GMT  
		Size: 2.6 MB (2602053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f097927af6340b18b96cc3a849e3b215985defa2f4d8acc11911ce889e820d90`  
		Last Modified: Tue, 03 Feb 2026 09:03:42 GMT  
		Size: 23.3 KB (23254 bytes)  
		MIME: application/vnd.in-toto+json

### `ruby:slim-bookworm` - linux; s390x

```console
$ docker pull ruby@sha256:3d3a587e0dcb7b8930159626e29757e14f8f65c83b4b42bed88b1a8e304e450b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73143285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddff654dc709b1bc6306b432c6f7fc372689b6a438ca70cdefc7567debbb0321`
-	Default Command: `["irb"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:51:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:51:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:54:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:54:08 GMT
ENV RUBY_VERSION=4.0.1
# Tue, 03 Feb 2026 04:54:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/4.0/ruby-4.0.1.tar.xz
# Tue, 03 Feb 2026 04:54:08 GMT
ENV RUBY_DOWNLOAD_SHA256=0531fe57dfdb56bf591620d2450642ea0e0964f3512a6ebee7dc9305de69395f
# Tue, 03 Feb 2026 04:54:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 		${rustArch:+--enable-zjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:54:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:54:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:54:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:54:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:54:08 GMT
CMD ["irb"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f7390ccdb7b4a5def783d284b344e2af5b50fc5823c91432133c471caa8a91`  
		Last Modified: Tue, 03 Feb 2026 04:54:24 GMT  
		Size: 3.2 MB (3171176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fa4002709c72af26203c684e2edc88e622b4001d27f4fa65b9265b5004aceb`  
		Last Modified: Tue, 03 Feb 2026 04:54:24 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a0e0e96d43b79f0230792f367e8c18eb62206c53c07f531636acc41dff4abe`  
		Last Modified: Tue, 03 Feb 2026 04:54:24 GMT  
		Size: 43.1 MB (43087392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e13ed4f217ec7f2380f364b09f7d3369657c28fe73d45d09ba17ffaa42cf5f`  
		Last Modified: Tue, 03 Feb 2026 04:54:24 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ruby:slim-bookworm` - unknown; unknown

```console
$ docker pull ruby@sha256:38e6076881b64334856813b58e847aed30bbf3afdb5bc75680d980eb725d074e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5ccd8897dd8539cf71cee72bb39c0d8efac925934a04cfc2c4805e67633bc8`

```dockerfile
```

-	Layers:
	-	`sha256:cfc5ee54b3c323f8bd4761708f6a6e2979c74c84b83544faa9ec4f2016b10cfa`  
		Last Modified: Tue, 03 Feb 2026 04:54:23 GMT  
		Size: 2.6 MB (2594493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82109765bd1e59f03a6866169dd23649d8954e0b0351d1642abf9b9a7ea25c7a`  
		Last Modified: Tue, 03 Feb 2026 04:54:24 GMT  
		Size: 23.2 KB (23204 bytes)  
		MIME: application/vnd.in-toto+json
