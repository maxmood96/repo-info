## `fluentd:latest`

```console
$ docker pull fluentd@sha256:78d5681c95f5ee5b0580e21df5c85283ad836c6d96efdadeed4ff00f7a0ba8e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `fluentd:latest` - linux; amd64

```console
$ docker pull fluentd@sha256:923e773ac3f9e116e75e7acdc8a3d45b8cb7073eaf868417fdb2215fdc939149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79168923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21659659461b2a27f6738735a7d7285c8c91ffe9da7a4f58504eb79e8d837c79`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:45:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:45:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:47:48 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:47:48 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 00:47:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 00:47:48 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 00:47:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:47:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:47:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:47:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:47:48 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:47:48 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 01:50:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 01:50:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 01:50:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 01:50:28 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 01:50:28 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 01:50:28 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 01:50:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 01:50:28 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 01:50:28 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 01:50:28 GMT
USER fluent
# Tue, 30 Dec 2025 01:50:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 01:50:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3f82d8b2b84a490177071ffba31720bfb49acb0e43e2a998e116c8f9e38177`  
		Last Modified: Tue, 30 Dec 2025 00:48:01 GMT  
		Size: 1.3 MB (1279418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a703fb352b369c2d889461725f817dc3db510690d710f2dcb1e3154aea02273`  
		Last Modified: Tue, 30 Dec 2025 00:48:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1972213005d369f582dce1669fa13c5846a2835ad44233803accb7576a2b960d`  
		Last Modified: Tue, 30 Dec 2025 00:48:05 GMT  
		Size: 42.1 MB (42112330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac039e63a1ea58452045c2b17ecf741eacaa97e6c965346c7d0879b4604332c`  
		Last Modified: Tue, 30 Dec 2025 00:48:01 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a59a96e68ea26f8a02c07149a92aed40db57eb9f88b0a1c64f58488c5c0c8e`  
		Last Modified: Tue, 30 Dec 2025 01:50:50 GMT  
		Size: 6.0 MB (5998243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7d1cf480c8d8d06c8a649157809a80546c1c9520fb0775c1696e780ebd5ffd`  
		Last Modified: Tue, 30 Dec 2025 01:50:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b6326d4fd68deb87dc0f4b7a96b4296a6f527c1ba7716c24003f26e5165f31`  
		Last Modified: Tue, 30 Dec 2025 01:50:41 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d59774943d808d15f913261bd34f3d1f6c1cc17c12714e6e701290caad12104`  
		Last Modified: Tue, 30 Dec 2025 01:50:41 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:ca0e699ea67d957fd008c19bbb07720d96d7b08093a002ed0fc07901e9106dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2d05635d1f157987e8d5f0ae0c07f7d74af15aa8daa3326d8ff439a708c25a`

```dockerfile
```

-	Layers:
	-	`sha256:50cd7fd6d47d480eeee4b3caf578fcc624a0313ed8f4d6c1de98197dd11b4321`  
		Last Modified: Tue, 30 Dec 2025 03:30:17 GMT  
		Size: 2.3 MB (2280105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ee603fb8d25128be7a7558824b32aa9b24c66647e32c4c8aa094ef35d1873f5`  
		Last Modified: Tue, 30 Dec 2025 03:30:17 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:e15abaa2472d8904b5e8f50342d1cb349fe1fbb346cae8d937640dad65ca84b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73015273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b440db1c2c07110c98e5a0b83d68e966226c15b8d05477a21a990a8fda94ae6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:08:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:08:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:11:54 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:11:54 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 01:11:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 01:11:54 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 01:11:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:11:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:11:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:11:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:11:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:11:54 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 02:34:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 02:34:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 02:34:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 02:34:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 02:34:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 02:34:28 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 02:34:28 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 02:34:28 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 02:34:28 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 02:34:28 GMT
USER fluent
# Tue, 30 Dec 2025 02:34:28 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 02:34:28 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e4b1c9b816c636def9d490041218bfbdd3f37dc813c37db0d2b8b4ede4a098`  
		Last Modified: Tue, 30 Dec 2025 01:12:10 GMT  
		Size: 1.3 MB (1263028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:578fd90120971b5e505555ba7e6f8f98c0f8b564a5e006c969c8d8926472b614`  
		Last Modified: Tue, 30 Dec 2025 01:12:10 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d243f50f6bbb9337b25d8788ff3b34a73d494de9f239c2147873c5dada3cde`  
		Last Modified: Tue, 30 Dec 2025 01:12:13 GMT  
		Size: 37.9 MB (37906154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1ef86045bbf0427399d82d8f27ed604a6cbb1c4063360e16ec7995d425532`  
		Last Modified: Tue, 30 Dec 2025 01:12:10 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5d6fe9caf62a1e12e8b0973f661a4dad231a76cb2d51359fe00c3bf740e668`  
		Last Modified: Tue, 30 Dec 2025 02:34:42 GMT  
		Size: 5.9 MB (5899551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a91abb235ef63e97ee0b4ea6692540b554522d12e0a79e2edf60fab66cd9805`  
		Last Modified: Tue, 30 Dec 2025 02:34:41 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84ba4933052d48894132ed3cdcf832bc8e91328cb14b68fe434f295482c15bb`  
		Last Modified: Tue, 30 Dec 2025 02:34:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7de12035509e7a9f636687a83a756a3bb4939aaa73186b96cbbbb76d178cab`  
		Last Modified: Tue, 30 Dec 2025 02:34:54 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:2aa9c1bdf8edc4e1374ea7de70f20e8e4c5c458fe7857afa8e9cca759373f50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59dc6fe167d716603ff44c9e13e714b7900b08c4e96a919e55bbf171aa3cb977`

```dockerfile
```

-	Layers:
	-	`sha256:4040e932b9a44d97f811c9959f5373b436f4dd8bb3debd436ff9fea33dded126`  
		Last Modified: Tue, 30 Dec 2025 03:29:37 GMT  
		Size: 2.3 MB (2283076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9419e23a2d557e681b0130fbf34c91c90342af8fcd72a95b5845376efa824122`  
		Last Modified: Tue, 30 Dec 2025 03:29:38 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f5472345642cb67a58e64c4d36cce46d0e527dd72c2c6509ce80177c515b0e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70882301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270ee110f8f09274841817eae2b9a9e0467404dec1a889e73369e0037ad7715b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:42:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:42:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:45:03 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:45:03 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 01:45:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 01:45:03 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 01:45:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:45:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:45:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:45:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:45:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:45:03 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 02:42:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 02:42:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 02:42:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 02:42:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 02:42:52 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 02:42:52 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 02:42:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 02:42:52 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 02:42:52 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 02:42:52 GMT
USER fluent
# Tue, 30 Dec 2025 02:42:52 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 02:42:52 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb07a57ef2e8915a5c72f33caef6b28df50d1e9339b009d924f19660f1bb47d`  
		Last Modified: Tue, 30 Dec 2025 01:45:19 GMT  
		Size: 1.2 MB (1236528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71818343477bfbb99d507df41c1619d159f6858a5abe20dff04fdf9c4921ec8`  
		Last Modified: Tue, 30 Dec 2025 01:45:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3617adf354ec63e6bbb5e6e0db0b8a51d0b7cc913d9718644c3f0763232f5649`  
		Last Modified: Tue, 30 Dec 2025 01:45:28 GMT  
		Size: 37.8 MB (37767052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9174446788b782c20a045c265edf3b0f78849133e356bc434447451025192747`  
		Last Modified: Tue, 30 Dec 2025 01:45:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae8dd56910f47f90c95fe275d1ad5aa1c45a9254c407722d0bf96a8140afe620`  
		Last Modified: Tue, 30 Dec 2025 02:43:05 GMT  
		Size: 5.7 MB (5666325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b145d7942d82b1dfebaf9a05b1a57c94f9544c7d41e733fa7dca5e07949362`  
		Last Modified: Tue, 30 Dec 2025 02:43:04 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a46bdd39ae39b283ee0a3093c98445f82478d85b6f4de19967dafc64c931de`  
		Last Modified: Tue, 30 Dec 2025 02:43:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc9b61ff65c37d76e0623a0b632640010aa7cdfdcf69fa9f2bebe213259bac0`  
		Last Modified: Tue, 30 Dec 2025 02:43:04 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:838922a1de8989dec73c0201d204ec5faad73c95dacd32558bb1c70c5bc73994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c969920b1cecb7659d2035c306555bb94a95aba9e7cb71acc195a06c6d7757f`

```dockerfile
```

-	Layers:
	-	`sha256:16fe3f756dfce302637f6c59a506597a2cac191514d60c02450e1ba37b22c062`  
		Last Modified: Tue, 30 Dec 2025 03:29:42 GMT  
		Size: 2.3 MB (2281517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de19c72911bc173577f7ae5834185b4ccec4355507405e9011e5bedb5443ffb`  
		Last Modified: Tue, 30 Dec 2025 03:29:43 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:435850e2b1e8390c8b8495393c4aec7013e71bb18d78c484700049348ca6a896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79464489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5038a3bc921af08ecdbaa5a523dd5a66e10af0c54685d87e7004d9455873414`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:50:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:50:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:52:39 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:52:39 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 00:52:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 00:52:39 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 00:52:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:52:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:52:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:52:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:52:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:52:39 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 01:51:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 01:51:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 01:51:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 01:51:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 01:51:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 01:51:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 01:51:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 01:51:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 01:51:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 01:51:42 GMT
USER fluent
# Tue, 30 Dec 2025 01:51:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 01:51:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3183fdb7fc98c15e70d3b6d9ba67ae6e41e2aa929413236db750c4521df9fb53`  
		Last Modified: Tue, 30 Dec 2025 00:52:57 GMT  
		Size: 1.3 MB (1261691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d46ba2a1fdc8652bfd68b538943821d6b4274161d6f8081895d1f283191b89`  
		Last Modified: Tue, 30 Dec 2025 00:52:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649c227e52765cf93de91a72f103ea2acfb301c19b45d79948be43d259df5832`  
		Last Modified: Tue, 30 Dec 2025 00:53:02 GMT  
		Size: 42.1 MB (42073709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf44f0cf00ebed6323c8b8b816a67b124012b8033e58a22342dd419e6f09ae4`  
		Last Modified: Tue, 30 Dec 2025 00:52:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c5b9a7f0fcb50aa73e275718dc9db9fe7d2ab824c03dc255aa0a714e3b969`  
		Last Modified: Tue, 30 Dec 2025 01:51:57 GMT  
		Size: 6.0 MB (5988061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7671ebc840e7d3f9895d16fa580b11741c2d5867f5d97d4fc192192e5b009c`  
		Last Modified: Tue, 30 Dec 2025 01:51:57 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f73180e6c6c19f3322e8ba3a22bd4af8b44678be2362ae6103278247a8d436a`  
		Last Modified: Tue, 30 Dec 2025 01:51:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e1e7b325488647f9a9c550d40b0ce77f83a66162726c7f69d3a8d8fa04bc45`  
		Last Modified: Tue, 30 Dec 2025 01:51:57 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:de146f4594bcbbf8bf83c147a5497f5dabd6f948bf1c6c059c0e417ef0f4e890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a20ab71272838368a5f1c19ebf3c997619168b18fc75693301d7ef1598ac2bbc`

```dockerfile
```

-	Layers:
	-	`sha256:5adf998f234a9e091f72fc97c7cf062649d31a7ab24f5c51ebbce02ab0282302`  
		Last Modified: Tue, 30 Dec 2025 03:30:26 GMT  
		Size: 2.3 MB (2280377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79ae47bf0c76acc419aa37b92fde1a7bca698538525d889b3783b640fa9e7311`  
		Last Modified: Tue, 30 Dec 2025 03:30:27 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:3930ed212b090e53d727d6d93bc8b88b200e425b9debd9da57b49c483ab630c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76211669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cee118df6a054277b1849625d3d1595708c719af3a4d5f221ef7dc8028db20f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:12:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:12:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:15:13 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:15:13 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 00:15:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 00:15:13 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 00:15:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:15:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:15:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:15:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:15:13 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:15:13 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 01:53:39 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 01:53:39 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 01:53:39 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 01:53:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 01:53:39 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 01:53:39 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 01:53:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 01:53:39 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 01:53:39 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 01:53:39 GMT
USER fluent
# Tue, 30 Dec 2025 01:53:39 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 01:53:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975753064198344e755679c6bca60bcbb08ca2e56f29acb58807e3f8edb6c9a0`  
		Last Modified: Tue, 30 Dec 2025 00:15:26 GMT  
		Size: 1.3 MB (1287251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f10a931458cc9a7130fb6bb718473e910babdacba6ef90673a5b81379580285`  
		Last Modified: Tue, 30 Dec 2025 00:15:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc5026ce01a097e7e662cf895ff0b46ddc2f99229b0c12cb2d1f20ce6874e0`  
		Last Modified: Tue, 30 Dec 2025 00:15:31 GMT  
		Size: 37.7 MB (37661245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559e9981cd50892ee03a4c54ff77a588aa9b71fc0d12abcc2abde2dd9794fbb6`  
		Last Modified: Tue, 30 Dec 2025 00:15:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078823d69c2fc322574ce92bdf45aa3591c9ea28afe1dea271e4cb0575ece171`  
		Last Modified: Tue, 30 Dec 2025 01:53:54 GMT  
		Size: 6.0 MB (5967678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17137bde15cdf7d0672a68982bd7fc1aee6ed1537df93d02318e1070c2790260`  
		Last Modified: Tue, 30 Dec 2025 01:53:54 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0e6c82f7557c6fabb3a764d57cc97e5c4fc46ccd2f47f0376cc3ccb3fc6a70`  
		Last Modified: Tue, 30 Dec 2025 01:53:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bca934631f735c03b108413c71f2a36a28fa35170517600b428130e91a27f4b`  
		Last Modified: Tue, 30 Dec 2025 01:53:54 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:94cb1109cc551b2d694c4e6e76ad0802aad5756454567efa680b10eb3e5d383b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80550798fcde479e34c458a454ae148c634a5e29410918b91a81579c7865119`

```dockerfile
```

-	Layers:
	-	`sha256:c1f0a0a0d4fb056fb252b4308bedb76d53956abbd0c1fc6a965f15458f1066fe`  
		Last Modified: Tue, 30 Dec 2025 03:29:49 GMT  
		Size: 2.3 MB (2277293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:472b8c278cf8e18154250feb81441d4188497524bcc843ff68ae2565b0c246a7`  
		Last Modified: Tue, 30 Dec 2025 03:29:50 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:6849b58499b10e0822daa9d246498d3a1491b677ae70ba38140b2c04105fdadf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80958356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3f7281f0f193a6cb59a08d1732c2023ca2834bbaca2d2b3593254b9de2a78dc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 03:34:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 03:34:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:07:00 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:07:00 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:07:00 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:07:00 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:07:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:07:00 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:07:00 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:07:00 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:07:00 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:07:00 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:13:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 21:13:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 21:13:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 21:13:57 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 21:13:57 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 21:13:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 21:13:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 21:13:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 21:13:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 21:13:58 GMT
USER fluent
# Wed, 17 Dec 2025 21:13:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 21:13:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d3671620f3e48336d62a7594d5e2d543d9e64a95aad33bfc1d7771e56acf03`  
		Last Modified: Tue, 09 Dec 2025 03:40:15 GMT  
		Size: 1.3 MB (1309685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f018d664c90820e92e1c9763e0ff1c2d9fac0edb7ffc1e2324b238098d157eac`  
		Last Modified: Tue, 09 Dec 2025 03:40:15 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66763531391a834e433e9229e39be412ba7d793e4fdaead743792c8e781dde7`  
		Last Modified: Wed, 17 Dec 2025 20:07:31 GMT  
		Size: 39.5 MB (39535315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91219609dfc8fb19e3729ba74e82c665165badd8ba34d4c525d8f0f5a42c62f`  
		Last Modified: Wed, 17 Dec 2025 20:07:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7f80c50d0aeb50968f7fc4773f4acb9a70d70127b323c731ff47910dab8ec`  
		Last Modified: Wed, 17 Dec 2025 21:14:37 GMT  
		Size: 6.5 MB (6514075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191e384147b65c34f1190a3741221d6b18de16986418f782b3fda420e291c662`  
		Last Modified: Wed, 17 Dec 2025 21:14:37 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d713361ed7e1fdbc59dd668a553e4972af352071ee75b7cb2a22cecd53afdc`  
		Last Modified: Wed, 17 Dec 2025 21:14:36 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86886b11cd41b0fa1d95b298b55cfe624158653ffa720770ab2482eb7e632bda`  
		Last Modified: Wed, 17 Dec 2025 21:14:37 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:968fe310c511c91c26566ef573b38fc6c37c4cb6f2754b641a8f17fe3589afbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6843e9c3d28dc11561aa1c2fbd8fdecb778bd0a628d61359f8d9aeb3a553e610`

```dockerfile
```

-	Layers:
	-	`sha256:0d70c5c43c91cba5eabd4a501ae6d91095615a948958b2e4cee68ef22490bfbb`  
		Last Modified: Thu, 18 Dec 2025 00:29:04 GMT  
		Size: 2.3 MB (2283640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7e39eb480011e2b1128d639347abd6704bad78583ab34585fd8cca353b7eca`  
		Last Modified: Thu, 18 Dec 2025 00:29:05 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:def22b68057e3ff27ecde8b8bc630f9d8b578871268494016e1ce694609815af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76695433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43022f046804104ac7304dedd3078e11b557ef09461b957ee3a6165f8dcb8529`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:51:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:51:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:54:32 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:54:32 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 01:54:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 01:54:32 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 01:54:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:54:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:54:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:54:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:54:32 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:54:32 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 03:05:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 03:05:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 03:05:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 03:05:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 03:05:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 03:05:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 03:05:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 03:05:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 03:05:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 03:05:23 GMT
USER fluent
# Tue, 30 Dec 2025 03:05:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 03:05:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a528b2a04b7b80b3dca8fec03ae0226090a72c259b8b26c3d3a0f00e3a453d44`  
		Last Modified: Tue, 30 Dec 2025 01:54:53 GMT  
		Size: 1.3 MB (1294295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd038b1b9ae71af581e559fd993f6882a7668a8436c8b057e891d7a70de00254`  
		Last Modified: Tue, 30 Dec 2025 01:54:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5450a5305d6d984f587ab8d21fccddc17cf3239699b76c0f998eee48668150`  
		Last Modified: Tue, 30 Dec 2025 01:54:55 GMT  
		Size: 39.2 MB (39190881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e2ba3d00bfb2a08536b2ff4538ae7140a71b541e47e87bd6f679540be9119b`  
		Last Modified: Tue, 30 Dec 2025 01:54:52 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7f3b3d046434d53ecf4b21455a93c55db875eddbe1784a0f03c40af37c6bf3`  
		Last Modified: Tue, 30 Dec 2025 03:05:43 GMT  
		Size: 6.4 MB (6373446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18017d4010740c3024c6761f71605640d28eb4055f49adf3734bbcaf89a20762`  
		Last Modified: Tue, 30 Dec 2025 03:05:42 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb98f48c409ae413a3ae5ddfed1258b38cc6581bb3bcdfb71098d5c9caa79cfd`  
		Last Modified: Tue, 30 Dec 2025 03:05:42 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7513d97cb970254ade08d48d0bcce67851d9318011fe027c43e4d3aa7fa7d94`  
		Last Modified: Tue, 30 Dec 2025 03:05:42 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:471476bb199636c0ec9af23ad4358f695b4133ad2e0372a109f42ab656dde406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ad18dfc732194216c97bed7bde81a15c511b96c061360cbfde4b14af815e8e2`

```dockerfile
```

-	Layers:
	-	`sha256:72d9b8f70b8adc7c743d315d89b1b7c26735125853efefe378267836d297063d`  
		Last Modified: Tue, 30 Dec 2025 03:29:58 GMT  
		Size: 2.3 MB (2281550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f87a3f20bb60a60c5e48ef1f376d0ddcf27c8ec30e8c2767107edf23d6d45d6`  
		Last Modified: Tue, 30 Dec 2025 03:29:59 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
