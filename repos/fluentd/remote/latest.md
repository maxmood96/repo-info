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
