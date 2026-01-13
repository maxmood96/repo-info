<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.11-debian-1.0`](#fluentdv11611-debian-10)
-	[`fluentd:v1.19-1`](#fluentdv119-1)
-	[`fluentd:v1.19-debian-1`](#fluentdv119-debian-1)
-	[`fluentd:v1.19.0-1.0`](#fluentdv1190-10)
-	[`fluentd:v1.19.1-debian-1.0`](#fluentdv1191-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:d3aa191d6f942c95058b251fb8e58db6afe19316a4f4b0a3ed70f3e6313af9f0
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
$ docker pull fluentd@sha256:3bcde99e3687abecf27e8212ee5c19f0438469a5ddb314883fa63d5008311b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79169074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437e7a69cd621f6ebc46e4a9a1d50a934a36bacf8a69b345d7bddf67175aaa4d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:15:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:17:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:17:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:17:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:17:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:59:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:59:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:59:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:59:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:59:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:59:58 GMT
USER fluent
# Tue, 13 Jan 2026 04:59:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:59:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eef9b8933028d4d086fca9528ccc9271c5f7c65abfa73e952107ef4e71f5b`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 1.3 MB (1279374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef44c7bbb15316ed3c8b90e1149e7e65006f6a352bfbc150f83ba34cf36b8f0`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d36f3a5655a63fccdac1be1dea43008bf13f50700604d5bbb51dfd67c4f1`  
		Last Modified: Tue, 13 Jan 2026 03:17:34 GMT  
		Size: 42.1 MB (42112593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403786353912e853ee3b03de8484cf9cb0c6a860807846ff07bb720943ad0cc2`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95a20976cd45bd6c70aafe68db5deac22d7041dcc4332f23f4371cfb918ba2`  
		Last Modified: Tue, 13 Jan 2026 05:00:25 GMT  
		Size: 6.0 MB (6001029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532f021056a355ffebc964ee6e349fc264a0ffdabb2e14ec25a50f2b008efe2`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8358e169dbb7ee057d2e5fe1001b6db5516639c6e88ed047dca2a65dfb01d`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988474eade660a7633fbfdad69c9a561ab991db1686c4ea44d2227977121d7`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:40742be2e1f215c37553c2e750818bedea348558eef163d65e00231896a7e4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247793a0a9928ab02b7e2013c0ae4ec3be4b506c0db291830b3dfe73be1323fc`

```dockerfile
```

-	Layers:
	-	`sha256:96f7d5ffebc16796703f3e1508ef6ed1867ff28f62d4ef6faf52f9f426b28892`  
		Last Modified: Tue, 13 Jan 2026 06:30:07 GMT  
		Size: 2.3 MB (2280167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d245ee90fda65ffc9ff75c6931bfb574b96d405448a7215873c5367f08bad`  
		Last Modified: Tue, 13 Jan 2026 06:30:07 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:f52d517870022f9ed7bffb4772dc8a2588760749e6605719195dcc85199a2d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73015490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05859ae973b197cc8a0246f09dcf7bea6bf454bb4ce55ee0ed5176fe0da576ac`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:23:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:26:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:38:08 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:38:08 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:38:08 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:38:08 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:38:08 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:38:08 GMT
USER fluent
# Tue, 13 Jan 2026 04:38:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:38:08 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1320c956f4c83fcb0562b315b8bda5dd174609e7d7ca750c0c5b25757c3a4e39`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 1.3 MB (1263009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4536c4a4c2b9a4b25706298eea75e411ecf7474ec825e95487a3fc45677109b`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6673c3e63216c5e4ec98fc85dddea075baddb32362e818e7ce47e7028fc26574`  
		Last Modified: Tue, 13 Jan 2026 03:26:50 GMT  
		Size: 37.9 MB (37905868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0676e2edb97826a7240b8e67fa4464779b809420476b9a092842c95228a68c2`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e667d8c88075d8402d7e8e9d1c8a2e8d83d266277342528ad7324ce3d65eeb0a`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 5.9 MB (5901500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f0bd7482758a351bf2332fce7368df03d0fcd8fd2536fc8d4411ab00f82d04`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0417fc24ae33338c26093691d99cba4dc63c357664c86f9865b640d4718c7f`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ea0521b7ac5a88ea214f2aee9f3572ab1b928e8ec982413f551b5550b8d30c`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:b4949c17a66864f5b759d52baf0b5b56262328a7c5e00cb36f1b18651a3d1501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37f234ef4b0e2b6bc356defd5465da1e3f4900dab4f8d0d0f5ae950c385e12`

```dockerfile
```

-	Layers:
	-	`sha256:3de1fffa2b8ba00ff71bab251fe6d3cb80c93072d51e7b0f66fc50ba8d862863`  
		Last Modified: Tue, 13 Jan 2026 06:30:11 GMT  
		Size: 2.3 MB (2283138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a727fbbb6584143a529944a5a01d6a0f141ad05ecbf2c84f7030bb180513cf89`  
		Last Modified: Tue, 13 Jan 2026 06:30:12 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:d11673dae75290f1512772fbf2fccf20f343e5f35200b7242c5d64461cf9c7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70883874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012e252ef68a7d2d9e65f9bd3e732c7a7a77c480ac76e2c262b317e71e3f404d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 04:01:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:01:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 04:03:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 04:03:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 04:03:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:03:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:52:53 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:52:53 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:52:53 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:52:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:52:53 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:52:53 GMT
USER fluent
# Tue, 13 Jan 2026 04:52:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:52:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb89ad4eba0f6c13ed221ba61cd63256963a2ae6022c5eb1a90dfe213d338e`  
		Last Modified: Tue, 13 Jan 2026 04:04:17 GMT  
		Size: 1.2 MB (1236555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4524518ebfe925ff0ba895a410f351e2ee7d22045883650d8b7fac782a9cc4c`  
		Last Modified: Tue, 13 Jan 2026 04:04:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafc5c289841a0fbb484e454157cfd1cd3e738994188089f928286b34c74f8`  
		Last Modified: Tue, 13 Jan 2026 04:04:25 GMT  
		Size: 37.8 MB (37767155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c4e1fbfecc70f8903b4522859b5ef39a5906274e2351951079ed8f886585`  
		Last Modified: Tue, 13 Jan 2026 04:04:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7740d7e2c777411352b0085fe0094c95668acdde8c6ece31de343123a5cf9`  
		Last Modified: Tue, 13 Jan 2026 04:53:08 GMT  
		Size: 5.7 MB (5669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2b431fd4058cc969b8cbb21b31aacdf5b6c415776385b9bd855de095a86be`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0486e503a316218c72159c4aecfd966c0227bea5022343f9e65a9bab48e9a294`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a8b50351ca059aa0d8b903508c9a57aa8984f21e7a73c28431739b765cabf`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:28ce653f313504add74d6ae0ea8a60b536b728cce10f717c1b3b6b702df1a407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d63c54bd63cbb3caddc547142ff8e84bd64af8fa85b87fb1ad06e91d13c95c6`

```dockerfile
```

-	Layers:
	-	`sha256:1af10659db7793cb979bd306619dc8928e9299489553158805ffbdb212d7cabc`  
		Last Modified: Tue, 13 Jan 2026 06:30:16 GMT  
		Size: 2.3 MB (2281579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37545b709467be88ec29e37388b144288be9462833e3cab824fdb247fc368901`  
		Last Modified: Tue, 13 Jan 2026 06:30:17 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2ba5ac0282f0a65ad95fc63a472a55621f2f4b0fcb0e0ce1160034733c471471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79461765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a54308eb52c307d090b75de044c8eb95213037450e55a4d504e551dd7a804bc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:23:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:26:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 05:01:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 05:01:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 05:01:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 05:01:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 05:01:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 05:01:38 GMT
USER fluent
# Tue, 13 Jan 2026 05:01:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 05:01:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0525c3d775730a255f13515eebc27444890213cd946823934e1e349ebf85d`  
		Last Modified: Tue, 13 Jan 2026 03:26:18 GMT  
		Size: 1.3 MB (1261687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afe863bf626435a4acc6286e46071f69c3c80a6a559f73494d100c77e2a459f`  
		Last Modified: Tue, 13 Jan 2026 03:25:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505e6a88accd972129dcba73d3823653527e349b86bd85b23d7be05e6b7d131e`  
		Last Modified: Tue, 13 Jan 2026 03:26:20 GMT  
		Size: 42.1 MB (42074273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12087ea894d19fc0f651859b919a840ad2d733574392ff2bab6decc744d11ee`  
		Last Modified: Tue, 13 Jan 2026 03:26:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42466d7a4e7c4317a6aca126263010a1f5d4cbf475285844859615e6f8647cbc`  
		Last Modified: Tue, 13 Jan 2026 05:01:55 GMT  
		Size: 6.0 MB (5989373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd395c404a6148260abf43c4fc068f0b8cc16e4f0cc22e7e47f0d6861db9ec0c`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228cea3da2223620ff60c397a125f567c560bfabe61226b0b0a4ca0ee4e995a4`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423f136b4f2f4082396887c88c937d76864d24d7c3520bff51d342355d459f2a`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:58ac976c6818af47fcc251821f582953708800364f8645c8c20db42650b6079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e553d3d1f1c6af6ffd1dbbc3cd00eddcf89a9244856d490e67448175ad2ae0cd`

```dockerfile
```

-	Layers:
	-	`sha256:c881d4ff0b96d3adb92b3f5d51324cd3000d2b17891c26d2344509210b0055c5`  
		Last Modified: Tue, 13 Jan 2026 06:30:21 GMT  
		Size: 2.3 MB (2280439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac4b52effa78caa2eaab59f393d2747368a2723ded9da3da8999144a067da91`  
		Last Modified: Tue, 13 Jan 2026 06:30:21 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:90a276a23933880908550e3b249d0636588803070ad0cc3125c0650c1798c07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76209821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb7f8b78264676135dfddc1a5a8ea25db76afae7125f39945e3b100ac88217`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 02:49:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 02:49:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 02:49:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:49:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:00:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:00:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:00:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:00:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:00:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:00:27 GMT
USER fluent
# Tue, 13 Jan 2026 04:00:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:00:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca9739d6b026ec1d4cd350482fedc4374621d2428ab77e18051bdb8ca6c93a`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 1.3 MB (1287208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf308c9322d7b7ccb72a3b032126ea9174c0dd19d5133f792f459c5f0fec63`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077996a21b00611176c639502288dd2a7a31e063ef348d46a1652665d276aa0`  
		Last Modified: Tue, 13 Jan 2026 02:49:43 GMT  
		Size: 37.7 MB (37661435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f373e260e56fe68e120ff78469b633199ef4d7e6980f6c1706b0628c090ec`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b70dc93001436daee4f4c2269d3b473cc83687fd15af6b3b65b15d67a592ad`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 6.0 MB (5970309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64083097cffea937936c9ec17bfa648c81bbc71f8d05d684b7afb9e52a48d5c5`  
		Last Modified: Tue, 13 Jan 2026 04:01:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5966fa1c56255ac85fd3cda423eb24e7808ebd4ca2f9f0ea681e3e09bfc34`  
		Last Modified: Tue, 13 Jan 2026 04:00:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefc55a043cc735826153c6bbcbc2f26bc3b8b365fb9dd174493eeb4c568d44`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:4dcfb61e511dc10991bc33f42e5660fc254fc795b9f1364f8f111b6a050be002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e6add496a0ab66cc6edaaa2ce6ffb23a10a39d16e78f5a6362f09a674985c2`

```dockerfile
```

-	Layers:
	-	`sha256:eea3a0edad86e0c342eb31d911134cbbf7295ec64067fb3bbfd4a1d860ccf606`  
		Last Modified: Tue, 13 Jan 2026 06:30:25 GMT  
		Size: 2.3 MB (2277355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0ea0b7db35baa06510b1a0264df2ddf0c3651935cfe0f32813ad862ea1efe8`  
		Last Modified: Tue, 13 Jan 2026 06:30:26 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:d3adf405db172cdb0926246543a6512e24c94c39d2c8f8fa6de24b4f4230f417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80942262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e134450b5ea6ce9b16abc2e430bd5deb9bcb6dbb166e9f8d53d29fdbad29a2c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 18:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 18:53:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 18:57:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 18:57:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 18:57:58 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 21:20:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 21:20:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 21:20:29 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 21:20:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 21:20:30 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 21:20:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 21:20:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 21:20:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 21:20:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 21:20:31 GMT
USER fluent
# Tue, 30 Dec 2025 21:20:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 21:20:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec427cb0f29aa78b3a35043f5c43e0a07e16cba482febff3fe2087900b8e01`  
		Last Modified: Tue, 30 Dec 2025 18:58:40 GMT  
		Size: 1.3 MB (1309698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119f3f7815c4977fbb7b151b6aaa8cf695081c5e63a241e7e8ccfa7cff83fcb`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6841342fbfd6bcc1a592039fcb307930a186477e89093dcc569ddb52f69b663`  
		Last Modified: Tue, 30 Dec 2025 18:58:42 GMT  
		Size: 39.5 MB (39519497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ecf017368e45fae8cb085ed7b4384c0e98da8232a690f0b6c1dffc3a99bb0`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c06a5efcd7af94fd4a7d702dddc472d60cb22b1ed26f26cf4b421e3c32f3f7f`  
		Last Modified: Tue, 30 Dec 2025 21:20:58 GMT  
		Size: 6.5 MB (6513782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d35286b4d75cd4ff6451e45864c1d79e0f811e301fe3b34540241af0a87d8`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534390e158cdb1f91f722d150993c5cd591cbefdc5b40262115b84a4c1977fe2`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1185bfeb67fbda08aa3f66a4c34eea27c0cf23ca82c32fb778f16b994d79f43`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:2dfeb20c2fabcf019f75db5cb34b6d87d224cc95c8faad30eadc12a2d3cd89de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa85e5209179c6f949d0f2a73450f2b6a987ac9db17c829dac828f742025461`

```dockerfile
```

-	Layers:
	-	`sha256:44270606ed9db02298dbbf78bd7ae9bd926994714d651d08aa9afeca92bf8afa`  
		Last Modified: Wed, 31 Dec 2025 00:28:36 GMT  
		Size: 2.3 MB (2283640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ad2156a8f759a86af16633a4b90867f271a588d55694eccc556442f519404e`  
		Last Modified: Wed, 31 Dec 2025 00:28:37 GMT  
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

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:e057ae4394891d05553f8f040120efa5a4fd26d609cfc1a1f999c76301444f4e
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

### `fluentd:v1.16-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:d15b9c90ac2a6ac29ef0c3c06848d1b519df8462f40d0a16d6f121eec1cfe5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82040699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497bb0f8d4ec539229975e2d2275491fa7d58c606138313431c6f7d5ebfa7dcf`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:16:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:18:38 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:18:38 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 03:18:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 03:18:38 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 03:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:18:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:18:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:18:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:18:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:18:39 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:59:53 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:59:53 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 04:59:53 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 04:59:53 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 04:59:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:59:53 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:59:53 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:59:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:59:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:59:53 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:59:53 GMT
USER fluent
# Tue, 13 Jan 2026 04:59:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:59:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c867442486918ea68669aaa91486e4d57f173e10338d29984bb7a3536def8980`  
		Last Modified: Tue, 13 Jan 2026 03:18:54 GMT  
		Size: 3.5 MB (3509989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81715e94d1f88b8e1e42543f96730089821036d553a5e66c7b1b9cccd04c237`  
		Last Modified: Tue, 13 Jan 2026 03:18:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7da126231fdb147109b8a01b94590f110ca11094acb20f9ca5f19e80c308834`  
		Last Modified: Tue, 13 Jan 2026 03:18:57 GMT  
		Size: 36.0 MB (36008302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3c7e1c54cfffb4572a0fcafd2707ca0743a3173320aba622c048a09f96927`  
		Last Modified: Tue, 13 Jan 2026 03:18:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02dbe4e965cfc3107ade9d62fc09fd73c4daf29ce14ecd2cc2af5522cf6aa3`  
		Last Modified: Tue, 13 Jan 2026 05:00:18 GMT  
		Size: 14.3 MB (14291444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7698fceb111af8f2ba206f8c9249d2eb1adce2686da7ae4aa475e17fc36e1`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed049f2443b53eb7ac79df20380364b7ce65f598c3abf845f201fd75f732db`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9936110fa45e61a00821872dbcce32d1c164c1715958c692a7b9f72c2a44761d`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:42d52a363c2cd32b4bb2348ffaa2a9060f21a5a2c81fc37123484a0c25effcd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f38231ef96de83694b4d18a8ba9cf22fb13535d1e3945d8b8cf3c0a9c28949`

```dockerfile
```

-	Layers:
	-	`sha256:791507e35d202e02f466befc4fcc91e9f9a0c48aede1cdd1144cbddacf819186`  
		Last Modified: Tue, 13 Jan 2026 06:30:31 GMT  
		Size: 2.7 MB (2671032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3dfbc135922bc2fa1c7c068557473f6053b2e1fdf1b0e9c0ca81ac081c0cf0`  
		Last Modified: Tue, 13 Jan 2026 06:30:31 GMT  
		Size: 21.1 KB (21068 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:51678e3f051d85416c3191027ace27d50915fd179d32977e22a75420a5c2acaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75438707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec403e5730f92e3997cc1a347f9807e038c267b3a82614bc4c9d1434563a2ae0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:26:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:26:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:28:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:28:53 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 03:28:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 03:28:53 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 03:28:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:28:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:28:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:28:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:28:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:28:54 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:37:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:37:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 04:37:10 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 04:37:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 04:37:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:37:10 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:37:10 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:37:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:37:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:37:10 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:37:10 GMT
USER fluent
# Tue, 13 Jan 2026 04:37:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:37:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:43595593b17008d0147d9ea53c9ed04f4ec8fde216c1d359e2de9daa9e0665f6`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 25.8 MB (25757697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea68f8d639671ff68dce83d136086909a58ff5957c1c4424f23dba509ab8929`  
		Last Modified: Tue, 13 Jan 2026 03:29:09 GMT  
		Size: 3.1 MB (3080686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e164755af9df33311e54ac8f585cb4f4c2beb5588d89239bce20804932bf7795`  
		Last Modified: Tue, 13 Jan 2026 03:29:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad923f0512d30e9f82cf7712fe08ebd11be1840b4a7428489110aaeb27e9ab6`  
		Last Modified: Tue, 13 Jan 2026 03:29:11 GMT  
		Size: 32.3 MB (32328081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b206d4be1faa9c91b9a00ac65c10bb859908a1c44be33c29ddbbcd42a1f4b5c5`  
		Last Modified: Tue, 13 Jan 2026 03:29:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ff4d29e2aad90863fea8c8544717c5b323288983f47e1cd9d980dbedb1841`  
		Last Modified: Tue, 13 Jan 2026 04:37:27 GMT  
		Size: 14.3 MB (14269853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a852f86141bc67ee84471b8afe9dd4e2c6e4cf00d355659584637bae65e913`  
		Last Modified: Tue, 13 Jan 2026 04:37:25 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3264bb23f61f6c26e1fd25fea3b67d990508b78b44e8592cd62ef2f952154fb9`  
		Last Modified: Tue, 13 Jan 2026 04:37:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ee7f145c0fb22f8b3c8b02363e97567ffb2c375b4d960d5bfc55ce5e5b2ffd`  
		Last Modified: Tue, 13 Jan 2026 04:37:25 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2489180e804fac08a1c877a85c5227122a6e2d178fa651a9416a62ed4d5b2db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d548c0c7d3f0b618c20a8a3f273ad32aca8b02862d4a5b385fc5258d31ced12`

```dockerfile
```

-	Layers:
	-	`sha256:c43ac698ebb599d4fa1c6230fb5fb639d59ef5ff39ee0e0fb577b7060d5a4ffa`  
		Last Modified: Tue, 13 Jan 2026 06:30:35 GMT  
		Size: 2.7 MB (2674827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946ed5ba4e6e00b56cd9447b8f5cbd9d39e7e3d90f3bbe22b71c27a76e825c01`  
		Last Modified: Tue, 13 Jan 2026 06:30:36 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:1fd208bb9af259f4110de6cd26e308e96340a89db992e4dd6743ce37c1212c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73212919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3a829a5f75b0282562b0f72d1bddeaefae6b40d513952e0c4787f741ea4927`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 04:02:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:02:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 04:04:29 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:04:29 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 04:04:29 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 04:04:29 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 04:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 04:04:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 04:04:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 04:04:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:04:29 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 04:04:29 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:52:37 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:52:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 04:52:37 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 04:52:37 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 04:52:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:52:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:52:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:52:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:52:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:52:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:52:38 GMT
USER fluent
# Tue, 13 Jan 2026 04:52:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:52:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d56538f5372345b89edb9cd7f69785f059e689e1ec75c9f857831b903d4e5`  
		Last Modified: Tue, 13 Jan 2026 04:04:46 GMT  
		Size: 2.9 MB (2913529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d87fb932f0dc243377dc90b97d38a1ec5eae15cc624bc03054bb0d2064bbc8`  
		Last Modified: Tue, 13 Jan 2026 04:04:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76f28198b3321c896e5c8e4c74a535de1a9eeab19dcb65685938796fcdc43e6`  
		Last Modified: Tue, 13 Jan 2026 04:04:48 GMT  
		Size: 32.2 MB (32164038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2a883f21bae6d75ef1ff2d48ec47ff0ab114698a7ea49a603ac618ea1a925`  
		Last Modified: Tue, 13 Jan 2026 04:04:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d23e82d902e26b770ddeae77134efbbf9813b0d1d87cef0595f67890ae39e7e`  
		Last Modified: Tue, 13 Jan 2026 04:52:55 GMT  
		Size: 14.2 MB (14198838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9a4d8443083883f985b84364e9464aa62dfbcadd285dc27a6f083d63790f80`  
		Last Modified: Tue, 13 Jan 2026 04:52:52 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b500b4431caacbe51d6d7fd49c47f0888b9ce6bd71c04dd86ae9228d562470a6`  
		Last Modified: Tue, 13 Jan 2026 04:52:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f7c1bdb18920fd7d5e97d7503e7a2523c66229a5f402f57f8adea0e3583ae`  
		Last Modified: Tue, 13 Jan 2026 04:52:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:789c34c60fffeb59c7d58232e1ffe80dae65f53ebf054a56d6b9338733c6b5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d15ffe924e5c6d796ee5967e575c1bdfd7ace064351e003ca3c2c64d3e87305`

```dockerfile
```

-	Layers:
	-	`sha256:44b0474111486de1dea1bb5d31bfbada4eac4f1fa2d440318b3c7ec08edfe273`  
		Last Modified: Tue, 13 Jan 2026 06:30:40 GMT  
		Size: 2.7 MB (2673258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2ead36bc243d61d33100516a0bcc86d90c7ee251b498f2ddfb5fdb44186b3d`  
		Last Modified: Tue, 13 Jan 2026 06:30:41 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:d4d7668eec7debbb16ddfd5fd30a0ad8e6135016c3ae4914a98a6d6148eb9dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81659010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3feacef73f69390fb9fd1c5ef8cc294ecfe64f93f4992974230fef6944537f9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:23:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:23:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:25:58 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:25:58 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 03:25:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 03:25:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 03:25:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:25:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:25:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:25:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:25:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:25:58 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 05:01:46 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 05:01:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 05:01:46 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 05:01:46 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 05:01:46 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 05:01:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 05:01:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 05:01:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 05:01:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 05:01:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 05:01:46 GMT
USER fluent
# Tue, 13 Jan 2026 05:01:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 05:01:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958b8dd8e23755aaefa85b99db1d889e2074dd250cad0466d545393efd097bce`  
		Last Modified: Tue, 13 Jan 2026 03:26:15 GMT  
		Size: 3.3 MB (3341737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa4f687c57629cc566697ca61b0e02bacb8b263b8296dac609cd2b83586c5c`  
		Last Modified: Tue, 13 Jan 2026 03:26:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc3167b0828ba135d00ac7fdd2f23f1673e33aff953d3049d391d81c3642c7d`  
		Last Modified: Tue, 13 Jan 2026 03:26:17 GMT  
		Size: 35.9 MB (35909290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e402e2a753f9e159e1383396df4d880e246b96cf1ce3303e83bdd1c5cb2f9a`  
		Last Modified: Tue, 13 Jan 2026 03:26:14 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7780af10fbf5b79e40b3b17b5f2ee696d4f834469e08733d4a3e730c5bf12c`  
		Last Modified: Tue, 13 Jan 2026 05:02:03 GMT  
		Size: 14.3 MB (14297702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d5b50a4603ee1ee9fa643909293517f2bb43d575578c1e274981a1c22a5ad5`  
		Last Modified: Tue, 13 Jan 2026 05:02:02 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2a5d1023f1a9e7c96e0900fc0d668c54702c1cbd09026cbd1d88f022c6ef35`  
		Last Modified: Tue, 13 Jan 2026 05:02:02 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae4ca798439d0b2a8ca5c19b825f47a834362150d503b45943fb734a01b36de`  
		Last Modified: Tue, 13 Jan 2026 05:02:02 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:71563cf244ba181c1c20ea38aced23fdbac379d85ea1b358b6f3e6a2517491d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf114ba8b47bdfa5d4a58459a10cb7ca723e4eeee30e33140055761a3ec55dd`

```dockerfile
```

-	Layers:
	-	`sha256:7cac6a4413f038c133b0a2f6114b3c7850dbc38a226ce83bb4f7b89de674431d`  
		Last Modified: Tue, 13 Jan 2026 06:30:45 GMT  
		Size: 2.7 MB (2671272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6765faaef1795747ebe1d5fbc15220e29065b55ffdc951a1c19bd9f19301f83`  
		Last Modified: Tue, 13 Jan 2026 06:30:46 GMT  
		Size: 21.2 KB (21163 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:c35bf73ea8000c3b093f04a8040460b08eb014dbca81d4ae2468675c15ee6bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78965873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3a26c2eb7f93ddc68c72c2c41673b190500ba69cb15424b5010fb300f00ddc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:47:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:47:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 02:50:03 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:50:03 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 02:50:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 02:50:03 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 02:50:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 02:50:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 02:50:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 02:50:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:50:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 02:50:03 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:00:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:00:31 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 04:00:31 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 04:00:31 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 04:00:31 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:00:31 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:00:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:00:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:00:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:00:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:00:31 GMT
USER fluent
# Tue, 13 Jan 2026 04:00:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:00:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:45 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee0c6efab824f716683c3690cc0e16b2f865a123d24b5b015faaa5e7cdd2e3`  
		Last Modified: Tue, 13 Jan 2026 02:50:19 GMT  
		Size: 3.5 MB (3512239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf28144f4a1147bda31ee6657575807b7a418b220243bb3a754bf210b4042d7`  
		Last Modified: Tue, 13 Jan 2026 02:50:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41686bade84f460dca8dd3dfb9a0105001e23cf8c9ef69ee3a633a74860e76e`  
		Last Modified: Tue, 13 Jan 2026 02:50:22 GMT  
		Size: 32.2 MB (32160036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b888d579ad5fe0d15bc72ac04ebd51e2bc1745bbd24f34cb48bac755fe7806`  
		Last Modified: Tue, 13 Jan 2026 02:50:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68f2e38d0b7df1fc95d9d6744ec65f1707efc7bb6a4a853d774910a98f73bf3`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 14.1 MB (14081141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ebd2a4b35dc3c3bc81b28cea13f92479297e0b09df0c20ff9bf5040bc527f0`  
		Last Modified: Tue, 13 Jan 2026 04:00:47 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d98d0e0139ae2ef068637297aa55a8eb7c3b779c75029d6fb1c3ecb72ae75`  
		Last Modified: Tue, 13 Jan 2026 04:00:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf23808d3611a1c489f5dc573a03a73069588d8cd0004c530f52e70b14056b1`  
		Last Modified: Tue, 13 Jan 2026 04:00:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:81bf17962ee658c140e1585ca6b205054730be47e0942cbadeb3463078c91005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0eb5fed5e7ae777066f3f18dd5f9348f61d862d5ce5cca39caf6ed2f616796e`

```dockerfile
```

-	Layers:
	-	`sha256:607939948a2e2428e615301ee2d3ec8328bfde9c12a141534eef4268a27b4cbd`  
		Last Modified: Tue, 13 Jan 2026 06:30:52 GMT  
		Size: 2.7 MB (2668211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d43cd07a49f975797eed668d10c28a041e348e25aa1e5374cebe6684d70349`  
		Last Modified: Tue, 13 Jan 2026 06:30:52 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:21d9c93229b70e222730b89a18d20fd3008cce81db02fec3d4352c042dfa1006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84298660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9a88d2b40bf3d6feb0868ee8fc0f97396472266d1c3b0f6d132dd2d9f83aa8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 04:57:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:57:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 05:11:49 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 05:11:49 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 05:11:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 05:11:49 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 05:11:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 05:11:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 05:11:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 05:11:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:11:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 05:11:49 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 08:53:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 08:53:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 08:53:25 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 08:53:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 08:53:26 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 08:53:26 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 08:53:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 08:53:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 08:53:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 08:53:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 08:53:27 GMT
USER fluent
# Tue, 30 Dec 2025 08:53:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 08:53:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9cebfd28c842195ef306457f689bf8cbec529ccf65729ab7749cf1505623f`  
		Last Modified: Tue, 30 Dec 2025 05:02:13 GMT  
		Size: 3.7 MB (3709070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a333055b244abc340531d6bf67be5e762ede7cc94d700c3a3bd170892ea00113`  
		Last Modified: Tue, 30 Dec 2025 05:02:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e386747298c411ef446c44b05925fcca2e6ee47e039f8608eb84ce4428a5c9d5`  
		Last Modified: Tue, 30 Dec 2025 05:12:18 GMT  
		Size: 33.8 MB (33832992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d894c7df1e0acbf3b7cbc7f42df580787a6cc196eb3535767a153975936125`  
		Last Modified: Tue, 30 Dec 2025 05:12:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca20d39404859ce3688f8951597ef3168ad8870943c5221d01605bf899e7fce`  
		Last Modified: Tue, 30 Dec 2025 08:53:58 GMT  
		Size: 14.7 MB (14685361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1adbdec974ea4246009f77b918df3a820d275dda5aa24b8d7f0e33b6071453`  
		Last Modified: Tue, 30 Dec 2025 08:53:56 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1562f97b4c32aef274d3b6a579fda7832834b940897245947914012df963d3`  
		Last Modified: Tue, 30 Dec 2025 08:53:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eaff77d7a86a19b41d23de29eafb3a887ec0627dcbbdbabc2d6bc3b9b06830`  
		Last Modified: Tue, 30 Dec 2025 08:53:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:287589312a9ce169b781a03d28b2832f8c17310d1cbf23a39afaf5f37a9a985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220486435be460cddba1a1098c09f9b0999ba2011fa12d1edad2ae3c6641a418`

```dockerfile
```

-	Layers:
	-	`sha256:d84b5217c8bc0f4970ec0bbf64e27886eebff2dd0aa6a551c348838402b71ba4`  
		Last Modified: Tue, 30 Dec 2025 09:28:38 GMT  
		Size: 2.7 MB (2675439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30abf1c9149a2f912678403135c814450e872f1e1c901ad5f43f9a82caad0cd7`  
		Last Modified: Tue, 30 Dec 2025 09:28:38 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:61ce2c2ed097ee6dda79508430e8f2f72dec03d2dbb45352dbbce98513583f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6ec814751f6e7f4a5d6655c1ba62c00bc4ba56029989ad7b3d7741adf126b1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:50:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:50:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 02:56:35 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:56:35 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 02:56:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 02:56:35 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 02:56:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 02:56:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 02:56:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 02:56:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:56:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 02:56:35 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 03:53:46 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 03:53:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 03:53:46 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 03:53:46 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 03:53:46 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 03:53:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 03:53:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 03:53:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 03:53:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 03:53:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 03:53:46 GMT
USER fluent
# Tue, 13 Jan 2026 03:53:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 03:53:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f278c74b521395e8d456670779ae7a05b6a65ebc00089ae668b5ee55ef6d62f6`  
		Last Modified: Tue, 13 Jan 2026 02:53:45 GMT  
		Size: 3.2 MB (3170974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9183b3c1e9c49337647755deafe50e320b6879585d0a54774393f706fd9fbb72`  
		Last Modified: Tue, 13 Jan 2026 02:53:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ff566d9453f5bcc7d1124d5b1cf75702f3143e3138ed814f440cf76c3ae21e`  
		Last Modified: Tue, 13 Jan 2026 02:56:56 GMT  
		Size: 33.1 MB (33099443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913aa72cc9e474391604787929b188b70d911a86938b3687657777f737b07d40`  
		Last Modified: Tue, 13 Jan 2026 02:56:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e266214ee923c141a23b75e07d7dca01d348772853440a3aa686f61b0f0bd8ae`  
		Last Modified: Tue, 13 Jan 2026 03:54:05 GMT  
		Size: 14.4 MB (14426591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ce6d343ec15b0e452de3065d3e059c4d549513905bc3a57f3057d283648aff`  
		Last Modified: Tue, 13 Jan 2026 03:54:04 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6193a0ccbccd5cce14ce5a59f35d6c67ab36d9a36e2d62ce0967386a853829e`  
		Last Modified: Tue, 13 Jan 2026 03:54:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5a90d1e1578fb71188a9cfbf5fa3a314206ba9be5f12be98307fadc8b1006d`  
		Last Modified: Tue, 13 Jan 2026 03:54:04 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e51e8a7c6e2cd879b710ed7951d18d3dc1b88f9686537d3f00d953d882d38c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed20f4a303f3eda794e7e472f0d5555829a0766f711d9ea5c921526357a172e`

```dockerfile
```

-	Layers:
	-	`sha256:ae9963afe7780f9ffd9e058634655212bb6ea6501c0eaf836b9be624a483aac8`  
		Last Modified: Tue, 13 Jan 2026 06:30:59 GMT  
		Size: 2.7 MB (2667857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1380e81681baa1f593eabb1515c615fbd14c00214d97b29e3fc15365e61b8d`  
		Last Modified: Tue, 13 Jan 2026 06:31:00 GMT  
		Size: 21.1 KB (21067 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.11-debian-1.0`

```console
$ docker pull fluentd@sha256:e057ae4394891d05553f8f040120efa5a4fd26d609cfc1a1f999c76301444f4e
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

### `fluentd:v1.16.11-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:d15b9c90ac2a6ac29ef0c3c06848d1b519df8462f40d0a16d6f121eec1cfe5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82040699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:497bb0f8d4ec539229975e2d2275491fa7d58c606138313431c6f7d5ebfa7dcf`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:16:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:16:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:18:38 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:18:38 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 03:18:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 03:18:38 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 03:18:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:18:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:18:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:18:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:18:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:18:39 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:59:53 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:59:53 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 04:59:53 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 04:59:53 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 04:59:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:59:53 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:59:53 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:59:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:59:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:59:53 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:59:53 GMT
USER fluent
# Tue, 13 Jan 2026 04:59:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:59:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c867442486918ea68669aaa91486e4d57f173e10338d29984bb7a3536def8980`  
		Last Modified: Tue, 13 Jan 2026 03:18:54 GMT  
		Size: 3.5 MB (3509989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81715e94d1f88b8e1e42543f96730089821036d553a5e66c7b1b9cccd04c237`  
		Last Modified: Tue, 13 Jan 2026 03:18:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7da126231fdb147109b8a01b94590f110ca11094acb20f9ca5f19e80c308834`  
		Last Modified: Tue, 13 Jan 2026 03:18:57 GMT  
		Size: 36.0 MB (36008302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d3c7e1c54cfffb4572a0fcafd2707ca0743a3173320aba622c048a09f96927`  
		Last Modified: Tue, 13 Jan 2026 03:18:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae02dbe4e965cfc3107ade9d62fc09fd73c4daf29ce14ecd2cc2af5522cf6aa3`  
		Last Modified: Tue, 13 Jan 2026 05:00:18 GMT  
		Size: 14.3 MB (14291444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee7698fceb111af8f2ba206f8c9249d2eb1adce2686da7ae4aa475e17fc36e1`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed049f2443b53eb7ac79df20380364b7ce65f598c3abf845f201fd75f732db`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9936110fa45e61a00821872dbcce32d1c164c1715958c692a7b9f72c2a44761d`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:42d52a363c2cd32b4bb2348ffaa2a9060f21a5a2c81fc37123484a0c25effcd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f38231ef96de83694b4d18a8ba9cf22fb13535d1e3945d8b8cf3c0a9c28949`

```dockerfile
```

-	Layers:
	-	`sha256:791507e35d202e02f466befc4fcc91e9f9a0c48aede1cdd1144cbddacf819186`  
		Last Modified: Tue, 13 Jan 2026 06:30:31 GMT  
		Size: 2.7 MB (2671032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e3dfbc135922bc2fa1c7c068557473f6053b2e1fdf1b0e9c0ca81ac081c0cf0`  
		Last Modified: Tue, 13 Jan 2026 06:30:31 GMT  
		Size: 21.1 KB (21068 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:51678e3f051d85416c3191027ace27d50915fd179d32977e22a75420a5c2acaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75438707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec403e5730f92e3997cc1a347f9807e038c267b3a82614bc4c9d1434563a2ae0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:26:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:26:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:28:53 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:28:53 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 03:28:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 03:28:53 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 03:28:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:28:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:28:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:28:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:28:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:28:54 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:37:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:37:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 04:37:10 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 04:37:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 04:37:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:37:10 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:37:10 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:37:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:37:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:37:10 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:37:10 GMT
USER fluent
# Tue, 13 Jan 2026 04:37:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:37:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:43595593b17008d0147d9ea53c9ed04f4ec8fde216c1d359e2de9daa9e0665f6`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 25.8 MB (25757697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea68f8d639671ff68dce83d136086909a58ff5957c1c4424f23dba509ab8929`  
		Last Modified: Tue, 13 Jan 2026 03:29:09 GMT  
		Size: 3.1 MB (3080686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e164755af9df33311e54ac8f585cb4f4c2beb5588d89239bce20804932bf7795`  
		Last Modified: Tue, 13 Jan 2026 03:29:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad923f0512d30e9f82cf7712fe08ebd11be1840b4a7428489110aaeb27e9ab6`  
		Last Modified: Tue, 13 Jan 2026 03:29:11 GMT  
		Size: 32.3 MB (32328081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b206d4be1faa9c91b9a00ac65c10bb859908a1c44be33c29ddbbcd42a1f4b5c5`  
		Last Modified: Tue, 13 Jan 2026 03:29:08 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ff4d29e2aad90863fea8c8544717c5b323288983f47e1cd9d980dbedb1841`  
		Last Modified: Tue, 13 Jan 2026 04:37:27 GMT  
		Size: 14.3 MB (14269853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a852f86141bc67ee84471b8afe9dd4e2c6e4cf00d355659584637bae65e913`  
		Last Modified: Tue, 13 Jan 2026 04:37:25 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3264bb23f61f6c26e1fd25fea3b67d990508b78b44e8592cd62ef2f952154fb9`  
		Last Modified: Tue, 13 Jan 2026 04:37:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ee7f145c0fb22f8b3c8b02363e97567ffb2c375b4d960d5bfc55ce5e5b2ffd`  
		Last Modified: Tue, 13 Jan 2026 04:37:25 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2489180e804fac08a1c877a85c5227122a6e2d178fa651a9416a62ed4d5b2db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d548c0c7d3f0b618c20a8a3f273ad32aca8b02862d4a5b385fc5258d31ced12`

```dockerfile
```

-	Layers:
	-	`sha256:c43ac698ebb599d4fa1c6230fb5fb639d59ef5ff39ee0e0fb577b7060d5a4ffa`  
		Last Modified: Tue, 13 Jan 2026 06:30:35 GMT  
		Size: 2.7 MB (2674827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:946ed5ba4e6e00b56cd9447b8f5cbd9d39e7e3d90f3bbe22b71c27a76e825c01`  
		Last Modified: Tue, 13 Jan 2026 06:30:36 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:1fd208bb9af259f4110de6cd26e308e96340a89db992e4dd6743ce37c1212c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73212919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3a829a5f75b0282562b0f72d1bddeaefae6b40d513952e0c4787f741ea4927`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 04:02:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:02:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 04:04:29 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:04:29 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 04:04:29 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 04:04:29 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 04:04:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 04:04:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 04:04:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 04:04:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:04:29 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 04:04:29 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:52:37 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:52:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 04:52:37 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 04:52:37 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 04:52:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:52:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:52:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:52:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:52:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:52:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:52:38 GMT
USER fluent
# Tue, 13 Jan 2026 04:52:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:52:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:08 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d56538f5372345b89edb9cd7f69785f059e689e1ec75c9f857831b903d4e5`  
		Last Modified: Tue, 13 Jan 2026 04:04:46 GMT  
		Size: 2.9 MB (2913529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d87fb932f0dc243377dc90b97d38a1ec5eae15cc624bc03054bb0d2064bbc8`  
		Last Modified: Tue, 13 Jan 2026 04:04:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f76f28198b3321c896e5c8e4c74a535de1a9eeab19dcb65685938796fcdc43e6`  
		Last Modified: Tue, 13 Jan 2026 04:04:48 GMT  
		Size: 32.2 MB (32164038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f2a883f21bae6d75ef1ff2d48ec47ff0ab114698a7ea49a603ac618ea1a925`  
		Last Modified: Tue, 13 Jan 2026 04:04:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d23e82d902e26b770ddeae77134efbbf9813b0d1d87cef0595f67890ae39e7e`  
		Last Modified: Tue, 13 Jan 2026 04:52:55 GMT  
		Size: 14.2 MB (14198838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9a4d8443083883f985b84364e9464aa62dfbcadd285dc27a6f083d63790f80`  
		Last Modified: Tue, 13 Jan 2026 04:52:52 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b500b4431caacbe51d6d7fd49c47f0888b9ce6bd71c04dd86ae9228d562470a6`  
		Last Modified: Tue, 13 Jan 2026 04:52:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24f7c1bdb18920fd7d5e97d7503e7a2523c66229a5f402f57f8adea0e3583ae`  
		Last Modified: Tue, 13 Jan 2026 04:52:52 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:789c34c60fffeb59c7d58232e1ffe80dae65f53ebf054a56d6b9338733c6b5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d15ffe924e5c6d796ee5967e575c1bdfd7ace064351e003ca3c2c64d3e87305`

```dockerfile
```

-	Layers:
	-	`sha256:44b0474111486de1dea1bb5d31bfbada4eac4f1fa2d440318b3c7ec08edfe273`  
		Last Modified: Tue, 13 Jan 2026 06:30:40 GMT  
		Size: 2.7 MB (2673258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2ead36bc243d61d33100516a0bcc86d90c7ee251b498f2ddfb5fdb44186b3d`  
		Last Modified: Tue, 13 Jan 2026 06:30:41 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:d4d7668eec7debbb16ddfd5fd30a0ad8e6135016c3ae4914a98a6d6148eb9dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81659010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3feacef73f69390fb9fd1c5ef8cc294ecfe64f93f4992974230fef6944537f9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:23:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 03:23:49 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:25:58 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:25:58 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 03:25:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 03:25:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 03:25:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:25:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:25:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:25:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:25:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:25:58 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 05:01:46 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 05:01:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 05:01:46 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 05:01:46 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 05:01:46 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 05:01:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 05:01:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 05:01:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 05:01:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 05:01:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 05:01:46 GMT
USER fluent
# Tue, 13 Jan 2026 05:01:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 05:01:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958b8dd8e23755aaefa85b99db1d889e2074dd250cad0466d545393efd097bce`  
		Last Modified: Tue, 13 Jan 2026 03:26:15 GMT  
		Size: 3.3 MB (3341737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fa4f687c57629cc566697ca61b0e02bacb8b263b8296dac609cd2b83586c5c`  
		Last Modified: Tue, 13 Jan 2026 03:26:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc3167b0828ba135d00ac7fdd2f23f1673e33aff953d3049d391d81c3642c7d`  
		Last Modified: Tue, 13 Jan 2026 03:26:17 GMT  
		Size: 35.9 MB (35909290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e402e2a753f9e159e1383396df4d880e246b96cf1ce3303e83bdd1c5cb2f9a`  
		Last Modified: Tue, 13 Jan 2026 03:26:14 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7780af10fbf5b79e40b3b17b5f2ee696d4f834469e08733d4a3e730c5bf12c`  
		Last Modified: Tue, 13 Jan 2026 05:02:03 GMT  
		Size: 14.3 MB (14297702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d5b50a4603ee1ee9fa643909293517f2bb43d575578c1e274981a1c22a5ad5`  
		Last Modified: Tue, 13 Jan 2026 05:02:02 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2a5d1023f1a9e7c96e0900fc0d668c54702c1cbd09026cbd1d88f022c6ef35`  
		Last Modified: Tue, 13 Jan 2026 05:02:02 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae4ca798439d0b2a8ca5c19b825f47a834362150d503b45943fb734a01b36de`  
		Last Modified: Tue, 13 Jan 2026 05:02:02 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:71563cf244ba181c1c20ea38aced23fdbac379d85ea1b358b6f3e6a2517491d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf114ba8b47bdfa5d4a58459a10cb7ca723e4eeee30e33140055761a3ec55dd`

```dockerfile
```

-	Layers:
	-	`sha256:7cac6a4413f038c133b0a2f6114b3c7850dbc38a226ce83bb4f7b89de674431d`  
		Last Modified: Tue, 13 Jan 2026 06:30:45 GMT  
		Size: 2.7 MB (2671272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6765faaef1795747ebe1d5fbc15220e29065b55ffdc951a1c19bd9f19301f83`  
		Last Modified: Tue, 13 Jan 2026 06:30:46 GMT  
		Size: 21.2 KB (21163 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:c35bf73ea8000c3b093f04a8040460b08eb014dbca81d4ae2468675c15ee6bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78965873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3a26c2eb7f93ddc68c72c2c41673b190500ba69cb15424b5010fb300f00ddc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:47:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:47:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 02:50:03 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:50:03 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 02:50:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 02:50:03 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 02:50:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 02:50:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 02:50:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 02:50:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:50:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 02:50:03 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:00:31 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:00:31 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 04:00:31 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 04:00:31 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 04:00:31 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:00:31 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:00:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:00:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:00:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:00:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:00:31 GMT
USER fluent
# Tue, 13 Jan 2026 04:00:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:00:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:45 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ee0c6efab824f716683c3690cc0e16b2f865a123d24b5b015faaa5e7cdd2e3`  
		Last Modified: Tue, 13 Jan 2026 02:50:19 GMT  
		Size: 3.5 MB (3512239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf28144f4a1147bda31ee6657575807b7a418b220243bb3a754bf210b4042d7`  
		Last Modified: Tue, 13 Jan 2026 02:50:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41686bade84f460dca8dd3dfb9a0105001e23cf8c9ef69ee3a633a74860e76e`  
		Last Modified: Tue, 13 Jan 2026 02:50:22 GMT  
		Size: 32.2 MB (32160036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b888d579ad5fe0d15bc72ac04ebd51e2bc1745bbd24f34cb48bac755fe7806`  
		Last Modified: Tue, 13 Jan 2026 02:50:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68f2e38d0b7df1fc95d9d6744ec65f1707efc7bb6a4a853d774910a98f73bf3`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 14.1 MB (14081141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ebd2a4b35dc3c3bc81b28cea13f92479297e0b09df0c20ff9bf5040bc527f0`  
		Last Modified: Tue, 13 Jan 2026 04:00:47 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84d98d0e0139ae2ef068637297aa55a8eb7c3b779c75029d6fb1c3ecb72ae75`  
		Last Modified: Tue, 13 Jan 2026 04:00:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf23808d3611a1c489f5dc573a03a73069588d8cd0004c530f52e70b14056b1`  
		Last Modified: Tue, 13 Jan 2026 04:00:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:81bf17962ee658c140e1585ca6b205054730be47e0942cbadeb3463078c91005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0eb5fed5e7ae777066f3f18dd5f9348f61d862d5ce5cca39caf6ed2f616796e`

```dockerfile
```

-	Layers:
	-	`sha256:607939948a2e2428e615301ee2d3ec8328bfde9c12a141534eef4268a27b4cbd`  
		Last Modified: Tue, 13 Jan 2026 06:30:52 GMT  
		Size: 2.7 MB (2668211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75d43cd07a49f975797eed668d10c28a041e348e25aa1e5374cebe6684d70349`  
		Last Modified: Tue, 13 Jan 2026 06:30:52 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:21d9c93229b70e222730b89a18d20fd3008cce81db02fec3d4352c042dfa1006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84298660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9a88d2b40bf3d6feb0868ee8fc0f97396472266d1c3b0f6d132dd2d9f83aa8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 04:57:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 04:57:36 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 05:11:49 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 05:11:49 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 05:11:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 05:11:49 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 05:11:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 05:11:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 05:11:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 05:11:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:11:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 05:11:49 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 08:53:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 08:53:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 08:53:25 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 08:53:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 08:53:26 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 08:53:26 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 08:53:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 08:53:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 08:53:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 08:53:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 08:53:27 GMT
USER fluent
# Tue, 30 Dec 2025 08:53:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 08:53:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b9cebfd28c842195ef306457f689bf8cbec529ccf65729ab7749cf1505623f`  
		Last Modified: Tue, 30 Dec 2025 05:02:13 GMT  
		Size: 3.7 MB (3709070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a333055b244abc340531d6bf67be5e762ede7cc94d700c3a3bd170892ea00113`  
		Last Modified: Tue, 30 Dec 2025 05:02:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e386747298c411ef446c44b05925fcca2e6ee47e039f8608eb84ce4428a5c9d5`  
		Last Modified: Tue, 30 Dec 2025 05:12:18 GMT  
		Size: 33.8 MB (33832992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d894c7df1e0acbf3b7cbc7f42df580787a6cc196eb3535767a153975936125`  
		Last Modified: Tue, 30 Dec 2025 05:12:15 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca20d39404859ce3688f8951597ef3168ad8870943c5221d01605bf899e7fce`  
		Last Modified: Tue, 30 Dec 2025 08:53:58 GMT  
		Size: 14.7 MB (14685361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1adbdec974ea4246009f77b918df3a820d275dda5aa24b8d7f0e33b6071453`  
		Last Modified: Tue, 30 Dec 2025 08:53:56 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1562f97b4c32aef274d3b6a579fda7832834b940897245947914012df963d3`  
		Last Modified: Tue, 30 Dec 2025 08:53:56 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eaff77d7a86a19b41d23de29eafb3a887ec0627dcbbdbabc2d6bc3b9b06830`  
		Last Modified: Tue, 30 Dec 2025 08:53:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:287589312a9ce169b781a03d28b2832f8c17310d1cbf23a39afaf5f37a9a985f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220486435be460cddba1a1098c09f9b0999ba2011fa12d1edad2ae3c6641a418`

```dockerfile
```

-	Layers:
	-	`sha256:d84b5217c8bc0f4970ec0bbf64e27886eebff2dd0aa6a551c348838402b71ba4`  
		Last Modified: Tue, 30 Dec 2025 09:28:38 GMT  
		Size: 2.7 MB (2675439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30abf1c9149a2f912678403135c814450e872f1e1c901ad5f43f9a82caad0cd7`  
		Last Modified: Tue, 30 Dec 2025 09:28:38 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:61ce2c2ed097ee6dda79508430e8f2f72dec03d2dbb45352dbbce98513583f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6ec814751f6e7f4a5d6655c1ba62c00bc4ba56029989ad7b3d7741adf126b1`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 02:50:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:50:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 02:56:35 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:56:35 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 13 Jan 2026 02:56:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 13 Jan 2026 02:56:35 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 13 Jan 2026 02:56:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 02:56:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 02:56:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 02:56:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:56:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 02:56:35 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 03:53:46 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 03:53:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 13 Jan 2026 03:53:46 GMT
ENV TINI_VERSION=0.18.0
# Tue, 13 Jan 2026 03:53:46 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 13 Jan 2026 03:53:46 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 03:53:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 03:53:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 03:53:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 03:53:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 03:53:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 03:53:46 GMT
USER fluent
# Tue, 13 Jan 2026 03:53:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 03:53:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f278c74b521395e8d456670779ae7a05b6a65ebc00089ae668b5ee55ef6d62f6`  
		Last Modified: Tue, 13 Jan 2026 02:53:45 GMT  
		Size: 3.2 MB (3170974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9183b3c1e9c49337647755deafe50e320b6879585d0a54774393f706fd9fbb72`  
		Last Modified: Tue, 13 Jan 2026 02:53:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ff566d9453f5bcc7d1124d5b1cf75702f3143e3138ed814f440cf76c3ae21e`  
		Last Modified: Tue, 13 Jan 2026 02:56:56 GMT  
		Size: 33.1 MB (33099443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913aa72cc9e474391604787929b188b70d911a86938b3687657777f737b07d40`  
		Last Modified: Tue, 13 Jan 2026 02:56:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e266214ee923c141a23b75e07d7dca01d348772853440a3aa686f61b0f0bd8ae`  
		Last Modified: Tue, 13 Jan 2026 03:54:05 GMT  
		Size: 14.4 MB (14426591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ce6d343ec15b0e452de3065d3e059c4d549513905bc3a57f3057d283648aff`  
		Last Modified: Tue, 13 Jan 2026 03:54:04 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6193a0ccbccd5cce14ce5a59f35d6c67ab36d9a36e2d62ce0967386a853829e`  
		Last Modified: Tue, 13 Jan 2026 03:54:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5a90d1e1578fb71188a9cfbf5fa3a314206ba9be5f12be98307fadc8b1006d`  
		Last Modified: Tue, 13 Jan 2026 03:54:04 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e51e8a7c6e2cd879b710ed7951d18d3dc1b88f9686537d3f00d953d882d38c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed20f4a303f3eda794e7e472f0d5555829a0766f711d9ea5c921526357a172e`

```dockerfile
```

-	Layers:
	-	`sha256:ae9963afe7780f9ffd9e058634655212bb6ea6501c0eaf836b9be624a483aac8`  
		Last Modified: Tue, 13 Jan 2026 06:30:59 GMT  
		Size: 2.7 MB (2667857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d1380e81681baa1f593eabb1515c615fbd14c00214d97b29e3fc15365e61b8d`  
		Last Modified: Tue, 13 Jan 2026 06:31:00 GMT  
		Size: 21.1 KB (21067 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:d3aa191d6f942c95058b251fb8e58db6afe19316a4f4b0a3ed70f3e6313af9f0
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

### `fluentd:v1.19-1` - linux; amd64

```console
$ docker pull fluentd@sha256:3bcde99e3687abecf27e8212ee5c19f0438469a5ddb314883fa63d5008311b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79169074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437e7a69cd621f6ebc46e4a9a1d50a934a36bacf8a69b345d7bddf67175aaa4d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:15:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:17:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:17:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:17:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:17:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:59:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:59:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:59:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:59:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:59:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:59:58 GMT
USER fluent
# Tue, 13 Jan 2026 04:59:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:59:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eef9b8933028d4d086fca9528ccc9271c5f7c65abfa73e952107ef4e71f5b`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 1.3 MB (1279374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef44c7bbb15316ed3c8b90e1149e7e65006f6a352bfbc150f83ba34cf36b8f0`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d36f3a5655a63fccdac1be1dea43008bf13f50700604d5bbb51dfd67c4f1`  
		Last Modified: Tue, 13 Jan 2026 03:17:34 GMT  
		Size: 42.1 MB (42112593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403786353912e853ee3b03de8484cf9cb0c6a860807846ff07bb720943ad0cc2`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95a20976cd45bd6c70aafe68db5deac22d7041dcc4332f23f4371cfb918ba2`  
		Last Modified: Tue, 13 Jan 2026 05:00:25 GMT  
		Size: 6.0 MB (6001029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532f021056a355ffebc964ee6e349fc264a0ffdabb2e14ec25a50f2b008efe2`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8358e169dbb7ee057d2e5fe1001b6db5516639c6e88ed047dca2a65dfb01d`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988474eade660a7633fbfdad69c9a561ab991db1686c4ea44d2227977121d7`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:40742be2e1f215c37553c2e750818bedea348558eef163d65e00231896a7e4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247793a0a9928ab02b7e2013c0ae4ec3be4b506c0db291830b3dfe73be1323fc`

```dockerfile
```

-	Layers:
	-	`sha256:96f7d5ffebc16796703f3e1508ef6ed1867ff28f62d4ef6faf52f9f426b28892`  
		Last Modified: Tue, 13 Jan 2026 06:30:07 GMT  
		Size: 2.3 MB (2280167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d245ee90fda65ffc9ff75c6931bfb574b96d405448a7215873c5367f08bad`  
		Last Modified: Tue, 13 Jan 2026 06:30:07 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:f52d517870022f9ed7bffb4772dc8a2588760749e6605719195dcc85199a2d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73015490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05859ae973b197cc8a0246f09dcf7bea6bf454bb4ce55ee0ed5176fe0da576ac`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:23:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:26:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:38:08 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:38:08 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:38:08 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:38:08 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:38:08 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:38:08 GMT
USER fluent
# Tue, 13 Jan 2026 04:38:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:38:08 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1320c956f4c83fcb0562b315b8bda5dd174609e7d7ca750c0c5b25757c3a4e39`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 1.3 MB (1263009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4536c4a4c2b9a4b25706298eea75e411ecf7474ec825e95487a3fc45677109b`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6673c3e63216c5e4ec98fc85dddea075baddb32362e818e7ce47e7028fc26574`  
		Last Modified: Tue, 13 Jan 2026 03:26:50 GMT  
		Size: 37.9 MB (37905868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0676e2edb97826a7240b8e67fa4464779b809420476b9a092842c95228a68c2`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e667d8c88075d8402d7e8e9d1c8a2e8d83d266277342528ad7324ce3d65eeb0a`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 5.9 MB (5901500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f0bd7482758a351bf2332fce7368df03d0fcd8fd2536fc8d4411ab00f82d04`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0417fc24ae33338c26093691d99cba4dc63c357664c86f9865b640d4718c7f`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ea0521b7ac5a88ea214f2aee9f3572ab1b928e8ec982413f551b5550b8d30c`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b4949c17a66864f5b759d52baf0b5b56262328a7c5e00cb36f1b18651a3d1501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37f234ef4b0e2b6bc356defd5465da1e3f4900dab4f8d0d0f5ae950c385e12`

```dockerfile
```

-	Layers:
	-	`sha256:3de1fffa2b8ba00ff71bab251fe6d3cb80c93072d51e7b0f66fc50ba8d862863`  
		Last Modified: Tue, 13 Jan 2026 06:30:11 GMT  
		Size: 2.3 MB (2283138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a727fbbb6584143a529944a5a01d6a0f141ad05ecbf2c84f7030bb180513cf89`  
		Last Modified: Tue, 13 Jan 2026 06:30:12 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:d11673dae75290f1512772fbf2fccf20f343e5f35200b7242c5d64461cf9c7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70883874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012e252ef68a7d2d9e65f9bd3e732c7a7a77c480ac76e2c262b317e71e3f404d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 04:01:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:01:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 04:03:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 04:03:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 04:03:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:03:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:52:53 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:52:53 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:52:53 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:52:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:52:53 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:52:53 GMT
USER fluent
# Tue, 13 Jan 2026 04:52:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:52:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb89ad4eba0f6c13ed221ba61cd63256963a2ae6022c5eb1a90dfe213d338e`  
		Last Modified: Tue, 13 Jan 2026 04:04:17 GMT  
		Size: 1.2 MB (1236555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4524518ebfe925ff0ba895a410f351e2ee7d22045883650d8b7fac782a9cc4c`  
		Last Modified: Tue, 13 Jan 2026 04:04:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafc5c289841a0fbb484e454157cfd1cd3e738994188089f928286b34c74f8`  
		Last Modified: Tue, 13 Jan 2026 04:04:25 GMT  
		Size: 37.8 MB (37767155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c4e1fbfecc70f8903b4522859b5ef39a5906274e2351951079ed8f886585`  
		Last Modified: Tue, 13 Jan 2026 04:04:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7740d7e2c777411352b0085fe0094c95668acdde8c6ece31de343123a5cf9`  
		Last Modified: Tue, 13 Jan 2026 04:53:08 GMT  
		Size: 5.7 MB (5669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2b431fd4058cc969b8cbb21b31aacdf5b6c415776385b9bd855de095a86be`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0486e503a316218c72159c4aecfd966c0227bea5022343f9e65a9bab48e9a294`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a8b50351ca059aa0d8b903508c9a57aa8984f21e7a73c28431739b765cabf`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:28ce653f313504add74d6ae0ea8a60b536b728cce10f717c1b3b6b702df1a407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d63c54bd63cbb3caddc547142ff8e84bd64af8fa85b87fb1ad06e91d13c95c6`

```dockerfile
```

-	Layers:
	-	`sha256:1af10659db7793cb979bd306619dc8928e9299489553158805ffbdb212d7cabc`  
		Last Modified: Tue, 13 Jan 2026 06:30:16 GMT  
		Size: 2.3 MB (2281579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37545b709467be88ec29e37388b144288be9462833e3cab824fdb247fc368901`  
		Last Modified: Tue, 13 Jan 2026 06:30:17 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2ba5ac0282f0a65ad95fc63a472a55621f2f4b0fcb0e0ce1160034733c471471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79461765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a54308eb52c307d090b75de044c8eb95213037450e55a4d504e551dd7a804bc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:23:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:26:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 05:01:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 05:01:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 05:01:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 05:01:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 05:01:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 05:01:38 GMT
USER fluent
# Tue, 13 Jan 2026 05:01:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 05:01:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0525c3d775730a255f13515eebc27444890213cd946823934e1e349ebf85d`  
		Last Modified: Tue, 13 Jan 2026 03:26:18 GMT  
		Size: 1.3 MB (1261687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afe863bf626435a4acc6286e46071f69c3c80a6a559f73494d100c77e2a459f`  
		Last Modified: Tue, 13 Jan 2026 03:25:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505e6a88accd972129dcba73d3823653527e349b86bd85b23d7be05e6b7d131e`  
		Last Modified: Tue, 13 Jan 2026 03:26:20 GMT  
		Size: 42.1 MB (42074273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12087ea894d19fc0f651859b919a840ad2d733574392ff2bab6decc744d11ee`  
		Last Modified: Tue, 13 Jan 2026 03:26:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42466d7a4e7c4317a6aca126263010a1f5d4cbf475285844859615e6f8647cbc`  
		Last Modified: Tue, 13 Jan 2026 05:01:55 GMT  
		Size: 6.0 MB (5989373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd395c404a6148260abf43c4fc068f0b8cc16e4f0cc22e7e47f0d6861db9ec0c`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228cea3da2223620ff60c397a125f567c560bfabe61226b0b0a4ca0ee4e995a4`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423f136b4f2f4082396887c88c937d76864d24d7c3520bff51d342355d459f2a`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:58ac976c6818af47fcc251821f582953708800364f8645c8c20db42650b6079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e553d3d1f1c6af6ffd1dbbc3cd00eddcf89a9244856d490e67448175ad2ae0cd`

```dockerfile
```

-	Layers:
	-	`sha256:c881d4ff0b96d3adb92b3f5d51324cd3000d2b17891c26d2344509210b0055c5`  
		Last Modified: Tue, 13 Jan 2026 06:30:21 GMT  
		Size: 2.3 MB (2280439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac4b52effa78caa2eaab59f393d2747368a2723ded9da3da8999144a067da91`  
		Last Modified: Tue, 13 Jan 2026 06:30:21 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:90a276a23933880908550e3b249d0636588803070ad0cc3125c0650c1798c07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76209821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb7f8b78264676135dfddc1a5a8ea25db76afae7125f39945e3b100ac88217`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 02:49:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 02:49:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 02:49:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:49:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:00:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:00:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:00:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:00:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:00:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:00:27 GMT
USER fluent
# Tue, 13 Jan 2026 04:00:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:00:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca9739d6b026ec1d4cd350482fedc4374621d2428ab77e18051bdb8ca6c93a`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 1.3 MB (1287208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf308c9322d7b7ccb72a3b032126ea9174c0dd19d5133f792f459c5f0fec63`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077996a21b00611176c639502288dd2a7a31e063ef348d46a1652665d276aa0`  
		Last Modified: Tue, 13 Jan 2026 02:49:43 GMT  
		Size: 37.7 MB (37661435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f373e260e56fe68e120ff78469b633199ef4d7e6980f6c1706b0628c090ec`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b70dc93001436daee4f4c2269d3b473cc83687fd15af6b3b65b15d67a592ad`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 6.0 MB (5970309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64083097cffea937936c9ec17bfa648c81bbc71f8d05d684b7afb9e52a48d5c5`  
		Last Modified: Tue, 13 Jan 2026 04:01:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5966fa1c56255ac85fd3cda423eb24e7808ebd4ca2f9f0ea681e3e09bfc34`  
		Last Modified: Tue, 13 Jan 2026 04:00:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefc55a043cc735826153c6bbcbc2f26bc3b8b365fb9dd174493eeb4c568d44`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4dcfb61e511dc10991bc33f42e5660fc254fc795b9f1364f8f111b6a050be002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e6add496a0ab66cc6edaaa2ce6ffb23a10a39d16e78f5a6362f09a674985c2`

```dockerfile
```

-	Layers:
	-	`sha256:eea3a0edad86e0c342eb31d911134cbbf7295ec64067fb3bbfd4a1d860ccf606`  
		Last Modified: Tue, 13 Jan 2026 06:30:25 GMT  
		Size: 2.3 MB (2277355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0ea0b7db35baa06510b1a0264df2ddf0c3651935cfe0f32813ad862ea1efe8`  
		Last Modified: Tue, 13 Jan 2026 06:30:26 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:d3adf405db172cdb0926246543a6512e24c94c39d2c8f8fa6de24b4f4230f417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80942262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e134450b5ea6ce9b16abc2e430bd5deb9bcb6dbb166e9f8d53d29fdbad29a2c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 18:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 18:53:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 18:57:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 18:57:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 18:57:58 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 21:20:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 21:20:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 21:20:29 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 21:20:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 21:20:30 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 21:20:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 21:20:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 21:20:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 21:20:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 21:20:31 GMT
USER fluent
# Tue, 30 Dec 2025 21:20:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 21:20:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec427cb0f29aa78b3a35043f5c43e0a07e16cba482febff3fe2087900b8e01`  
		Last Modified: Tue, 30 Dec 2025 18:58:40 GMT  
		Size: 1.3 MB (1309698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119f3f7815c4977fbb7b151b6aaa8cf695081c5e63a241e7e8ccfa7cff83fcb`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6841342fbfd6bcc1a592039fcb307930a186477e89093dcc569ddb52f69b663`  
		Last Modified: Tue, 30 Dec 2025 18:58:42 GMT  
		Size: 39.5 MB (39519497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ecf017368e45fae8cb085ed7b4384c0e98da8232a690f0b6c1dffc3a99bb0`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c06a5efcd7af94fd4a7d702dddc472d60cb22b1ed26f26cf4b421e3c32f3f7f`  
		Last Modified: Tue, 30 Dec 2025 21:20:58 GMT  
		Size: 6.5 MB (6513782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d35286b4d75cd4ff6451e45864c1d79e0f811e301fe3b34540241af0a87d8`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534390e158cdb1f91f722d150993c5cd591cbefdc5b40262115b84a4c1977fe2`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1185bfeb67fbda08aa3f66a4c34eea27c0cf23ca82c32fb778f16b994d79f43`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2dfeb20c2fabcf019f75db5cb34b6d87d224cc95c8faad30eadc12a2d3cd89de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa85e5209179c6f949d0f2a73450f2b6a987ac9db17c829dac828f742025461`

```dockerfile
```

-	Layers:
	-	`sha256:44270606ed9db02298dbbf78bd7ae9bd926994714d651d08aa9afeca92bf8afa`  
		Last Modified: Wed, 31 Dec 2025 00:28:36 GMT  
		Size: 2.3 MB (2283640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ad2156a8f759a86af16633a4b90867f271a588d55694eccc556442f519404e`  
		Last Modified: Wed, 31 Dec 2025 00:28:37 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; s390x

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

### `fluentd:v1.19-1` - unknown; unknown

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

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:d3aa191d6f942c95058b251fb8e58db6afe19316a4f4b0a3ed70f3e6313af9f0
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

### `fluentd:v1.19-debian-1` - linux; amd64

```console
$ docker pull fluentd@sha256:3bcde99e3687abecf27e8212ee5c19f0438469a5ddb314883fa63d5008311b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79169074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437e7a69cd621f6ebc46e4a9a1d50a934a36bacf8a69b345d7bddf67175aaa4d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:15:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:17:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:17:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:17:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:17:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:59:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:59:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:59:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:59:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:59:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:59:58 GMT
USER fluent
# Tue, 13 Jan 2026 04:59:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:59:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eef9b8933028d4d086fca9528ccc9271c5f7c65abfa73e952107ef4e71f5b`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 1.3 MB (1279374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef44c7bbb15316ed3c8b90e1149e7e65006f6a352bfbc150f83ba34cf36b8f0`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d36f3a5655a63fccdac1be1dea43008bf13f50700604d5bbb51dfd67c4f1`  
		Last Modified: Tue, 13 Jan 2026 03:17:34 GMT  
		Size: 42.1 MB (42112593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403786353912e853ee3b03de8484cf9cb0c6a860807846ff07bb720943ad0cc2`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95a20976cd45bd6c70aafe68db5deac22d7041dcc4332f23f4371cfb918ba2`  
		Last Modified: Tue, 13 Jan 2026 05:00:25 GMT  
		Size: 6.0 MB (6001029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532f021056a355ffebc964ee6e349fc264a0ffdabb2e14ec25a50f2b008efe2`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8358e169dbb7ee057d2e5fe1001b6db5516639c6e88ed047dca2a65dfb01d`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988474eade660a7633fbfdad69c9a561ab991db1686c4ea44d2227977121d7`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:40742be2e1f215c37553c2e750818bedea348558eef163d65e00231896a7e4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247793a0a9928ab02b7e2013c0ae4ec3be4b506c0db291830b3dfe73be1323fc`

```dockerfile
```

-	Layers:
	-	`sha256:96f7d5ffebc16796703f3e1508ef6ed1867ff28f62d4ef6faf52f9f426b28892`  
		Last Modified: Tue, 13 Jan 2026 06:30:07 GMT  
		Size: 2.3 MB (2280167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d245ee90fda65ffc9ff75c6931bfb574b96d405448a7215873c5367f08bad`  
		Last Modified: Tue, 13 Jan 2026 06:30:07 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:f52d517870022f9ed7bffb4772dc8a2588760749e6605719195dcc85199a2d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73015490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05859ae973b197cc8a0246f09dcf7bea6bf454bb4ce55ee0ed5176fe0da576ac`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:23:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:26:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:38:08 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:38:08 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:38:08 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:38:08 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:38:08 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:38:08 GMT
USER fluent
# Tue, 13 Jan 2026 04:38:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:38:08 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1320c956f4c83fcb0562b315b8bda5dd174609e7d7ca750c0c5b25757c3a4e39`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 1.3 MB (1263009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4536c4a4c2b9a4b25706298eea75e411ecf7474ec825e95487a3fc45677109b`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6673c3e63216c5e4ec98fc85dddea075baddb32362e818e7ce47e7028fc26574`  
		Last Modified: Tue, 13 Jan 2026 03:26:50 GMT  
		Size: 37.9 MB (37905868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0676e2edb97826a7240b8e67fa4464779b809420476b9a092842c95228a68c2`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e667d8c88075d8402d7e8e9d1c8a2e8d83d266277342528ad7324ce3d65eeb0a`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 5.9 MB (5901500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f0bd7482758a351bf2332fce7368df03d0fcd8fd2536fc8d4411ab00f82d04`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0417fc24ae33338c26093691d99cba4dc63c357664c86f9865b640d4718c7f`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ea0521b7ac5a88ea214f2aee9f3572ab1b928e8ec982413f551b5550b8d30c`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b4949c17a66864f5b759d52baf0b5b56262328a7c5e00cb36f1b18651a3d1501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37f234ef4b0e2b6bc356defd5465da1e3f4900dab4f8d0d0f5ae950c385e12`

```dockerfile
```

-	Layers:
	-	`sha256:3de1fffa2b8ba00ff71bab251fe6d3cb80c93072d51e7b0f66fc50ba8d862863`  
		Last Modified: Tue, 13 Jan 2026 06:30:11 GMT  
		Size: 2.3 MB (2283138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a727fbbb6584143a529944a5a01d6a0f141ad05ecbf2c84f7030bb180513cf89`  
		Last Modified: Tue, 13 Jan 2026 06:30:12 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:d11673dae75290f1512772fbf2fccf20f343e5f35200b7242c5d64461cf9c7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70883874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012e252ef68a7d2d9e65f9bd3e732c7a7a77c480ac76e2c262b317e71e3f404d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 04:01:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:01:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 04:03:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 04:03:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 04:03:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:03:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:52:53 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:52:53 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:52:53 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:52:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:52:53 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:52:53 GMT
USER fluent
# Tue, 13 Jan 2026 04:52:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:52:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb89ad4eba0f6c13ed221ba61cd63256963a2ae6022c5eb1a90dfe213d338e`  
		Last Modified: Tue, 13 Jan 2026 04:04:17 GMT  
		Size: 1.2 MB (1236555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4524518ebfe925ff0ba895a410f351e2ee7d22045883650d8b7fac782a9cc4c`  
		Last Modified: Tue, 13 Jan 2026 04:04:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafc5c289841a0fbb484e454157cfd1cd3e738994188089f928286b34c74f8`  
		Last Modified: Tue, 13 Jan 2026 04:04:25 GMT  
		Size: 37.8 MB (37767155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c4e1fbfecc70f8903b4522859b5ef39a5906274e2351951079ed8f886585`  
		Last Modified: Tue, 13 Jan 2026 04:04:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7740d7e2c777411352b0085fe0094c95668acdde8c6ece31de343123a5cf9`  
		Last Modified: Tue, 13 Jan 2026 04:53:08 GMT  
		Size: 5.7 MB (5669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2b431fd4058cc969b8cbb21b31aacdf5b6c415776385b9bd855de095a86be`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0486e503a316218c72159c4aecfd966c0227bea5022343f9e65a9bab48e9a294`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a8b50351ca059aa0d8b903508c9a57aa8984f21e7a73c28431739b765cabf`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:28ce653f313504add74d6ae0ea8a60b536b728cce10f717c1b3b6b702df1a407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d63c54bd63cbb3caddc547142ff8e84bd64af8fa85b87fb1ad06e91d13c95c6`

```dockerfile
```

-	Layers:
	-	`sha256:1af10659db7793cb979bd306619dc8928e9299489553158805ffbdb212d7cabc`  
		Last Modified: Tue, 13 Jan 2026 06:30:16 GMT  
		Size: 2.3 MB (2281579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37545b709467be88ec29e37388b144288be9462833e3cab824fdb247fc368901`  
		Last Modified: Tue, 13 Jan 2026 06:30:17 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2ba5ac0282f0a65ad95fc63a472a55621f2f4b0fcb0e0ce1160034733c471471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79461765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a54308eb52c307d090b75de044c8eb95213037450e55a4d504e551dd7a804bc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:23:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:26:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 05:01:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 05:01:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 05:01:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 05:01:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 05:01:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 05:01:38 GMT
USER fluent
# Tue, 13 Jan 2026 05:01:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 05:01:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0525c3d775730a255f13515eebc27444890213cd946823934e1e349ebf85d`  
		Last Modified: Tue, 13 Jan 2026 03:26:18 GMT  
		Size: 1.3 MB (1261687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afe863bf626435a4acc6286e46071f69c3c80a6a559f73494d100c77e2a459f`  
		Last Modified: Tue, 13 Jan 2026 03:25:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505e6a88accd972129dcba73d3823653527e349b86bd85b23d7be05e6b7d131e`  
		Last Modified: Tue, 13 Jan 2026 03:26:20 GMT  
		Size: 42.1 MB (42074273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12087ea894d19fc0f651859b919a840ad2d733574392ff2bab6decc744d11ee`  
		Last Modified: Tue, 13 Jan 2026 03:26:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42466d7a4e7c4317a6aca126263010a1f5d4cbf475285844859615e6f8647cbc`  
		Last Modified: Tue, 13 Jan 2026 05:01:55 GMT  
		Size: 6.0 MB (5989373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd395c404a6148260abf43c4fc068f0b8cc16e4f0cc22e7e47f0d6861db9ec0c`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228cea3da2223620ff60c397a125f567c560bfabe61226b0b0a4ca0ee4e995a4`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423f136b4f2f4082396887c88c937d76864d24d7c3520bff51d342355d459f2a`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:58ac976c6818af47fcc251821f582953708800364f8645c8c20db42650b6079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e553d3d1f1c6af6ffd1dbbc3cd00eddcf89a9244856d490e67448175ad2ae0cd`

```dockerfile
```

-	Layers:
	-	`sha256:c881d4ff0b96d3adb92b3f5d51324cd3000d2b17891c26d2344509210b0055c5`  
		Last Modified: Tue, 13 Jan 2026 06:30:21 GMT  
		Size: 2.3 MB (2280439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac4b52effa78caa2eaab59f393d2747368a2723ded9da3da8999144a067da91`  
		Last Modified: Tue, 13 Jan 2026 06:30:21 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:90a276a23933880908550e3b249d0636588803070ad0cc3125c0650c1798c07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76209821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb7f8b78264676135dfddc1a5a8ea25db76afae7125f39945e3b100ac88217`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 02:49:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 02:49:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 02:49:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:49:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:00:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:00:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:00:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:00:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:00:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:00:27 GMT
USER fluent
# Tue, 13 Jan 2026 04:00:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:00:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca9739d6b026ec1d4cd350482fedc4374621d2428ab77e18051bdb8ca6c93a`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 1.3 MB (1287208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf308c9322d7b7ccb72a3b032126ea9174c0dd19d5133f792f459c5f0fec63`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077996a21b00611176c639502288dd2a7a31e063ef348d46a1652665d276aa0`  
		Last Modified: Tue, 13 Jan 2026 02:49:43 GMT  
		Size: 37.7 MB (37661435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f373e260e56fe68e120ff78469b633199ef4d7e6980f6c1706b0628c090ec`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b70dc93001436daee4f4c2269d3b473cc83687fd15af6b3b65b15d67a592ad`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 6.0 MB (5970309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64083097cffea937936c9ec17bfa648c81bbc71f8d05d684b7afb9e52a48d5c5`  
		Last Modified: Tue, 13 Jan 2026 04:01:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5966fa1c56255ac85fd3cda423eb24e7808ebd4ca2f9f0ea681e3e09bfc34`  
		Last Modified: Tue, 13 Jan 2026 04:00:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefc55a043cc735826153c6bbcbc2f26bc3b8b365fb9dd174493eeb4c568d44`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4dcfb61e511dc10991bc33f42e5660fc254fc795b9f1364f8f111b6a050be002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e6add496a0ab66cc6edaaa2ce6ffb23a10a39d16e78f5a6362f09a674985c2`

```dockerfile
```

-	Layers:
	-	`sha256:eea3a0edad86e0c342eb31d911134cbbf7295ec64067fb3bbfd4a1d860ccf606`  
		Last Modified: Tue, 13 Jan 2026 06:30:25 GMT  
		Size: 2.3 MB (2277355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0ea0b7db35baa06510b1a0264df2ddf0c3651935cfe0f32813ad862ea1efe8`  
		Last Modified: Tue, 13 Jan 2026 06:30:26 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:d3adf405db172cdb0926246543a6512e24c94c39d2c8f8fa6de24b4f4230f417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80942262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e134450b5ea6ce9b16abc2e430bd5deb9bcb6dbb166e9f8d53d29fdbad29a2c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 18:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 18:53:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 18:57:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 18:57:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 18:57:58 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 21:20:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 21:20:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 21:20:29 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 21:20:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 21:20:30 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 21:20:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 21:20:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 21:20:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 21:20:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 21:20:31 GMT
USER fluent
# Tue, 30 Dec 2025 21:20:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 21:20:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec427cb0f29aa78b3a35043f5c43e0a07e16cba482febff3fe2087900b8e01`  
		Last Modified: Tue, 30 Dec 2025 18:58:40 GMT  
		Size: 1.3 MB (1309698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119f3f7815c4977fbb7b151b6aaa8cf695081c5e63a241e7e8ccfa7cff83fcb`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6841342fbfd6bcc1a592039fcb307930a186477e89093dcc569ddb52f69b663`  
		Last Modified: Tue, 30 Dec 2025 18:58:42 GMT  
		Size: 39.5 MB (39519497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ecf017368e45fae8cb085ed7b4384c0e98da8232a690f0b6c1dffc3a99bb0`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c06a5efcd7af94fd4a7d702dddc472d60cb22b1ed26f26cf4b421e3c32f3f7f`  
		Last Modified: Tue, 30 Dec 2025 21:20:58 GMT  
		Size: 6.5 MB (6513782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d35286b4d75cd4ff6451e45864c1d79e0f811e301fe3b34540241af0a87d8`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534390e158cdb1f91f722d150993c5cd591cbefdc5b40262115b84a4c1977fe2`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1185bfeb67fbda08aa3f66a4c34eea27c0cf23ca82c32fb778f16b994d79f43`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2dfeb20c2fabcf019f75db5cb34b6d87d224cc95c8faad30eadc12a2d3cd89de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa85e5209179c6f949d0f2a73450f2b6a987ac9db17c829dac828f742025461`

```dockerfile
```

-	Layers:
	-	`sha256:44270606ed9db02298dbbf78bd7ae9bd926994714d651d08aa9afeca92bf8afa`  
		Last Modified: Wed, 31 Dec 2025 00:28:36 GMT  
		Size: 2.3 MB (2283640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ad2156a8f759a86af16633a4b90867f271a588d55694eccc556442f519404e`  
		Last Modified: Wed, 31 Dec 2025 00:28:37 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; s390x

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

## `fluentd:v1.19.0-1.0`

```console
$ docker pull fluentd@sha256:d3aa191d6f942c95058b251fb8e58db6afe19316a4f4b0a3ed70f3e6313af9f0
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

### `fluentd:v1.19.0-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:3bcde99e3687abecf27e8212ee5c19f0438469a5ddb314883fa63d5008311b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79169074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437e7a69cd621f6ebc46e4a9a1d50a934a36bacf8a69b345d7bddf67175aaa4d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:15:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:17:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:17:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:17:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:17:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:59:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:59:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:59:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:59:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:59:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:59:58 GMT
USER fluent
# Tue, 13 Jan 2026 04:59:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:59:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eef9b8933028d4d086fca9528ccc9271c5f7c65abfa73e952107ef4e71f5b`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 1.3 MB (1279374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef44c7bbb15316ed3c8b90e1149e7e65006f6a352bfbc150f83ba34cf36b8f0`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d36f3a5655a63fccdac1be1dea43008bf13f50700604d5bbb51dfd67c4f1`  
		Last Modified: Tue, 13 Jan 2026 03:17:34 GMT  
		Size: 42.1 MB (42112593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403786353912e853ee3b03de8484cf9cb0c6a860807846ff07bb720943ad0cc2`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95a20976cd45bd6c70aafe68db5deac22d7041dcc4332f23f4371cfb918ba2`  
		Last Modified: Tue, 13 Jan 2026 05:00:25 GMT  
		Size: 6.0 MB (6001029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532f021056a355ffebc964ee6e349fc264a0ffdabb2e14ec25a50f2b008efe2`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8358e169dbb7ee057d2e5fe1001b6db5516639c6e88ed047dca2a65dfb01d`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988474eade660a7633fbfdad69c9a561ab991db1686c4ea44d2227977121d7`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:40742be2e1f215c37553c2e750818bedea348558eef163d65e00231896a7e4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247793a0a9928ab02b7e2013c0ae4ec3be4b506c0db291830b3dfe73be1323fc`

```dockerfile
```

-	Layers:
	-	`sha256:96f7d5ffebc16796703f3e1508ef6ed1867ff28f62d4ef6faf52f9f426b28892`  
		Last Modified: Tue, 13 Jan 2026 06:30:07 GMT  
		Size: 2.3 MB (2280167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d245ee90fda65ffc9ff75c6931bfb574b96d405448a7215873c5367f08bad`  
		Last Modified: Tue, 13 Jan 2026 06:30:07 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:f52d517870022f9ed7bffb4772dc8a2588760749e6605719195dcc85199a2d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73015490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05859ae973b197cc8a0246f09dcf7bea6bf454bb4ce55ee0ed5176fe0da576ac`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:23:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:26:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:38:08 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:38:08 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:38:08 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:38:08 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:38:08 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:38:08 GMT
USER fluent
# Tue, 13 Jan 2026 04:38:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:38:08 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1320c956f4c83fcb0562b315b8bda5dd174609e7d7ca750c0c5b25757c3a4e39`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 1.3 MB (1263009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4536c4a4c2b9a4b25706298eea75e411ecf7474ec825e95487a3fc45677109b`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6673c3e63216c5e4ec98fc85dddea075baddb32362e818e7ce47e7028fc26574`  
		Last Modified: Tue, 13 Jan 2026 03:26:50 GMT  
		Size: 37.9 MB (37905868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0676e2edb97826a7240b8e67fa4464779b809420476b9a092842c95228a68c2`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e667d8c88075d8402d7e8e9d1c8a2e8d83d266277342528ad7324ce3d65eeb0a`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 5.9 MB (5901500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f0bd7482758a351bf2332fce7368df03d0fcd8fd2536fc8d4411ab00f82d04`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0417fc24ae33338c26093691d99cba4dc63c357664c86f9865b640d4718c7f`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ea0521b7ac5a88ea214f2aee9f3572ab1b928e8ec982413f551b5550b8d30c`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b4949c17a66864f5b759d52baf0b5b56262328a7c5e00cb36f1b18651a3d1501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37f234ef4b0e2b6bc356defd5465da1e3f4900dab4f8d0d0f5ae950c385e12`

```dockerfile
```

-	Layers:
	-	`sha256:3de1fffa2b8ba00ff71bab251fe6d3cb80c93072d51e7b0f66fc50ba8d862863`  
		Last Modified: Tue, 13 Jan 2026 06:30:11 GMT  
		Size: 2.3 MB (2283138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a727fbbb6584143a529944a5a01d6a0f141ad05ecbf2c84f7030bb180513cf89`  
		Last Modified: Tue, 13 Jan 2026 06:30:12 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:d11673dae75290f1512772fbf2fccf20f343e5f35200b7242c5d64461cf9c7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70883874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012e252ef68a7d2d9e65f9bd3e732c7a7a77c480ac76e2c262b317e71e3f404d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 04:01:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:01:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 04:03:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 04:03:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 04:03:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:03:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:52:53 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:52:53 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:52:53 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:52:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:52:53 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:52:53 GMT
USER fluent
# Tue, 13 Jan 2026 04:52:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:52:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb89ad4eba0f6c13ed221ba61cd63256963a2ae6022c5eb1a90dfe213d338e`  
		Last Modified: Tue, 13 Jan 2026 04:04:17 GMT  
		Size: 1.2 MB (1236555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4524518ebfe925ff0ba895a410f351e2ee7d22045883650d8b7fac782a9cc4c`  
		Last Modified: Tue, 13 Jan 2026 04:04:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafc5c289841a0fbb484e454157cfd1cd3e738994188089f928286b34c74f8`  
		Last Modified: Tue, 13 Jan 2026 04:04:25 GMT  
		Size: 37.8 MB (37767155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c4e1fbfecc70f8903b4522859b5ef39a5906274e2351951079ed8f886585`  
		Last Modified: Tue, 13 Jan 2026 04:04:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7740d7e2c777411352b0085fe0094c95668acdde8c6ece31de343123a5cf9`  
		Last Modified: Tue, 13 Jan 2026 04:53:08 GMT  
		Size: 5.7 MB (5669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2b431fd4058cc969b8cbb21b31aacdf5b6c415776385b9bd855de095a86be`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0486e503a316218c72159c4aecfd966c0227bea5022343f9e65a9bab48e9a294`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a8b50351ca059aa0d8b903508c9a57aa8984f21e7a73c28431739b765cabf`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:28ce653f313504add74d6ae0ea8a60b536b728cce10f717c1b3b6b702df1a407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d63c54bd63cbb3caddc547142ff8e84bd64af8fa85b87fb1ad06e91d13c95c6`

```dockerfile
```

-	Layers:
	-	`sha256:1af10659db7793cb979bd306619dc8928e9299489553158805ffbdb212d7cabc`  
		Last Modified: Tue, 13 Jan 2026 06:30:16 GMT  
		Size: 2.3 MB (2281579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37545b709467be88ec29e37388b144288be9462833e3cab824fdb247fc368901`  
		Last Modified: Tue, 13 Jan 2026 06:30:17 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2ba5ac0282f0a65ad95fc63a472a55621f2f4b0fcb0e0ce1160034733c471471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79461765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a54308eb52c307d090b75de044c8eb95213037450e55a4d504e551dd7a804bc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:23:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:26:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 05:01:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 05:01:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 05:01:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 05:01:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 05:01:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 05:01:38 GMT
USER fluent
# Tue, 13 Jan 2026 05:01:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 05:01:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0525c3d775730a255f13515eebc27444890213cd946823934e1e349ebf85d`  
		Last Modified: Tue, 13 Jan 2026 03:26:18 GMT  
		Size: 1.3 MB (1261687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afe863bf626435a4acc6286e46071f69c3c80a6a559f73494d100c77e2a459f`  
		Last Modified: Tue, 13 Jan 2026 03:25:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505e6a88accd972129dcba73d3823653527e349b86bd85b23d7be05e6b7d131e`  
		Last Modified: Tue, 13 Jan 2026 03:26:20 GMT  
		Size: 42.1 MB (42074273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12087ea894d19fc0f651859b919a840ad2d733574392ff2bab6decc744d11ee`  
		Last Modified: Tue, 13 Jan 2026 03:26:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42466d7a4e7c4317a6aca126263010a1f5d4cbf475285844859615e6f8647cbc`  
		Last Modified: Tue, 13 Jan 2026 05:01:55 GMT  
		Size: 6.0 MB (5989373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd395c404a6148260abf43c4fc068f0b8cc16e4f0cc22e7e47f0d6861db9ec0c`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228cea3da2223620ff60c397a125f567c560bfabe61226b0b0a4ca0ee4e995a4`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423f136b4f2f4082396887c88c937d76864d24d7c3520bff51d342355d459f2a`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:58ac976c6818af47fcc251821f582953708800364f8645c8c20db42650b6079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e553d3d1f1c6af6ffd1dbbc3cd00eddcf89a9244856d490e67448175ad2ae0cd`

```dockerfile
```

-	Layers:
	-	`sha256:c881d4ff0b96d3adb92b3f5d51324cd3000d2b17891c26d2344509210b0055c5`  
		Last Modified: Tue, 13 Jan 2026 06:30:21 GMT  
		Size: 2.3 MB (2280439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac4b52effa78caa2eaab59f393d2747368a2723ded9da3da8999144a067da91`  
		Last Modified: Tue, 13 Jan 2026 06:30:21 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:90a276a23933880908550e3b249d0636588803070ad0cc3125c0650c1798c07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76209821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb7f8b78264676135dfddc1a5a8ea25db76afae7125f39945e3b100ac88217`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 02:49:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 02:49:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 02:49:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:49:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:00:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:00:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:00:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:00:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:00:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:00:27 GMT
USER fluent
# Tue, 13 Jan 2026 04:00:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:00:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca9739d6b026ec1d4cd350482fedc4374621d2428ab77e18051bdb8ca6c93a`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 1.3 MB (1287208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf308c9322d7b7ccb72a3b032126ea9174c0dd19d5133f792f459c5f0fec63`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077996a21b00611176c639502288dd2a7a31e063ef348d46a1652665d276aa0`  
		Last Modified: Tue, 13 Jan 2026 02:49:43 GMT  
		Size: 37.7 MB (37661435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f373e260e56fe68e120ff78469b633199ef4d7e6980f6c1706b0628c090ec`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b70dc93001436daee4f4c2269d3b473cc83687fd15af6b3b65b15d67a592ad`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 6.0 MB (5970309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64083097cffea937936c9ec17bfa648c81bbc71f8d05d684b7afb9e52a48d5c5`  
		Last Modified: Tue, 13 Jan 2026 04:01:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5966fa1c56255ac85fd3cda423eb24e7808ebd4ca2f9f0ea681e3e09bfc34`  
		Last Modified: Tue, 13 Jan 2026 04:00:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefc55a043cc735826153c6bbcbc2f26bc3b8b365fb9dd174493eeb4c568d44`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4dcfb61e511dc10991bc33f42e5660fc254fc795b9f1364f8f111b6a050be002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e6add496a0ab66cc6edaaa2ce6ffb23a10a39d16e78f5a6362f09a674985c2`

```dockerfile
```

-	Layers:
	-	`sha256:eea3a0edad86e0c342eb31d911134cbbf7295ec64067fb3bbfd4a1d860ccf606`  
		Last Modified: Tue, 13 Jan 2026 06:30:25 GMT  
		Size: 2.3 MB (2277355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0ea0b7db35baa06510b1a0264df2ddf0c3651935cfe0f32813ad862ea1efe8`  
		Last Modified: Tue, 13 Jan 2026 06:30:26 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:d3adf405db172cdb0926246543a6512e24c94c39d2c8f8fa6de24b4f4230f417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80942262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e134450b5ea6ce9b16abc2e430bd5deb9bcb6dbb166e9f8d53d29fdbad29a2c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 18:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 18:53:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 18:57:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 18:57:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 18:57:58 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 21:20:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 21:20:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 21:20:29 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 21:20:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 21:20:30 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 21:20:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 21:20:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 21:20:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 21:20:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 21:20:31 GMT
USER fluent
# Tue, 30 Dec 2025 21:20:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 21:20:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec427cb0f29aa78b3a35043f5c43e0a07e16cba482febff3fe2087900b8e01`  
		Last Modified: Tue, 30 Dec 2025 18:58:40 GMT  
		Size: 1.3 MB (1309698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119f3f7815c4977fbb7b151b6aaa8cf695081c5e63a241e7e8ccfa7cff83fcb`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6841342fbfd6bcc1a592039fcb307930a186477e89093dcc569ddb52f69b663`  
		Last Modified: Tue, 30 Dec 2025 18:58:42 GMT  
		Size: 39.5 MB (39519497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ecf017368e45fae8cb085ed7b4384c0e98da8232a690f0b6c1dffc3a99bb0`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c06a5efcd7af94fd4a7d702dddc472d60cb22b1ed26f26cf4b421e3c32f3f7f`  
		Last Modified: Tue, 30 Dec 2025 21:20:58 GMT  
		Size: 6.5 MB (6513782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d35286b4d75cd4ff6451e45864c1d79e0f811e301fe3b34540241af0a87d8`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534390e158cdb1f91f722d150993c5cd591cbefdc5b40262115b84a4c1977fe2`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1185bfeb67fbda08aa3f66a4c34eea27c0cf23ca82c32fb778f16b994d79f43`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2dfeb20c2fabcf019f75db5cb34b6d87d224cc95c8faad30eadc12a2d3cd89de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa85e5209179c6f949d0f2a73450f2b6a987ac9db17c829dac828f742025461`

```dockerfile
```

-	Layers:
	-	`sha256:44270606ed9db02298dbbf78bd7ae9bd926994714d651d08aa9afeca92bf8afa`  
		Last Modified: Wed, 31 Dec 2025 00:28:36 GMT  
		Size: 2.3 MB (2283640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ad2156a8f759a86af16633a4b90867f271a588d55694eccc556442f519404e`  
		Last Modified: Wed, 31 Dec 2025 00:28:37 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; s390x

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

### `fluentd:v1.19.0-1.0` - unknown; unknown

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

## `fluentd:v1.19.1-debian-1.0`

```console
$ docker pull fluentd@sha256:d3aa191d6f942c95058b251fb8e58db6afe19316a4f4b0a3ed70f3e6313af9f0
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

### `fluentd:v1.19.1-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:3bcde99e3687abecf27e8212ee5c19f0438469a5ddb314883fa63d5008311b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79169074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437e7a69cd621f6ebc46e4a9a1d50a934a36bacf8a69b345d7bddf67175aaa4d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:15:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:15:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:17:14 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:17:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:17:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:17:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:17:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:17:14 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:59:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:59:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:59:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:59:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:59:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:59:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:59:58 GMT
USER fluent
# Tue, 13 Jan 2026 04:59:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:59:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eef9b8933028d4d086fca9528ccc9271c5f7c65abfa73e952107ef4e71f5b`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 1.3 MB (1279374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef44c7bbb15316ed3c8b90e1149e7e65006f6a352bfbc150f83ba34cf36b8f0`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d36f3a5655a63fccdac1be1dea43008bf13f50700604d5bbb51dfd67c4f1`  
		Last Modified: Tue, 13 Jan 2026 03:17:34 GMT  
		Size: 42.1 MB (42112593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403786353912e853ee3b03de8484cf9cb0c6a860807846ff07bb720943ad0cc2`  
		Last Modified: Tue, 13 Jan 2026 03:17:30 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95a20976cd45bd6c70aafe68db5deac22d7041dcc4332f23f4371cfb918ba2`  
		Last Modified: Tue, 13 Jan 2026 05:00:25 GMT  
		Size: 6.0 MB (6001029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532f021056a355ffebc964ee6e349fc264a0ffdabb2e14ec25a50f2b008efe2`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8358e169dbb7ee057d2e5fe1001b6db5516639c6e88ed047dca2a65dfb01d`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988474eade660a7633fbfdad69c9a561ab991db1686c4ea44d2227977121d7`  
		Last Modified: Tue, 13 Jan 2026 05:00:23 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:40742be2e1f215c37553c2e750818bedea348558eef163d65e00231896a7e4c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247793a0a9928ab02b7e2013c0ae4ec3be4b506c0db291830b3dfe73be1323fc`

```dockerfile
```

-	Layers:
	-	`sha256:96f7d5ffebc16796703f3e1508ef6ed1867ff28f62d4ef6faf52f9f426b28892`  
		Last Modified: Tue, 13 Jan 2026 06:30:07 GMT  
		Size: 2.3 MB (2280167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d245ee90fda65ffc9ff75c6931bfb574b96d405448a7215873c5367f08bad`  
		Last Modified: Tue, 13 Jan 2026 06:30:07 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:f52d517870022f9ed7bffb4772dc8a2588760749e6605719195dcc85199a2d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73015490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05859ae973b197cc8a0246f09dcf7bea6bf454bb4ce55ee0ed5176fe0da576ac`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:23:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:26:30 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:26:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:30 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:30 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:30 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:26:30 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:38:08 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:38:08 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:38:08 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:38:08 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:38:08 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:38:08 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:38:08 GMT
USER fluent
# Tue, 13 Jan 2026 04:38:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:38:08 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1320c956f4c83fcb0562b315b8bda5dd174609e7d7ca750c0c5b25757c3a4e39`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 1.3 MB (1263009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4536c4a4c2b9a4b25706298eea75e411ecf7474ec825e95487a3fc45677109b`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6673c3e63216c5e4ec98fc85dddea075baddb32362e818e7ce47e7028fc26574`  
		Last Modified: Tue, 13 Jan 2026 03:26:50 GMT  
		Size: 37.9 MB (37905868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0676e2edb97826a7240b8e67fa4464779b809420476b9a092842c95228a68c2`  
		Last Modified: Tue, 13 Jan 2026 03:26:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e667d8c88075d8402d7e8e9d1c8a2e8d83d266277342528ad7324ce3d65eeb0a`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 5.9 MB (5901500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f0bd7482758a351bf2332fce7368df03d0fcd8fd2536fc8d4411ab00f82d04`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0417fc24ae33338c26093691d99cba4dc63c357664c86f9865b640d4718c7f`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ea0521b7ac5a88ea214f2aee9f3572ab1b928e8ec982413f551b5550b8d30c`  
		Last Modified: Tue, 13 Jan 2026 04:38:23 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b4949c17a66864f5b759d52baf0b5b56262328a7c5e00cb36f1b18651a3d1501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37f234ef4b0e2b6bc356defd5465da1e3f4900dab4f8d0d0f5ae950c385e12`

```dockerfile
```

-	Layers:
	-	`sha256:3de1fffa2b8ba00ff71bab251fe6d3cb80c93072d51e7b0f66fc50ba8d862863`  
		Last Modified: Tue, 13 Jan 2026 06:30:11 GMT  
		Size: 2.3 MB (2283138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a727fbbb6584143a529944a5a01d6a0f141ad05ecbf2c84f7030bb180513cf89`  
		Last Modified: Tue, 13 Jan 2026 06:30:12 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:d11673dae75290f1512772fbf2fccf20f343e5f35200b7242c5d64461cf9c7ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70883874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012e252ef68a7d2d9e65f9bd3e732c7a7a77c480ac76e2c262b317e71e3f404d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 04:01:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:01:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 04:03:55 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 04:03:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 04:03:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 04:03:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:03:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 04:03:55 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:52:53 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:52:53 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:52:53 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:52:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:52:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:52:53 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:52:53 GMT
USER fluent
# Tue, 13 Jan 2026 04:52:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:52:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb89ad4eba0f6c13ed221ba61cd63256963a2ae6022c5eb1a90dfe213d338e`  
		Last Modified: Tue, 13 Jan 2026 04:04:17 GMT  
		Size: 1.2 MB (1236555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4524518ebfe925ff0ba895a410f351e2ee7d22045883650d8b7fac782a9cc4c`  
		Last Modified: Tue, 13 Jan 2026 04:04:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafc5c289841a0fbb484e454157cfd1cd3e738994188089f928286b34c74f8`  
		Last Modified: Tue, 13 Jan 2026 04:04:25 GMT  
		Size: 37.8 MB (37767155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c4e1fbfecc70f8903b4522859b5ef39a5906274e2351951079ed8f886585`  
		Last Modified: Tue, 13 Jan 2026 04:04:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7740d7e2c777411352b0085fe0094c95668acdde8c6ece31de343123a5cf9`  
		Last Modified: Tue, 13 Jan 2026 04:53:08 GMT  
		Size: 5.7 MB (5669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2b431fd4058cc969b8cbb21b31aacdf5b6c415776385b9bd855de095a86be`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0486e503a316218c72159c4aecfd966c0227bea5022343f9e65a9bab48e9a294`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a8b50351ca059aa0d8b903508c9a57aa8984f21e7a73c28431739b765cabf`  
		Last Modified: Tue, 13 Jan 2026 04:53:07 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:28ce653f313504add74d6ae0ea8a60b536b728cce10f717c1b3b6b702df1a407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d63c54bd63cbb3caddc547142ff8e84bd64af8fa85b87fb1ad06e91d13c95c6`

```dockerfile
```

-	Layers:
	-	`sha256:1af10659db7793cb979bd306619dc8928e9299489553158805ffbdb212d7cabc`  
		Last Modified: Tue, 13 Jan 2026 06:30:16 GMT  
		Size: 2.3 MB (2281579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37545b709467be88ec29e37388b144288be9462833e3cab824fdb247fc368901`  
		Last Modified: Tue, 13 Jan 2026 06:30:17 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:2ba5ac0282f0a65ad95fc63a472a55621f2f4b0fcb0e0ce1160034733c471471
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79461765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a54308eb52c307d090b75de044c8eb95213037450e55a4d504e551dd7a804bc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:23:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 03:26:01 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 03:26:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 03:26:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:26:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 03:26:01 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 05:01:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 05:01:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 05:01:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 05:01:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 05:01:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 05:01:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 05:01:38 GMT
USER fluent
# Tue, 13 Jan 2026 05:01:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 05:01:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e0525c3d775730a255f13515eebc27444890213cd946823934e1e349ebf85d`  
		Last Modified: Tue, 13 Jan 2026 03:26:18 GMT  
		Size: 1.3 MB (1261687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afe863bf626435a4acc6286e46071f69c3c80a6a559f73494d100c77e2a459f`  
		Last Modified: Tue, 13 Jan 2026 03:25:50 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:505e6a88accd972129dcba73d3823653527e349b86bd85b23d7be05e6b7d131e`  
		Last Modified: Tue, 13 Jan 2026 03:26:20 GMT  
		Size: 42.1 MB (42074273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12087ea894d19fc0f651859b919a840ad2d733574392ff2bab6decc744d11ee`  
		Last Modified: Tue, 13 Jan 2026 03:26:18 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42466d7a4e7c4317a6aca126263010a1f5d4cbf475285844859615e6f8647cbc`  
		Last Modified: Tue, 13 Jan 2026 05:01:55 GMT  
		Size: 6.0 MB (5989373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd395c404a6148260abf43c4fc068f0b8cc16e4f0cc22e7e47f0d6861db9ec0c`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228cea3da2223620ff60c397a125f567c560bfabe61226b0b0a4ca0ee4e995a4`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423f136b4f2f4082396887c88c937d76864d24d7c3520bff51d342355d459f2a`  
		Last Modified: Tue, 13 Jan 2026 05:01:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:58ac976c6818af47fcc251821f582953708800364f8645c8c20db42650b6079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e553d3d1f1c6af6ffd1dbbc3cd00eddcf89a9244856d490e67448175ad2ae0cd`

```dockerfile
```

-	Layers:
	-	`sha256:c881d4ff0b96d3adb92b3f5d51324cd3000d2b17891c26d2344509210b0055c5`  
		Last Modified: Tue, 13 Jan 2026 06:30:21 GMT  
		Size: 2.3 MB (2280439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fac4b52effa78caa2eaab59f393d2747368a2723ded9da3da8999144a067da91`  
		Last Modified: Tue, 13 Jan 2026 06:30:21 GMT  
		Size: 21.5 KB (21456 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:90a276a23933880908550e3b249d0636588803070ad0cc3125c0650c1798c07d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76209821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eb7f8b78264676135dfddc1a5a8ea25db76afae7125f39945e3b100ac88217`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 02:47:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 02:49:26 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 02:49:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 02:49:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 02:49:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 02:49:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 02:49:26 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 04:00:27 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 04:00:27 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 04:00:27 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 04:00:27 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 04:00:27 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 04:00:27 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 04:00:27 GMT
USER fluent
# Tue, 13 Jan 2026 04:00:27 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 04:00:27 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca9739d6b026ec1d4cd350482fedc4374621d2428ab77e18051bdb8ca6c93a`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 1.3 MB (1287208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf308c9322d7b7ccb72a3b032126ea9174c0dd19d5133f792f459c5f0fec63`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077996a21b00611176c639502288dd2a7a31e063ef348d46a1652665d276aa0`  
		Last Modified: Tue, 13 Jan 2026 02:49:43 GMT  
		Size: 37.7 MB (37661435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f373e260e56fe68e120ff78469b633199ef4d7e6980f6c1706b0628c090ec`  
		Last Modified: Tue, 13 Jan 2026 02:49:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b70dc93001436daee4f4c2269d3b473cc83687fd15af6b3b65b15d67a592ad`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 6.0 MB (5970309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64083097cffea937936c9ec17bfa648c81bbc71f8d05d684b7afb9e52a48d5c5`  
		Last Modified: Tue, 13 Jan 2026 04:01:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5966fa1c56255ac85fd3cda423eb24e7808ebd4ca2f9f0ea681e3e09bfc34`  
		Last Modified: Tue, 13 Jan 2026 04:00:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefc55a043cc735826153c6bbcbc2f26bc3b8b365fb9dd174493eeb4c568d44`  
		Last Modified: Tue, 13 Jan 2026 04:00:48 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4dcfb61e511dc10991bc33f42e5660fc254fc795b9f1364f8f111b6a050be002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e6add496a0ab66cc6edaaa2ce6ffb23a10a39d16e78f5a6362f09a674985c2`

```dockerfile
```

-	Layers:
	-	`sha256:eea3a0edad86e0c342eb31d911134cbbf7295ec64067fb3bbfd4a1d860ccf606`  
		Last Modified: Tue, 13 Jan 2026 06:30:25 GMT  
		Size: 2.3 MB (2277355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0ea0b7db35baa06510b1a0264df2ddf0c3651935cfe0f32813ad862ea1efe8`  
		Last Modified: Tue, 13 Jan 2026 06:30:26 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:d3adf405db172cdb0926246543a6512e24c94c39d2c8f8fa6de24b4f4230f417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80942262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e134450b5ea6ce9b16abc2e430bd5deb9bcb6dbb166e9f8d53d29fdbad29a2c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 18:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 18:53:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 30 Dec 2025 18:57:57 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 30 Dec 2025 18:57:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 18:57:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 18:57:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 18:57:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 18:57:58 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 21:20:29 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 21:20:29 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 30 Dec 2025 21:20:29 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 30 Dec 2025 21:20:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 21:20:30 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 21:20:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 21:20:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 21:20:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 21:20:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 21:20:31 GMT
USER fluent
# Tue, 30 Dec 2025 21:20:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 21:20:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec427cb0f29aa78b3a35043f5c43e0a07e16cba482febff3fe2087900b8e01`  
		Last Modified: Tue, 30 Dec 2025 18:58:40 GMT  
		Size: 1.3 MB (1309698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a119f3f7815c4977fbb7b151b6aaa8cf695081c5e63a241e7e8ccfa7cff83fcb`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6841342fbfd6bcc1a592039fcb307930a186477e89093dcc569ddb52f69b663`  
		Last Modified: Tue, 30 Dec 2025 18:58:42 GMT  
		Size: 39.5 MB (39519497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02ecf017368e45fae8cb085ed7b4384c0e98da8232a690f0b6c1dffc3a99bb0`  
		Last Modified: Tue, 30 Dec 2025 18:58:39 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c06a5efcd7af94fd4a7d702dddc472d60cb22b1ed26f26cf4b421e3c32f3f7f`  
		Last Modified: Tue, 30 Dec 2025 21:20:58 GMT  
		Size: 6.5 MB (6513782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:706d35286b4d75cd4ff6451e45864c1d79e0f811e301fe3b34540241af0a87d8`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534390e158cdb1f91f722d150993c5cd591cbefdc5b40262115b84a4c1977fe2`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1185bfeb67fbda08aa3f66a4c34eea27c0cf23ca82c32fb778f16b994d79f43`  
		Last Modified: Tue, 30 Dec 2025 21:20:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2dfeb20c2fabcf019f75db5cb34b6d87d224cc95c8faad30eadc12a2d3cd89de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa85e5209179c6f949d0f2a73450f2b6a987ac9db17c829dac828f742025461`

```dockerfile
```

-	Layers:
	-	`sha256:44270606ed9db02298dbbf78bd7ae9bd926994714d651d08aa9afeca92bf8afa`  
		Last Modified: Wed, 31 Dec 2025 00:28:36 GMT  
		Size: 2.3 MB (2283640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14ad2156a8f759a86af16633a4b90867f271a588d55694eccc556442f519404e`  
		Last Modified: Wed, 31 Dec 2025 00:28:37 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; s390x

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

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

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
