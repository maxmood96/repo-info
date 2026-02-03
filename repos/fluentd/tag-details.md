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
$ docker pull fluentd@sha256:af0791958bda6a479c153ca075b66f19cd40711fa78f77890c14e0e3f50a966c
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eef9b8933028d4d086fca9528ccc9271c5f7c65abfa73e952107ef4e71f5b`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 1.3 MB (1279374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef44c7bbb15316ed3c8b90e1149e7e65006f6a352bfbc150f83ba34cf36b8f0`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d36f3a5655a63fccdac1be1dea43008bf13f50700604d5bbb51dfd67c4f1`  
		Last Modified: Tue, 13 Jan 2026 03:17:24 GMT  
		Size: 42.1 MB (42112593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403786353912e853ee3b03de8484cf9cb0c6a860807846ff07bb720943ad0cc2`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95a20976cd45bd6c70aafe68db5deac22d7041dcc4332f23f4371cfb918ba2`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 6.0 MB (6001029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532f021056a355ffebc964ee6e349fc264a0ffdabb2e14ec25a50f2b008efe2`  
		Last Modified: Tue, 13 Jan 2026 05:00:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8358e169dbb7ee057d2e5fe1001b6db5516639c6e88ed047dca2a65dfb01d`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988474eade660a7633fbfdad69c9a561ab991db1686c4ea44d2227977121d7`  
		Last Modified: Tue, 13 Jan 2026 05:00:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 2.3 MB (2280167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d245ee90fda65ffc9ff75c6931bfb574b96d405448a7215873c5367f08bad`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:0268ca13bd306373fa628ffb063d494511eaea9240e44562752d0c95cbca83f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73024415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7328b17097e2e8bd9f392beb281688f548c4df6f7284c720119c0b2af899cd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:05:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:08:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:08:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:08:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:08:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:20:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:20:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 05:20:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:20:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:20:11 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:20:11 GMT
USER fluent
# Tue, 03 Feb 2026 05:20:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:20:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c14c6607560c7a97ca9cfcea3b52c3e76d7f20a7a35dfe9b77e8708dd1fb7a`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 1.3 MB (1263042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f3d0abef83d6f39ac1c802952a4c2d86bf87a3aab9c740d74354a361f3e897`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd1fa3197d5bf05a1ea42217fa36b4717385020eb13f031c4c543c880566c17`  
		Last Modified: Tue, 03 Feb 2026 04:08:14 GMT  
		Size: 37.9 MB (37905931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1bd1524e6a19a2549304082069b00ec1576b14900ad4203b654e6b5cd58179`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e401279a3be72d9dbf3322784bc98c9c917434f8ff60c4576b29520c00032c1`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 5.9 MB (5905492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9b508d832ed0b4b1485e4bd292145dd4102edda5951f954253bbae1a3074c9`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac904c03283287d26e5bd6fa8358575fe330fb80af609bf7864369f9eca5a3c`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0675a8863a728fff8eec1942fdb64861bf3eb25e8ca794b2b5b07ad7b2c7a0c`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:3ede44144d8ac305efa5d19e232a56a17d887d125b42b67bfcc9fbc2cb1a2f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3397f404daf080cec4b573b13c94a3a2fdda180b8b8c17fa9986a4c930dbcbc5`

```dockerfile
```

-	Layers:
	-	`sha256:8a0a68521f31754df0c2f4f6c4bc5c1ef3a8de07b01f4be9342b91cb40d27c94`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 2.3 MB (2283164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d150826744b8296099adc8263b7ea42fd2b939265f06ff5e8c9f80130b46dbb6`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb89ad4eba0f6c13ed221ba61cd63256963a2ae6022c5eb1a90dfe213d338e`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 1.2 MB (1236555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4524518ebfe925ff0ba895a410f351e2ee7d22045883650d8b7fac782a9cc4c`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafc5c289841a0fbb484e454157cfd1cd3e738994188089f928286b34c74f8`  
		Last Modified: Tue, 13 Jan 2026 04:04:06 GMT  
		Size: 37.8 MB (37767155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c4e1fbfecc70f8903b4522859b5ef39a5906274e2351951079ed8f886585`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7740d7e2c777411352b0085fe0094c95668acdde8c6ece31de343123a5cf9`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 5.7 MB (5669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2b431fd4058cc969b8cbb21b31aacdf5b6c415776385b9bd855de095a86be`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0486e503a316218c72159c4aecfd966c0227bea5022343f9e65a9bab48e9a294`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a8b50351ca059aa0d8b903508c9a57aa8984f21e7a73c28431739b765cabf`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 2.3 MB (2281579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37545b709467be88ec29e37388b144288be9462833e3cab824fdb247fc368901`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:393b40c65ea83034dac8a29e04ded08acdd09b849edb2470c55d8f37006e8428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79470598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae22c0ff3b2b2d113e9093561de35f509074c56e9c45ff9feddcbf5ae577038c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:29:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:29:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:29:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:29:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:30:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:30:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:30:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:30:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:30:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:30:22 GMT
USER fluent
# Tue, 03 Feb 2026 04:30:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:30:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31281d91ffa5f433313784df0c0ab0303ae74e32c5eda8b5ed5e2ebd226e1769`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 1.3 MB (1261309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d703736f2a80eda1164a8432ec78cbb829dbe3b051f6fb77c389472322fa01fb`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c91036fff8080ee027ae4f27750a5445ddcadec9de626473b6bdecfe894fc`  
		Last Modified: Tue, 03 Feb 2026 03:29:12 GMT  
		Size: 42.1 MB (42073926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed131edf8d7f65cd888be6678e899e156b9e716575f254ae37e5ba9f368acc`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb721bec1b751561b6777457ba90580423562c1aa7239410f12bba5d9201fca`  
		Last Modified: Tue, 03 Feb 2026 04:30:31 GMT  
		Size: 6.0 MB (5992899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551cdc25412e01b56a32cf31f8da37234b3859b3013e35daaff806b60cc00550`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f7e0cf6ef7ea5036dc344617893905cf6d6d512362eb3e38fc0d0dbc6bfc17`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97948803dcc2bcc57916b670d8982b6e3e12d244d9471073640caf04816c306`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:494d2cf3e7fac63e031e0c02319c428ce7420a9e254f5bb2c6e177f15bd2a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcd1a00cc12bca92e35286f8b0fe8d85c847108ab1c777c1f42d017794b5168`

```dockerfile
```

-	Layers:
	-	`sha256:fb768aabcf004fa31fe669d97982beccd8c2f5a8f37cc0122ef369dc39205c06`  
		Last Modified: Tue, 03 Feb 2026 04:30:31 GMT  
		Size: 2.3 MB (2280465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2c695d2b0f6ef93b2c0fc48f00af91038e73c664edc15c49233e7d78d4ca78`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 21.5 KB (21457 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca9739d6b026ec1d4cd350482fedc4374621d2428ab77e18051bdb8ca6c93a`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 1.3 MB (1287208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf308c9322d7b7ccb72a3b032126ea9174c0dd19d5133f792f459c5f0fec63`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077996a21b00611176c639502288dd2a7a31e063ef348d46a1652665d276aa0`  
		Last Modified: Tue, 13 Jan 2026 02:49:35 GMT  
		Size: 37.7 MB (37661435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f373e260e56fe68e120ff78469b633199ef4d7e6980f6c1706b0628c090ec`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b70dc93001436daee4f4c2269d3b473cc83687fd15af6b3b65b15d67a592ad`  
		Last Modified: Tue, 13 Jan 2026 04:00:39 GMT  
		Size: 6.0 MB (5970309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64083097cffea937936c9ec17bfa648c81bbc71f8d05d684b7afb9e52a48d5c5`  
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5966fa1c56255ac85fd3cda423eb24e7808ebd4ca2f9f0ea681e3e09bfc34`  
		Last Modified: Tue, 13 Jan 2026 04:00:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefc55a043cc735826153c6bbcbc2f26bc3b8b365fb9dd174493eeb4c568d44`  
		Last Modified: Tue, 13 Jan 2026 04:00:37 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 2.3 MB (2277355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0ea0b7db35baa06510b1a0264df2ddf0c3651935cfe0f32813ad862ea1efe8`  
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9a3cafd2ad15ecca523d44c12561730c9618fcb6a8a324c012616df63417cccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80944198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2391227cf9ff745e5a0ddc2e174b4f2162089c1f4a73ebfe775fe96933d8f3d7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:13:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 05:24:03 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 05:24:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 05:24:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 05:24:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 05:24:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:24:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 05:24:04 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 09:00:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 09:00:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 09:00:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 09:00:45 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 09:00:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 09:00:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 09:00:46 GMT
USER fluent
# Tue, 13 Jan 2026 09:00:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 09:00:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd359a7e5d3b012a0e1f773e5ca872b7185e1ae4c53f7a9a7d797ae3eaaf8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 1.3 MB (1309726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eeff64fa1ee2c5a20375771788d22ec3d5ad95481b75598a70ada63b47d8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5604be4a4b60f4fed68c22b913b07851aa0414cc66ee4da7ee7c4338b2e5d28e`  
		Last Modified: Tue, 13 Jan 2026 05:24:26 GMT  
		Size: 39.5 MB (39519922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc1dc23f8783cc9ad3639c62138f859289801c771b5a9e82fd86f8e4e4f7d19`  
		Last Modified: Tue, 13 Jan 2026 05:24:25 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e30a59d33d2a25b91e6031d498d0e8223513a391ec9a792eea32735baa9de15`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 6.5 MB (6516555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f924ba79838c3e65a0a1331631e11f5844fcff2d3c1c940dc123fab38974a2`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c3db13e0b69bf0fb77f89fca056dada7d7cf70bfe910ac9c2a95048d221003`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb4153c5f33f3ac2b2b9dd2e803c3ed885e8990d990b99f7d129ee38342af3c`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:0032be699998ed132a2460102525b0fc79f3749b8ae840292df4cfbe7d33dbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a97bdbdb1fc3ecd09b897233c3be4d5e82e7331f90aa9d007be0b7e8e5f1f1`

```dockerfile
```

-	Layers:
	-	`sha256:ccfacc43efb7a135d5fb8cba44cce1125970f2e76f94c86a2e668fa770ee3eb9`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 2.3 MB (2283702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7b890f4811a2723a742990c05386c8fff28e65cec0ee2946431c1b38970752`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:b1c8103ef9d6bd1a2d4acaa83c631bdc92e00a34026c88d668605aaaf50a9084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76705553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80b4cea4899143ffdc5ffd2fa8c5c6324ee8452ca49c9136d94a09fcf89d1dc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:53:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:53:52 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 06:00:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 06:00:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 06:00:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 06:00:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 06:00:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 06:00:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 06:00:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 06:00:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 06:00:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 06:00:36 GMT
USER fluent
# Tue, 03 Feb 2026 06:00:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 06:00:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0ef58ef1eb78dd947e41fe50adfe7b4ab7ed59de6adb1cee9b213c29193b84`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 1.3 MB (1294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6191cacf2fcbd60736c6c6dd3a35edf5fb265ba19e0504896f4a96d590bdc0`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2e7a1acf75697b829c5674d2af59db59b82bd932f96d1c50df559112643e50`  
		Last Modified: Tue, 03 Feb 2026 04:54:07 GMT  
		Size: 39.2 MB (39191476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27dcf4be1994bc1f0cbe0b29edacbaeb7643532854664d63ed921b9823209fe`  
		Last Modified: Tue, 03 Feb 2026 04:54:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8836a2a3d5fe0612bd6f486ccf67502c90dca13b55f0ee3015dc8fc9b6dcb80d`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 6.4 MB (6379016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ab910ede55a870b32fe8533f6e8da853c247e99cabc2a0d54ea29e1f21a75a`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18813b9ae4d1bc8ed0dea132c93ede5766cd2fd64a961a8f60770e1163afd0a4`  
		Last Modified: Tue, 03 Feb 2026 06:00:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d235fff2840bba22a65cc11d16cfc6c02d9b103745e92481615dde3a9ec9bfca`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:833aa0335c34fbde7814ce09c890b3155346bc8500bd98a346ce1c02d8a7f823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f3e40c9d0bd52e3f4614bf12dbb9e2b426d8aa9e7c2e702cad2ffbec47004`

```dockerfile
```

-	Layers:
	-	`sha256:a03784ba6816bc7a3f5cc90a89bd87aeda3703bd11775b3e06f739dde63954f0`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 2.3 MB (2281638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39680257795ba8f20d5fa4200ee53f00d46bef5378ad0a8ad8fd43a097220b5d`  
		Last Modified: Tue, 03 Feb 2026 06:00:51 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:62336e643c39cdf540181c4dde19d577296e133b9f1210e7dd860a0087d3fcd4
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
$ docker pull fluentd@sha256:e41aea73fe3f1a66a30ae7c2683aedfecdcb14c886cf4bc8bba913741149bfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82043649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71830f9ed37e2ef95e88015a6a0e0f46d65926ea06456b0ed47894646c2b3fc9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:33:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:33:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:35:44 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:35:44 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:35:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:35:44 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:35:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:35:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:35:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:35:44 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:02:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jan 2026 18:02:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 14 Jan 2026 18:02:21 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jan 2026 18:02:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 14 Jan 2026 18:02:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 14 Jan 2026 18:02:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 14 Jan 2026 18:02:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 14 Jan 2026 18:02:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jan 2026 18:02:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jan 2026 18:02:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 14 Jan 2026 18:02:21 GMT
USER fluent
# Wed, 14 Jan 2026 18:02:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jan 2026 18:02:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992d85d4bb153b953b57ccc4ad423d042837aeba10255d229ae9a12a47bdea6`  
		Last Modified: Wed, 14 Jan 2026 17:35:54 GMT  
		Size: 3.5 MB (3509960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f8207ae9bcf98be8497b1a7fa74edb6df1804b698df6cebf00a2256c10d06d`  
		Last Modified: Wed, 14 Jan 2026 17:35:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc2145f95b9316ebbbf5428843e5d4a983e07877d6697399deea1ca33e04fca`  
		Last Modified: Wed, 14 Jan 2026 17:35:55 GMT  
		Size: 36.0 MB (36010912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11116098be267a65bdfbb06c327810aed28e5711f8ef8176502171556752a64`  
		Last Modified: Wed, 14 Jan 2026 17:35:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45db91b52f9cfe35a45db235cdee1895feab5807ca555c67707fe6ce075f90e`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 14.3 MB (14291814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493b35168a2436a5be2e0afee195d3a03e1ca54d03caa50f3c4ac7114411ffd0`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dff2234c592858a60c368f818eb99637ebbc65e2e9de3cba207a78e5b29f88`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bedce329989e41986a23203fb666eccf4860b791064226139f35e386f76f601`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1e0f32f35cf0364fcefd315929f831e5c8607753f36f895a86890de022254960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b060272aabc7fc9a2d1f7088b1d9d72a0c51866025ab0fdd212f6730615f45b`

```dockerfile
```

-	Layers:
	-	`sha256:293eae66fcafc83ac6cee7db8117b33ea4d008c58a89f36b470d3218713fe1b2`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb37ad55300ab9599cc38c7e888a386ab0cbb750de9a31e070877cac08a9387`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:c3b1eb72029705ccf4fbd7b6f16864fb5e12da05105c7ef795a356ae1d470e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75442097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3c59a9ed1744560e1c0bce5b82b98f03020189ba94ba31b6e91f8c1ce75610`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:06:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:11:26 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:11:26 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 04:11:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 04:11:26 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 04:11:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:11:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:11:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:11:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:11:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:11:26 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:19:52 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:19:52 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 05:19:52 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 05:19:52 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 05:19:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:19:53 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:19:53 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:19:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:19:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:19:53 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:19:53 GMT
USER fluent
# Tue, 03 Feb 2026 05:19:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:19:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6036aff531a372e1e9da48952322760c8c052f6735e66afd3251a32e5baace8d`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 25.8 MB (25757618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11754fc02e250c6c3c541c9c5d138d03a1d904951e1d30d4b3618bcc766fed9`  
		Last Modified: Tue, 03 Feb 2026 04:08:56 GMT  
		Size: 3.1 MB (3081090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3b441dd8e08320aa3d5f6a993764b26d7bd11ad068454631f6bb82fc90a4c8`  
		Last Modified: Tue, 03 Feb 2026 04:08:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c314a851cb76aa38bf99afb5a54cf327caa461cb653fdcc0c2aeb06202600f3`  
		Last Modified: Tue, 03 Feb 2026 04:11:35 GMT  
		Size: 32.3 MB (32330996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c829a989076bb857ef42e869c57e4097fc8b826d73812704410000c1b92c3e6f`  
		Last Modified: Tue, 03 Feb 2026 04:11:34 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d099fbbbf609240e19594bddb3fb2ff047f9ba92d2eefb666ccf023aadf1335e`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 14.3 MB (14269992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dc12ab8dbdeb1bb53f466479076b590d6b8184c9c1cd365984ee10d076690c`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd20f24277da591e86ae1872cb3eab72087731b6e684aa6bc689170bb3ccc32`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504df15bfee113910dc7529c871b8fcce28139d4d8ecff362ff218aab199d78b`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:39e92eaf7f8b1360fc13993a6a2c8af88e3f882212e0c13129e4a6cc1cb09a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca45ff357e10d1a35040c2ca1e2819c335bc748826b0b9f65d21c8b6dd6a3aa3`

```dockerfile
```

-	Layers:
	-	`sha256:8694a7b769151706efa904fa8b3e284171ddd48f782886f7cf7eb8bc7117b427`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 2.7 MB (2674277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8170f3a662219b51bd8cdbdb472918e9f3555d6b1a47679c193dbf39bb408323`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f12dc446d50ae437fcb96a3f456f3c5ae955760ea727934df90d4b2e5ecf5b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73216873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8647b8e5b10174aa105f2c269097d639b33a9534836939d5af73ceaa69b81877`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:33:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:35:51 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:35:51 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:35:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:35:51 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:35:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:35:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:35:51 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:35:51 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:07:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jan 2026 18:07:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 14 Jan 2026 18:07:19 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jan 2026 18:07:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 14 Jan 2026 18:07:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 14 Jan 2026 18:07:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 14 Jan 2026 18:07:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 14 Jan 2026 18:07:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jan 2026 18:07:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jan 2026 18:07:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 14 Jan 2026 18:07:20 GMT
USER fluent
# Wed, 14 Jan 2026 18:07:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jan 2026 18:07:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bf99e624f48fb7f11d92926014124333deec81b36a9ccd999d1842139fe22d`  
		Last Modified: Wed, 14 Jan 2026 17:36:01 GMT  
		Size: 2.9 MB (2913517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1544acf04562f4514e672d1a2f75a870b2aafb8b1a0cd3e74f8c5263cc6ab8`  
		Last Modified: Wed, 14 Jan 2026 17:36:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c33c777e42fded3b5f5b2856e6afef883f77414170170016846e32d70b673`  
		Last Modified: Wed, 14 Jan 2026 17:36:02 GMT  
		Size: 32.2 MB (32167678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb85378b7a191212c5b5565e5c7d410bc801af4c95d436fd0ce2869c525c0dd8`  
		Last Modified: Wed, 14 Jan 2026 17:36:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa2c7d6745f0cd4626efe869f24ce7bdb15a9a91e6f8fe6778172d6e4095318`  
		Last Modified: Wed, 14 Jan 2026 18:07:29 GMT  
		Size: 14.2 MB (14199171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67b6e9a6106d21cd23ee4b528c4e17735eeea2e66b5ce650cbd584da74e90cc`  
		Last Modified: Wed, 14 Jan 2026 18:07:28 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4f434167d16730375d1e40294f7109908519e7aa9691ae7ebeaea9ec5d95b`  
		Last Modified: Wed, 14 Jan 2026 18:07:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26bf48a1d8d164d3b461bad322266b4a020e91f7ca9e7c415a5f2c15663b394`  
		Last Modified: Wed, 14 Jan 2026 18:07:29 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:586d0ad31a66c350462527c3da65e22bc1d8bf97ec13c6dd7fdf60d79d342da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db67c22d67d75dbab102a8ef0be3be8f11e9edb4495ab0a08a78168a6a87ce3d`

```dockerfile
```

-	Layers:
	-	`sha256:cee651b50c9fb865d920c4a326d8bb3aae3e200af3977cd98bccf09a7271b946`  
		Last Modified: Wed, 14 Jan 2026 18:07:29 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9519d9c54b424f381cbc2e94b8dd11510113dfb508ae403ab46cb089a14c1afe`  
		Last Modified: Wed, 14 Jan 2026 18:07:28 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:45ada0546d2defd86306433d46a62fdf9ac0caba436f88912adbf0de973fc71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81661276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274c70e85d8c78644e0ecbaf9d03547e0c94448a4694e66554f5d0348523b28f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:17:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:19:55 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:19:55 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 03:19:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 03:19:55 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 03:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:19:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:19:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:19:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:19:56 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:30:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:30:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 04:30:17 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 04:30:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 04:30:17 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:30:17 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:30:17 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:30:17 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:30:17 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:30:17 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:30:17 GMT
USER fluent
# Tue, 03 Feb 2026 04:30:17 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:30:17 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0e9ddb05a323650c6ccaf3e49a9ce5e875c85339d1b3473e2dbee41a0a0c78`  
		Last Modified: Tue, 03 Feb 2026 03:20:05 GMT  
		Size: 3.3 MB (3341532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07293464e6c66c26eac167023b5b9d3789c082cdd43d099814e91e49c9d4d466`  
		Last Modified: Tue, 03 Feb 2026 03:20:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ccfad005922b0aafa4dad82bd47b8978c6cf1648758f454c244c557f5d1f72`  
		Last Modified: Tue, 03 Feb 2026 03:20:06 GMT  
		Size: 35.9 MB (35911835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f2c5d333ddb51a851aa30046969ba5958048b4f17110723cfe8add8036db90`  
		Last Modified: Tue, 03 Feb 2026 03:20:05 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d52e3857918c13fa3f684610d25461842622fcc7b5825ca1d20e8b5ad25677`  
		Last Modified: Tue, 03 Feb 2026 04:30:27 GMT  
		Size: 14.3 MB (14297685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb2d647140bc01d29b1b198669e9daa991f1bcf76989a5fa065107029da1170`  
		Last Modified: Tue, 03 Feb 2026 04:30:26 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561e80f37c011788d7200b5455a909968dbafc6a7f4581fbc4210be7f51071f3`  
		Last Modified: Tue, 03 Feb 2026 04:30:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61141732b10fb67faa20aa79c2416e35fbe1d668d29b5c2e4bfe57ca8b7da689`  
		Last Modified: Tue, 03 Feb 2026 04:30:26 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f5327fd71974d6ed16af8ca103330a4d218a9c33232f03a9f7514be4e7f712c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1d108c9d476f04bded3391e7889d9d7be94d2587ac3e23eab089f0442a9624`

```dockerfile
```

-	Layers:
	-	`sha256:368002be62137654a9e83c0a4d78846d701e974bb0892006414afe47cf582f6b`  
		Last Modified: Tue, 03 Feb 2026 04:30:26 GMT  
		Size: 2.7 MB (2670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262c0f95c03857683b26b61eb67d8305c59b1500a760369fa82ff1b2d4bc2840`  
		Last Modified: Tue, 03 Feb 2026 04:30:26 GMT  
		Size: 21.2 KB (21167 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:90f1c24b257c53b6410d0d97f1b98ebc48f67fcce63ce16550733f8075fb8428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78968250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd0c32127a25a0f7c604fcbf6f9ecc7942beb972b23ca2385806972efc4961e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:32:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:32:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:34:31 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:34:31 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:34:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:34:31 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:34:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:34:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:34:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:34:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:34:31 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:34:31 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 17:56:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jan 2026 17:56:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 14 Jan 2026 17:56:35 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jan 2026 17:56:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 14 Jan 2026 17:56:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 14 Jan 2026 17:56:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 14 Jan 2026 17:56:35 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 14 Jan 2026 17:56:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jan 2026 17:56:35 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jan 2026 17:56:35 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 14 Jan 2026 17:56:35 GMT
USER fluent
# Wed, 14 Jan 2026 17:56:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jan 2026 17:56:35 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:37 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9664d00f2ac07f1a53ca39e59420e0ad3b6d744a8e067b9b3a188609503eb53f`  
		Last Modified: Wed, 14 Jan 2026 17:34:41 GMT  
		Size: 3.5 MB (3512267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d1341420adb4e4c0776dbc2c45d78e4e46e5bbd4f04b0c31a49bbe15301989`  
		Last Modified: Wed, 14 Jan 2026 17:34:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2403fe3099c18d48da4cc7428c35b8a06c8863adb203a578ac9e16bcbdb405`  
		Last Modified: Wed, 14 Jan 2026 17:34:42 GMT  
		Size: 32.2 MB (32162614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4bf5f4010fca07e2de4b4dd7164f04c8ed771d92761739e7d43985c46b87c`  
		Last Modified: Wed, 14 Jan 2026 17:34:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301ba55b0e9384b0f71fdc19593d594ea08b47b1f910a513a829d0daef6304ef`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 14.1 MB (14080908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc3dab1e46344e84038b20f06abd8d431857e123dd62c84c7f7d039033d4513`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f866d64dba5c97eb9b1a6ed9307ffbc7a8ee753135b2349565566c76cdf0b13`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39356656143ad5c7597dbd1adbab41ed8ec0218f400a8e928df5e0366af73526`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:33c7fda88ba71531cdae91cdef4bbe85272adcc8f3f49ae22941411aadde079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f449b8c8b811820cbe784f0b50667ecaed09fd61a0f23ff8e7865b819ada420e`

```dockerfile
```

-	Layers:
	-	`sha256:20de6d15d9c0c430cc3a4c29893b2be6434d2e7f25cac8508eb89faa582f28af`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822d1cda5364d5d65c63acd2ac8f66231a29afc704a4c1585244345adefd8376`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 21.0 KB (21048 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9aa1d8c59752e4ffe06bcbd93b654bf17427879fb102d3a528e2b707ff363670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84303585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aaad992c9da5ed4deb21f2f7658acf817cd344e4f038754b88d6408c8d57502`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 02:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 02:40:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:41:02 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:41:02 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:41:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:41:02 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:41:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:41:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:41:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:41:02 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:41:02 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:46:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jan 2026 18:46:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 14 Jan 2026 18:46:35 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jan 2026 18:46:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 14 Jan 2026 18:46:37 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 14 Jan 2026 18:46:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 14 Jan 2026 18:46:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 14 Jan 2026 18:46:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jan 2026 18:46:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jan 2026 18:46:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 14 Jan 2026 18:46:38 GMT
USER fluent
# Wed, 14 Jan 2026 18:46:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jan 2026 18:46:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d040954f92ec97ea46ab26dcebf24a6ab2cc0e67f210bcce8bcb9dfb1faf77d6`  
		Last Modified: Wed, 14 Jan 2026 02:45:47 GMT  
		Size: 3.7 MB (3710271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9425bbafe39445bfc1ee834ed06db5e9c79e7483c2092810ffa256366c90b303`  
		Last Modified: Wed, 14 Jan 2026 02:45:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1227467ea0a824b18cf8aa0feb4b8b88b12384ba6539b2279092a31ec152162`  
		Last Modified: Wed, 14 Jan 2026 17:41:23 GMT  
		Size: 33.8 MB (33835867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06452470b4f462b81916f910dcdb89d1cbe76c38cd2a514358235fa72b8c21ae`  
		Last Modified: Wed, 14 Jan 2026 17:41:22 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663bb1414c8ccf30d8a816feb837edf44f968a6f065990af50bf5113301302bf`  
		Last Modified: Wed, 14 Jan 2026 18:47:02 GMT  
		Size: 14.7 MB (14686336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ca28754e30f055163ea627dcf14ba1dfa6cb5b375d50cb2ead5e4f63c23d62`  
		Last Modified: Wed, 14 Jan 2026 18:47:01 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8374192cc1f039a313736531286e52212534e91e611ba8ab608d334b22325b2d`  
		Last Modified: Wed, 14 Jan 2026 18:47:02 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c3b58d484d6b38343232ed48eca74819290dc5802066753fbf433f84a09e53`  
		Last Modified: Wed, 14 Jan 2026 18:47:01 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:92d357946fc2f973700b93554209c7268eabeabc0217d5ccfca60a05244fb384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a4c9ff427cbe0b1fc80626d1165ccbdb45c00838c0e49bb3907702ad5345c`

```dockerfile
```

-	Layers:
	-	`sha256:6bd73a9eaa3c79f705a170038cfc1d86c861cd25ab3672dd6354ef9fff564ed9`  
		Last Modified: Wed, 14 Jan 2026 18:47:02 GMT  
		Size: 2.7 MB (2674899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c3268d6b5c7ddbc9d1b51c0689637ab55179d48bb38d86d87bff2b903057bb`  
		Last Modified: Wed, 14 Jan 2026 18:47:01 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:70ffa14741aed127fe3c56aa5cd7128d493308bcdb8f4b4849074ca35badbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77588305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3a07efd5dd81993b0725e09910f685080fe53a0a93b6d0e3f7bf7aadc79bed`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:52:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:52:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:58:03 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:58:03 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 04:58:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 04:58:03 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 04:58:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:58:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:58:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:58:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:58:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:58:03 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 06:00:45 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 06:00:45 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 06:00:45 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 06:00:45 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 06:00:45 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 06:00:45 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 06:00:45 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 06:00:45 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 06:00:45 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 06:00:45 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 06:00:45 GMT
USER fluent
# Tue, 03 Feb 2026 06:00:45 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 06:00:45 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc41c1d20b68f1c7cbc98a19ce5b004fd426fc43dfdbee515f6d7b7f0b1a707`  
		Last Modified: Tue, 03 Feb 2026 04:55:38 GMT  
		Size: 3.2 MB (3171220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5f75f806d81ea37b8bca52c14c79c6d82a5fdc3cd7d255dc26352dd8b60a70`  
		Last Modified: Tue, 03 Feb 2026 04:55:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd4a6b6b71aefcebd8f7627a0c725eea4604094c4881b50115cb2183ff546a3`  
		Last Modified: Tue, 03 Feb 2026 04:58:17 GMT  
		Size: 33.1 MB (33103783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a208f8482e16e8115945c42792b6f9d69029a05cb09bc03b44a5d09299d152`  
		Last Modified: Tue, 03 Feb 2026 04:58:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f33c782dfcc09f11053485a946a254f46710ea633857edc0bdb82fafb43ea61`  
		Last Modified: Tue, 03 Feb 2026 06:00:59 GMT  
		Size: 14.4 MB (14426523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db49dff94be9b5f64fd1c78b8b5aef4229323d122606e740f568afc53319ae2`  
		Last Modified: Tue, 03 Feb 2026 06:00:59 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3d3d88c51398d874ec4c9260c9032207fbde2e54434eeeed6d486b9c6ae5a6`  
		Last Modified: Tue, 03 Feb 2026 06:00:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4c39f33fb4f2a94db43770cd936a761f15a284d236ca62b1d7829a085109f8`  
		Last Modified: Tue, 03 Feb 2026 06:00:58 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c4bacac5a1cdfb382fb0b9e6561c36fb31cb03cef91c7854cd6c33e41559f506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ddb98d78da7d91cf3805580573840a449447742bd39ecfcac6d9760673a2ee`

```dockerfile
```

-	Layers:
	-	`sha256:008d8bbb6bc5904b04a1c49e7a708386ba9c5501595d4d51e9e28cfb791ce6a2`  
		Last Modified: Tue, 03 Feb 2026 06:01:02 GMT  
		Size: 2.7 MB (2667307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f752b3f959cf2579075e87717de427972e6c191c043a7c97a8e6ded30d0d4d19`  
		Last Modified: Tue, 03 Feb 2026 06:00:59 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.11-debian-1.0`

```console
$ docker pull fluentd@sha256:62336e643c39cdf540181c4dde19d577296e133b9f1210e7dd860a0087d3fcd4
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
$ docker pull fluentd@sha256:e41aea73fe3f1a66a30ae7c2683aedfecdcb14c886cf4bc8bba913741149bfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82043649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71830f9ed37e2ef95e88015a6a0e0f46d65926ea06456b0ed47894646c2b3fc9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:33:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:33:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:35:44 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:35:44 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:35:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:35:44 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:35:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:35:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:35:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:35:44 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:02:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jan 2026 18:02:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 14 Jan 2026 18:02:21 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jan 2026 18:02:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 14 Jan 2026 18:02:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 14 Jan 2026 18:02:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 14 Jan 2026 18:02:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 14 Jan 2026 18:02:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jan 2026 18:02:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jan 2026 18:02:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 14 Jan 2026 18:02:21 GMT
USER fluent
# Wed, 14 Jan 2026 18:02:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jan 2026 18:02:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:44 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b992d85d4bb153b953b57ccc4ad423d042837aeba10255d229ae9a12a47bdea6`  
		Last Modified: Wed, 14 Jan 2026 17:35:54 GMT  
		Size: 3.5 MB (3509960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f8207ae9bcf98be8497b1a7fa74edb6df1804b698df6cebf00a2256c10d06d`  
		Last Modified: Wed, 14 Jan 2026 17:35:54 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc2145f95b9316ebbbf5428843e5d4a983e07877d6697399deea1ca33e04fca`  
		Last Modified: Wed, 14 Jan 2026 17:35:55 GMT  
		Size: 36.0 MB (36010912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11116098be267a65bdfbb06c327810aed28e5711f8ef8176502171556752a64`  
		Last Modified: Wed, 14 Jan 2026 17:35:54 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45db91b52f9cfe35a45db235cdee1895feab5807ca555c67707fe6ce075f90e`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 14.3 MB (14291814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493b35168a2436a5be2e0afee195d3a03e1ca54d03caa50f3c4ac7114411ffd0`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dff2234c592858a60c368f818eb99637ebbc65e2e9de3cba207a78e5b29f88`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bedce329989e41986a23203fb666eccf4860b791064226139f35e386f76f601`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1e0f32f35cf0364fcefd315929f831e5c8607753f36f895a86890de022254960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b060272aabc7fc9a2d1f7088b1d9d72a0c51866025ab0fdd212f6730615f45b`

```dockerfile
```

-	Layers:
	-	`sha256:293eae66fcafc83ac6cee7db8117b33ea4d008c58a89f36b470d3218713fe1b2`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb37ad55300ab9599cc38c7e888a386ab0cbb750de9a31e070877cac08a9387`  
		Last Modified: Wed, 14 Jan 2026 18:02:30 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:c3b1eb72029705ccf4fbd7b6f16864fb5e12da05105c7ef795a356ae1d470e3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75442097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad3c59a9ed1744560e1c0bce5b82b98f03020189ba94ba31b6e91f8c1ce75610`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:06:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:06:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:11:26 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:11:26 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 04:11:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 04:11:26 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 04:11:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:11:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:11:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:11:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:11:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:11:26 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:19:52 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:19:52 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 05:19:52 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 05:19:52 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 05:19:53 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:19:53 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:19:53 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:19:53 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:19:53 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:19:53 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:19:53 GMT
USER fluent
# Tue, 03 Feb 2026 05:19:53 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:19:53 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6036aff531a372e1e9da48952322760c8c052f6735e66afd3251a32e5baace8d`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 25.8 MB (25757618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11754fc02e250c6c3c541c9c5d138d03a1d904951e1d30d4b3618bcc766fed9`  
		Last Modified: Tue, 03 Feb 2026 04:08:56 GMT  
		Size: 3.1 MB (3081090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3b441dd8e08320aa3d5f6a993764b26d7bd11ad068454631f6bb82fc90a4c8`  
		Last Modified: Tue, 03 Feb 2026 04:08:55 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c314a851cb76aa38bf99afb5a54cf327caa461cb653fdcc0c2aeb06202600f3`  
		Last Modified: Tue, 03 Feb 2026 04:11:35 GMT  
		Size: 32.3 MB (32330996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c829a989076bb857ef42e869c57e4097fc8b826d73812704410000c1b92c3e6f`  
		Last Modified: Tue, 03 Feb 2026 04:11:34 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d099fbbbf609240e19594bddb3fb2ff047f9ba92d2eefb666ccf023aadf1335e`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 14.3 MB (14269992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dc12ab8dbdeb1bb53f466479076b590d6b8184c9c1cd365984ee10d076690c`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd20f24277da591e86ae1872cb3eab72087731b6e684aa6bc689170bb3ccc32`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504df15bfee113910dc7529c871b8fcce28139d4d8ecff362ff218aab199d78b`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:39e92eaf7f8b1360fc13993a6a2c8af88e3f882212e0c13129e4a6cc1cb09a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca45ff357e10d1a35040c2ca1e2819c335bc748826b0b9f65d21c8b6dd6a3aa3`

```dockerfile
```

-	Layers:
	-	`sha256:8694a7b769151706efa904fa8b3e284171ddd48f782886f7cf7eb8bc7117b427`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 2.7 MB (2674277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8170f3a662219b51bd8cdbdb472918e9f3555d6b1a47679c193dbf39bb408323`  
		Last Modified: Tue, 03 Feb 2026 05:20:01 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:f12dc446d50ae437fcb96a3f456f3c5ae955760ea727934df90d4b2e5ecf5b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73216873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8647b8e5b10174aa105f2c269097d639b33a9534836939d5af73ceaa69b81877`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:33:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:35:51 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:35:51 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:35:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:35:51 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:35:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:35:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:35:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:35:51 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:35:51 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:07:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jan 2026 18:07:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 14 Jan 2026 18:07:19 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jan 2026 18:07:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 14 Jan 2026 18:07:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 14 Jan 2026 18:07:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 14 Jan 2026 18:07:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 14 Jan 2026 18:07:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jan 2026 18:07:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jan 2026 18:07:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 14 Jan 2026 18:07:20 GMT
USER fluent
# Wed, 14 Jan 2026 18:07:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jan 2026 18:07:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ce9b9afe4e779d4b89f92e338fcd7dde1b11be3e68cd4c559a53dc9328ce4b5e`  
		Last Modified: Tue, 13 Jan 2026 00:42:03 GMT  
		Size: 23.9 MB (23934118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bf99e624f48fb7f11d92926014124333deec81b36a9ccd999d1842139fe22d`  
		Last Modified: Wed, 14 Jan 2026 17:36:01 GMT  
		Size: 2.9 MB (2913517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1544acf04562f4514e672d1a2f75a870b2aafb8b1a0cd3e74f8c5263cc6ab8`  
		Last Modified: Wed, 14 Jan 2026 17:36:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664c33c777e42fded3b5f5b2856e6afef883f77414170170016846e32d70b673`  
		Last Modified: Wed, 14 Jan 2026 17:36:02 GMT  
		Size: 32.2 MB (32167678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb85378b7a191212c5b5565e5c7d410bc801af4c95d436fd0ce2869c525c0dd8`  
		Last Modified: Wed, 14 Jan 2026 17:36:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa2c7d6745f0cd4626efe869f24ce7bdb15a9a91e6f8fe6778172d6e4095318`  
		Last Modified: Wed, 14 Jan 2026 18:07:29 GMT  
		Size: 14.2 MB (14199171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67b6e9a6106d21cd23ee4b528c4e17735eeea2e66b5ce650cbd584da74e90cc`  
		Last Modified: Wed, 14 Jan 2026 18:07:28 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4f434167d16730375d1e40294f7109908519e7aa9691ae7ebeaea9ec5d95b`  
		Last Modified: Wed, 14 Jan 2026 18:07:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26bf48a1d8d164d3b461bad322266b4a020e91f7ca9e7c415a5f2c15663b394`  
		Last Modified: Wed, 14 Jan 2026 18:07:29 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:586d0ad31a66c350462527c3da65e22bc1d8bf97ec13c6dd7fdf60d79d342da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db67c22d67d75dbab102a8ef0be3be8f11e9edb4495ab0a08a78168a6a87ce3d`

```dockerfile
```

-	Layers:
	-	`sha256:cee651b50c9fb865d920c4a326d8bb3aae3e200af3977cd98bccf09a7271b946`  
		Last Modified: Wed, 14 Jan 2026 18:07:29 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9519d9c54b424f381cbc2e94b8dd11510113dfb508ae403ab46cb089a14c1afe`  
		Last Modified: Wed, 14 Jan 2026 18:07:28 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:45ada0546d2defd86306433d46a62fdf9ac0caba436f88912adbf0de973fc71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81661276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274c70e85d8c78644e0ecbaf9d03547e0c94448a4694e66554f5d0348523b28f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:17:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:17:50 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:19:55 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:19:55 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 03:19:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 03:19:55 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 03:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:19:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:19:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:19:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:19:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:19:56 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:30:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:30:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 04:30:17 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 04:30:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 04:30:17 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:30:17 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:30:17 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:30:17 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:30:17 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:30:17 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:30:17 GMT
USER fluent
# Tue, 03 Feb 2026 04:30:17 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:30:17 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0e9ddb05a323650c6ccaf3e49a9ce5e875c85339d1b3473e2dbee41a0a0c78`  
		Last Modified: Tue, 03 Feb 2026 03:20:05 GMT  
		Size: 3.3 MB (3341532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07293464e6c66c26eac167023b5b9d3789c082cdd43d099814e91e49c9d4d466`  
		Last Modified: Tue, 03 Feb 2026 03:20:05 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ccfad005922b0aafa4dad82bd47b8978c6cf1648758f454c244c557f5d1f72`  
		Last Modified: Tue, 03 Feb 2026 03:20:06 GMT  
		Size: 35.9 MB (35911835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f2c5d333ddb51a851aa30046969ba5958048b4f17110723cfe8add8036db90`  
		Last Modified: Tue, 03 Feb 2026 03:20:05 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d52e3857918c13fa3f684610d25461842622fcc7b5825ca1d20e8b5ad25677`  
		Last Modified: Tue, 03 Feb 2026 04:30:27 GMT  
		Size: 14.3 MB (14297685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb2d647140bc01d29b1b198669e9daa991f1bcf76989a5fa065107029da1170`  
		Last Modified: Tue, 03 Feb 2026 04:30:26 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561e80f37c011788d7200b5455a909968dbafc6a7f4581fbc4210be7f51071f3`  
		Last Modified: Tue, 03 Feb 2026 04:30:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61141732b10fb67faa20aa79c2416e35fbe1d668d29b5c2e4bfe57ca8b7da689`  
		Last Modified: Tue, 03 Feb 2026 04:30:26 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f5327fd71974d6ed16af8ca103330a4d218a9c33232f03a9f7514be4e7f712c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1d108c9d476f04bded3391e7889d9d7be94d2587ac3e23eab089f0442a9624`

```dockerfile
```

-	Layers:
	-	`sha256:368002be62137654a9e83c0a4d78846d701e974bb0892006414afe47cf582f6b`  
		Last Modified: Tue, 03 Feb 2026 04:30:26 GMT  
		Size: 2.7 MB (2670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262c0f95c03857683b26b61eb67d8305c59b1500a760369fa82ff1b2d4bc2840`  
		Last Modified: Tue, 03 Feb 2026 04:30:26 GMT  
		Size: 21.2 KB (21167 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:90f1c24b257c53b6410d0d97f1b98ebc48f67fcce63ce16550733f8075fb8428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78968250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd0c32127a25a0f7c604fcbf6f9ecc7942beb972b23ca2385806972efc4961e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 17:32:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 17:32:19 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:34:31 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:34:31 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:34:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:34:31 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:34:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:34:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:34:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:34:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:34:31 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:34:31 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 17:56:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jan 2026 17:56:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 14 Jan 2026 17:56:35 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jan 2026 17:56:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 14 Jan 2026 17:56:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 14 Jan 2026 17:56:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 14 Jan 2026 17:56:35 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 14 Jan 2026 17:56:35 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jan 2026 17:56:35 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jan 2026 17:56:35 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 14 Jan 2026 17:56:35 GMT
USER fluent
# Wed, 14 Jan 2026 17:56:35 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jan 2026 17:56:35 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2a0cffcee0205fc7f72267552713e68aa945359253bcab303f4dd69e7491c38d`  
		Last Modified: Tue, 13 Jan 2026 00:42:37 GMT  
		Size: 29.2 MB (29210067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9664d00f2ac07f1a53ca39e59420e0ad3b6d744a8e067b9b3a188609503eb53f`  
		Last Modified: Wed, 14 Jan 2026 17:34:41 GMT  
		Size: 3.5 MB (3512267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d1341420adb4e4c0776dbc2c45d78e4e46e5bbd4f04b0c31a49bbe15301989`  
		Last Modified: Wed, 14 Jan 2026 17:34:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2403fe3099c18d48da4cc7428c35b8a06c8863adb203a578ac9e16bcbdb405`  
		Last Modified: Wed, 14 Jan 2026 17:34:42 GMT  
		Size: 32.2 MB (32162614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4bf5f4010fca07e2de4b4dd7164f04c8ed771d92761739e7d43985c46b87c`  
		Last Modified: Wed, 14 Jan 2026 17:34:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301ba55b0e9384b0f71fdc19593d594ea08b47b1f910a513a829d0daef6304ef`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 14.1 MB (14080908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc3dab1e46344e84038b20f06abd8d431857e123dd62c84c7f7d039033d4513`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f866d64dba5c97eb9b1a6ed9307ffbc7a8ee753135b2349565566c76cdf0b13`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39356656143ad5c7597dbd1adbab41ed8ec0218f400a8e928df5e0366af73526`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:33c7fda88ba71531cdae91cdef4bbe85272adcc8f3f49ae22941411aadde079e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f449b8c8b811820cbe784f0b50667ecaed09fd61a0f23ff8e7865b819ada420e`

```dockerfile
```

-	Layers:
	-	`sha256:20de6d15d9c0c430cc3a4c29893b2be6434d2e7f25cac8508eb89faa582f28af`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:822d1cda5364d5d65c63acd2ac8f66231a29afc704a4c1585244345adefd8376`  
		Last Modified: Wed, 14 Jan 2026 17:56:45 GMT  
		Size: 21.0 KB (21048 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9aa1d8c59752e4ffe06bcbd93b654bf17427879fb102d3a528e2b707ff363670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84303585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aaad992c9da5ed4deb21f2f7658acf817cd344e4f038754b88d6408c8d57502`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Wed, 14 Jan 2026 02:40:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 14 Jan 2026 02:40:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 14 Jan 2026 17:41:02 GMT
ENV LANG=C.UTF-8
# Wed, 14 Jan 2026 17:41:02 GMT
ENV RUBY_VERSION=3.2.10
# Wed, 14 Jan 2026 17:41:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Wed, 14 Jan 2026 17:41:02 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Wed, 14 Jan 2026 17:41:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 14 Jan 2026 17:41:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 14 Jan 2026 17:41:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 14 Jan 2026 17:41:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jan 2026 17:41:02 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 14 Jan 2026 17:41:02 GMT
CMD ["irb"]
# Wed, 14 Jan 2026 18:46:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 14 Jan 2026 18:46:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 14 Jan 2026 18:46:35 GMT
ENV TINI_VERSION=0.18.0
# Wed, 14 Jan 2026 18:46:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 14 Jan 2026 18:46:37 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 14 Jan 2026 18:46:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 14 Jan 2026 18:46:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 14 Jan 2026 18:46:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 14 Jan 2026 18:46:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 14 Jan 2026 18:46:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 14 Jan 2026 18:46:38 GMT
USER fluent
# Wed, 14 Jan 2026 18:46:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 14 Jan 2026 18:46:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d040954f92ec97ea46ab26dcebf24a6ab2cc0e67f210bcce8bcb9dfb1faf77d6`  
		Last Modified: Wed, 14 Jan 2026 02:45:47 GMT  
		Size: 3.7 MB (3710271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9425bbafe39445bfc1ee834ed06db5e9c79e7483c2092810ffa256366c90b303`  
		Last Modified: Wed, 14 Jan 2026 02:45:47 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1227467ea0a824b18cf8aa0feb4b8b88b12384ba6539b2279092a31ec152162`  
		Last Modified: Wed, 14 Jan 2026 17:41:23 GMT  
		Size: 33.8 MB (33835867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06452470b4f462b81916f910dcdb89d1cbe76c38cd2a514358235fa72b8c21ae`  
		Last Modified: Wed, 14 Jan 2026 17:41:22 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663bb1414c8ccf30d8a816feb837edf44f968a6f065990af50bf5113301302bf`  
		Last Modified: Wed, 14 Jan 2026 18:47:02 GMT  
		Size: 14.7 MB (14686336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ca28754e30f055163ea627dcf14ba1dfa6cb5b375d50cb2ead5e4f63c23d62`  
		Last Modified: Wed, 14 Jan 2026 18:47:01 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8374192cc1f039a313736531286e52212534e91e611ba8ab608d334b22325b2d`  
		Last Modified: Wed, 14 Jan 2026 18:47:02 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c3b58d484d6b38343232ed48eca74819290dc5802066753fbf433f84a09e53`  
		Last Modified: Wed, 14 Jan 2026 18:47:01 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:92d357946fc2f973700b93554209c7268eabeabc0217d5ccfca60a05244fb384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159a4c9ff427cbe0b1fc80626d1165ccbdb45c00838c0e49bb3907702ad5345c`

```dockerfile
```

-	Layers:
	-	`sha256:6bd73a9eaa3c79f705a170038cfc1d86c861cd25ab3672dd6354ef9fff564ed9`  
		Last Modified: Wed, 14 Jan 2026 18:47:02 GMT  
		Size: 2.7 MB (2674899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c3268d6b5c7ddbc9d1b51c0689637ab55179d48bb38d86d87bff2b903057bb`  
		Last Modified: Wed, 14 Jan 2026 18:47:01 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:70ffa14741aed127fe3c56aa5cd7128d493308bcdb8f4b4849074ca35badbfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77588305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3a07efd5dd81993b0725e09910f685080fe53a0a93b6d0e3f7bf7aadc79bed`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:52:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:52:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:58:03 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:58:03 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 04:58:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 04:58:03 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 04:58:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:58:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:58:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:58:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:58:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:58:03 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 06:00:45 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 06:00:45 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 06:00:45 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 06:00:45 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 06:00:45 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 06:00:45 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 06:00:45 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 06:00:45 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 06:00:45 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 06:00:45 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 06:00:45 GMT
USER fluent
# Tue, 03 Feb 2026 06:00:45 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 06:00:45 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc41c1d20b68f1c7cbc98a19ce5b004fd426fc43dfdbee515f6d7b7f0b1a707`  
		Last Modified: Tue, 03 Feb 2026 04:55:38 GMT  
		Size: 3.2 MB (3171220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5f75f806d81ea37b8bca52c14c79c6d82a5fdc3cd7d255dc26352dd8b60a70`  
		Last Modified: Tue, 03 Feb 2026 04:55:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd4a6b6b71aefcebd8f7627a0c725eea4604094c4881b50115cb2183ff546a3`  
		Last Modified: Tue, 03 Feb 2026 04:58:17 GMT  
		Size: 33.1 MB (33103783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a208f8482e16e8115945c42792b6f9d69029a05cb09bc03b44a5d09299d152`  
		Last Modified: Tue, 03 Feb 2026 04:58:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f33c782dfcc09f11053485a946a254f46710ea633857edc0bdb82fafb43ea61`  
		Last Modified: Tue, 03 Feb 2026 06:00:59 GMT  
		Size: 14.4 MB (14426523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db49dff94be9b5f64fd1c78b8b5aef4229323d122606e740f568afc53319ae2`  
		Last Modified: Tue, 03 Feb 2026 06:00:59 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3d3d88c51398d874ec4c9260c9032207fbde2e54434eeeed6d486b9c6ae5a6`  
		Last Modified: Tue, 03 Feb 2026 06:00:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4c39f33fb4f2a94db43770cd936a761f15a284d236ca62b1d7829a085109f8`  
		Last Modified: Tue, 03 Feb 2026 06:00:58 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c4bacac5a1cdfb382fb0b9e6561c36fb31cb03cef91c7854cd6c33e41559f506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ddb98d78da7d91cf3805580573840a449447742bd39ecfcac6d9760673a2ee`

```dockerfile
```

-	Layers:
	-	`sha256:008d8bbb6bc5904b04a1c49e7a708386ba9c5501595d4d51e9e28cfb791ce6a2`  
		Last Modified: Tue, 03 Feb 2026 06:01:02 GMT  
		Size: 2.7 MB (2667307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f752b3f959cf2579075e87717de427972e6c191c043a7c97a8e6ded30d0d4d19`  
		Last Modified: Tue, 03 Feb 2026 06:00:59 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:af0791958bda6a479c153ca075b66f19cd40711fa78f77890c14e0e3f50a966c
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eef9b8933028d4d086fca9528ccc9271c5f7c65abfa73e952107ef4e71f5b`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 1.3 MB (1279374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef44c7bbb15316ed3c8b90e1149e7e65006f6a352bfbc150f83ba34cf36b8f0`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d36f3a5655a63fccdac1be1dea43008bf13f50700604d5bbb51dfd67c4f1`  
		Last Modified: Tue, 13 Jan 2026 03:17:24 GMT  
		Size: 42.1 MB (42112593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403786353912e853ee3b03de8484cf9cb0c6a860807846ff07bb720943ad0cc2`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95a20976cd45bd6c70aafe68db5deac22d7041dcc4332f23f4371cfb918ba2`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 6.0 MB (6001029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532f021056a355ffebc964ee6e349fc264a0ffdabb2e14ec25a50f2b008efe2`  
		Last Modified: Tue, 13 Jan 2026 05:00:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8358e169dbb7ee057d2e5fe1001b6db5516639c6e88ed047dca2a65dfb01d`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988474eade660a7633fbfdad69c9a561ab991db1686c4ea44d2227977121d7`  
		Last Modified: Tue, 13 Jan 2026 05:00:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 2.3 MB (2280167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d245ee90fda65ffc9ff75c6931bfb574b96d405448a7215873c5367f08bad`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:0268ca13bd306373fa628ffb063d494511eaea9240e44562752d0c95cbca83f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73024415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7328b17097e2e8bd9f392beb281688f548c4df6f7284c720119c0b2af899cd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:05:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:08:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:08:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:08:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:08:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:20:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:20:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 05:20:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:20:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:20:11 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:20:11 GMT
USER fluent
# Tue, 03 Feb 2026 05:20:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:20:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c14c6607560c7a97ca9cfcea3b52c3e76d7f20a7a35dfe9b77e8708dd1fb7a`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 1.3 MB (1263042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f3d0abef83d6f39ac1c802952a4c2d86bf87a3aab9c740d74354a361f3e897`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd1fa3197d5bf05a1ea42217fa36b4717385020eb13f031c4c543c880566c17`  
		Last Modified: Tue, 03 Feb 2026 04:08:14 GMT  
		Size: 37.9 MB (37905931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1bd1524e6a19a2549304082069b00ec1576b14900ad4203b654e6b5cd58179`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e401279a3be72d9dbf3322784bc98c9c917434f8ff60c4576b29520c00032c1`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 5.9 MB (5905492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9b508d832ed0b4b1485e4bd292145dd4102edda5951f954253bbae1a3074c9`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac904c03283287d26e5bd6fa8358575fe330fb80af609bf7864369f9eca5a3c`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0675a8863a728fff8eec1942fdb64861bf3eb25e8ca794b2b5b07ad7b2c7a0c`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3ede44144d8ac305efa5d19e232a56a17d887d125b42b67bfcc9fbc2cb1a2f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3397f404daf080cec4b573b13c94a3a2fdda180b8b8c17fa9986a4c930dbcbc5`

```dockerfile
```

-	Layers:
	-	`sha256:8a0a68521f31754df0c2f4f6c4bc5c1ef3a8de07b01f4be9342b91cb40d27c94`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 2.3 MB (2283164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d150826744b8296099adc8263b7ea42fd2b939265f06ff5e8c9f80130b46dbb6`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb89ad4eba0f6c13ed221ba61cd63256963a2ae6022c5eb1a90dfe213d338e`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 1.2 MB (1236555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4524518ebfe925ff0ba895a410f351e2ee7d22045883650d8b7fac782a9cc4c`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafc5c289841a0fbb484e454157cfd1cd3e738994188089f928286b34c74f8`  
		Last Modified: Tue, 13 Jan 2026 04:04:06 GMT  
		Size: 37.8 MB (37767155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c4e1fbfecc70f8903b4522859b5ef39a5906274e2351951079ed8f886585`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7740d7e2c777411352b0085fe0094c95668acdde8c6ece31de343123a5cf9`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 5.7 MB (5669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2b431fd4058cc969b8cbb21b31aacdf5b6c415776385b9bd855de095a86be`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0486e503a316218c72159c4aecfd966c0227bea5022343f9e65a9bab48e9a294`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a8b50351ca059aa0d8b903508c9a57aa8984f21e7a73c28431739b765cabf`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 2.3 MB (2281579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37545b709467be88ec29e37388b144288be9462833e3cab824fdb247fc368901`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:393b40c65ea83034dac8a29e04ded08acdd09b849edb2470c55d8f37006e8428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79470598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae22c0ff3b2b2d113e9093561de35f509074c56e9c45ff9feddcbf5ae577038c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:29:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:29:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:29:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:29:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:30:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:30:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:30:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:30:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:30:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:30:22 GMT
USER fluent
# Tue, 03 Feb 2026 04:30:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:30:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31281d91ffa5f433313784df0c0ab0303ae74e32c5eda8b5ed5e2ebd226e1769`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 1.3 MB (1261309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d703736f2a80eda1164a8432ec78cbb829dbe3b051f6fb77c389472322fa01fb`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c91036fff8080ee027ae4f27750a5445ddcadec9de626473b6bdecfe894fc`  
		Last Modified: Tue, 03 Feb 2026 03:29:12 GMT  
		Size: 42.1 MB (42073926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed131edf8d7f65cd888be6678e899e156b9e716575f254ae37e5ba9f368acc`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb721bec1b751561b6777457ba90580423562c1aa7239410f12bba5d9201fca`  
		Last Modified: Tue, 03 Feb 2026 04:30:31 GMT  
		Size: 6.0 MB (5992899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551cdc25412e01b56a32cf31f8da37234b3859b3013e35daaff806b60cc00550`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f7e0cf6ef7ea5036dc344617893905cf6d6d512362eb3e38fc0d0dbc6bfc17`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97948803dcc2bcc57916b670d8982b6e3e12d244d9471073640caf04816c306`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:494d2cf3e7fac63e031e0c02319c428ce7420a9e254f5bb2c6e177f15bd2a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcd1a00cc12bca92e35286f8b0fe8d85c847108ab1c777c1f42d017794b5168`

```dockerfile
```

-	Layers:
	-	`sha256:fb768aabcf004fa31fe669d97982beccd8c2f5a8f37cc0122ef369dc39205c06`  
		Last Modified: Tue, 03 Feb 2026 04:30:31 GMT  
		Size: 2.3 MB (2280465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2c695d2b0f6ef93b2c0fc48f00af91038e73c664edc15c49233e7d78d4ca78`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 21.5 KB (21457 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca9739d6b026ec1d4cd350482fedc4374621d2428ab77e18051bdb8ca6c93a`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 1.3 MB (1287208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf308c9322d7b7ccb72a3b032126ea9174c0dd19d5133f792f459c5f0fec63`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077996a21b00611176c639502288dd2a7a31e063ef348d46a1652665d276aa0`  
		Last Modified: Tue, 13 Jan 2026 02:49:35 GMT  
		Size: 37.7 MB (37661435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f373e260e56fe68e120ff78469b633199ef4d7e6980f6c1706b0628c090ec`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b70dc93001436daee4f4c2269d3b473cc83687fd15af6b3b65b15d67a592ad`  
		Last Modified: Tue, 13 Jan 2026 04:00:39 GMT  
		Size: 6.0 MB (5970309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64083097cffea937936c9ec17bfa648c81bbc71f8d05d684b7afb9e52a48d5c5`  
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5966fa1c56255ac85fd3cda423eb24e7808ebd4ca2f9f0ea681e3e09bfc34`  
		Last Modified: Tue, 13 Jan 2026 04:00:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefc55a043cc735826153c6bbcbc2f26bc3b8b365fb9dd174493eeb4c568d44`  
		Last Modified: Tue, 13 Jan 2026 04:00:37 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 2.3 MB (2277355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0ea0b7db35baa06510b1a0264df2ddf0c3651935cfe0f32813ad862ea1efe8`  
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9a3cafd2ad15ecca523d44c12561730c9618fcb6a8a324c012616df63417cccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80944198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2391227cf9ff745e5a0ddc2e174b4f2162089c1f4a73ebfe775fe96933d8f3d7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:13:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 05:24:03 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 05:24:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 05:24:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 05:24:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 05:24:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:24:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 05:24:04 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 09:00:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 09:00:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 09:00:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 09:00:45 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 09:00:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 09:00:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 09:00:46 GMT
USER fluent
# Tue, 13 Jan 2026 09:00:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 09:00:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd359a7e5d3b012a0e1f773e5ca872b7185e1ae4c53f7a9a7d797ae3eaaf8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 1.3 MB (1309726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eeff64fa1ee2c5a20375771788d22ec3d5ad95481b75598a70ada63b47d8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5604be4a4b60f4fed68c22b913b07851aa0414cc66ee4da7ee7c4338b2e5d28e`  
		Last Modified: Tue, 13 Jan 2026 05:24:26 GMT  
		Size: 39.5 MB (39519922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc1dc23f8783cc9ad3639c62138f859289801c771b5a9e82fd86f8e4e4f7d19`  
		Last Modified: Tue, 13 Jan 2026 05:24:25 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e30a59d33d2a25b91e6031d498d0e8223513a391ec9a792eea32735baa9de15`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 6.5 MB (6516555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f924ba79838c3e65a0a1331631e11f5844fcff2d3c1c940dc123fab38974a2`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c3db13e0b69bf0fb77f89fca056dada7d7cf70bfe910ac9c2a95048d221003`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb4153c5f33f3ac2b2b9dd2e803c3ed885e8990d990b99f7d129ee38342af3c`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0032be699998ed132a2460102525b0fc79f3749b8ae840292df4cfbe7d33dbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a97bdbdb1fc3ecd09b897233c3be4d5e82e7331f90aa9d007be0b7e8e5f1f1`

```dockerfile
```

-	Layers:
	-	`sha256:ccfacc43efb7a135d5fb8cba44cce1125970f2e76f94c86a2e668fa770ee3eb9`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 2.3 MB (2283702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7b890f4811a2723a742990c05386c8fff28e65cec0ee2946431c1b38970752`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; s390x

```console
$ docker pull fluentd@sha256:b1c8103ef9d6bd1a2d4acaa83c631bdc92e00a34026c88d668605aaaf50a9084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76705553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80b4cea4899143ffdc5ffd2fa8c5c6324ee8452ca49c9136d94a09fcf89d1dc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:53:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:53:52 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 06:00:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 06:00:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 06:00:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 06:00:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 06:00:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 06:00:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 06:00:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 06:00:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 06:00:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 06:00:36 GMT
USER fluent
# Tue, 03 Feb 2026 06:00:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 06:00:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0ef58ef1eb78dd947e41fe50adfe7b4ab7ed59de6adb1cee9b213c29193b84`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 1.3 MB (1294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6191cacf2fcbd60736c6c6dd3a35edf5fb265ba19e0504896f4a96d590bdc0`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2e7a1acf75697b829c5674d2af59db59b82bd932f96d1c50df559112643e50`  
		Last Modified: Tue, 03 Feb 2026 04:54:07 GMT  
		Size: 39.2 MB (39191476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27dcf4be1994bc1f0cbe0b29edacbaeb7643532854664d63ed921b9823209fe`  
		Last Modified: Tue, 03 Feb 2026 04:54:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8836a2a3d5fe0612bd6f486ccf67502c90dca13b55f0ee3015dc8fc9b6dcb80d`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 6.4 MB (6379016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ab910ede55a870b32fe8533f6e8da853c247e99cabc2a0d54ea29e1f21a75a`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18813b9ae4d1bc8ed0dea132c93ede5766cd2fd64a961a8f60770e1163afd0a4`  
		Last Modified: Tue, 03 Feb 2026 06:00:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d235fff2840bba22a65cc11d16cfc6c02d9b103745e92481615dde3a9ec9bfca`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:833aa0335c34fbde7814ce09c890b3155346bc8500bd98a346ce1c02d8a7f823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f3e40c9d0bd52e3f4614bf12dbb9e2b426d8aa9e7c2e702cad2ffbec47004`

```dockerfile
```

-	Layers:
	-	`sha256:a03784ba6816bc7a3f5cc90a89bd87aeda3703bd11775b3e06f739dde63954f0`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 2.3 MB (2281638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39680257795ba8f20d5fa4200ee53f00d46bef5378ad0a8ad8fd43a097220b5d`  
		Last Modified: Tue, 03 Feb 2026 06:00:51 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:af0791958bda6a479c153ca075b66f19cd40711fa78f77890c14e0e3f50a966c
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eef9b8933028d4d086fca9528ccc9271c5f7c65abfa73e952107ef4e71f5b`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 1.3 MB (1279374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef44c7bbb15316ed3c8b90e1149e7e65006f6a352bfbc150f83ba34cf36b8f0`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d36f3a5655a63fccdac1be1dea43008bf13f50700604d5bbb51dfd67c4f1`  
		Last Modified: Tue, 13 Jan 2026 03:17:24 GMT  
		Size: 42.1 MB (42112593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403786353912e853ee3b03de8484cf9cb0c6a860807846ff07bb720943ad0cc2`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95a20976cd45bd6c70aafe68db5deac22d7041dcc4332f23f4371cfb918ba2`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 6.0 MB (6001029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532f021056a355ffebc964ee6e349fc264a0ffdabb2e14ec25a50f2b008efe2`  
		Last Modified: Tue, 13 Jan 2026 05:00:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8358e169dbb7ee057d2e5fe1001b6db5516639c6e88ed047dca2a65dfb01d`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988474eade660a7633fbfdad69c9a561ab991db1686c4ea44d2227977121d7`  
		Last Modified: Tue, 13 Jan 2026 05:00:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 2.3 MB (2280167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d245ee90fda65ffc9ff75c6931bfb574b96d405448a7215873c5367f08bad`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:0268ca13bd306373fa628ffb063d494511eaea9240e44562752d0c95cbca83f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73024415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7328b17097e2e8bd9f392beb281688f548c4df6f7284c720119c0b2af899cd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:05:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:08:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:08:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:08:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:08:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:20:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:20:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 05:20:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:20:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:20:11 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:20:11 GMT
USER fluent
# Tue, 03 Feb 2026 05:20:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:20:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c14c6607560c7a97ca9cfcea3b52c3e76d7f20a7a35dfe9b77e8708dd1fb7a`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 1.3 MB (1263042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f3d0abef83d6f39ac1c802952a4c2d86bf87a3aab9c740d74354a361f3e897`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd1fa3197d5bf05a1ea42217fa36b4717385020eb13f031c4c543c880566c17`  
		Last Modified: Tue, 03 Feb 2026 04:08:14 GMT  
		Size: 37.9 MB (37905931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1bd1524e6a19a2549304082069b00ec1576b14900ad4203b654e6b5cd58179`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e401279a3be72d9dbf3322784bc98c9c917434f8ff60c4576b29520c00032c1`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 5.9 MB (5905492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9b508d832ed0b4b1485e4bd292145dd4102edda5951f954253bbae1a3074c9`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac904c03283287d26e5bd6fa8358575fe330fb80af609bf7864369f9eca5a3c`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0675a8863a728fff8eec1942fdb64861bf3eb25e8ca794b2b5b07ad7b2c7a0c`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3ede44144d8ac305efa5d19e232a56a17d887d125b42b67bfcc9fbc2cb1a2f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3397f404daf080cec4b573b13c94a3a2fdda180b8b8c17fa9986a4c930dbcbc5`

```dockerfile
```

-	Layers:
	-	`sha256:8a0a68521f31754df0c2f4f6c4bc5c1ef3a8de07b01f4be9342b91cb40d27c94`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 2.3 MB (2283164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d150826744b8296099adc8263b7ea42fd2b939265f06ff5e8c9f80130b46dbb6`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb89ad4eba0f6c13ed221ba61cd63256963a2ae6022c5eb1a90dfe213d338e`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 1.2 MB (1236555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4524518ebfe925ff0ba895a410f351e2ee7d22045883650d8b7fac782a9cc4c`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafc5c289841a0fbb484e454157cfd1cd3e738994188089f928286b34c74f8`  
		Last Modified: Tue, 13 Jan 2026 04:04:06 GMT  
		Size: 37.8 MB (37767155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c4e1fbfecc70f8903b4522859b5ef39a5906274e2351951079ed8f886585`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7740d7e2c777411352b0085fe0094c95668acdde8c6ece31de343123a5cf9`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 5.7 MB (5669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2b431fd4058cc969b8cbb21b31aacdf5b6c415776385b9bd855de095a86be`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0486e503a316218c72159c4aecfd966c0227bea5022343f9e65a9bab48e9a294`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a8b50351ca059aa0d8b903508c9a57aa8984f21e7a73c28431739b765cabf`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 2.3 MB (2281579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37545b709467be88ec29e37388b144288be9462833e3cab824fdb247fc368901`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:393b40c65ea83034dac8a29e04ded08acdd09b849edb2470c55d8f37006e8428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79470598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae22c0ff3b2b2d113e9093561de35f509074c56e9c45ff9feddcbf5ae577038c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:29:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:29:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:29:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:29:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:30:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:30:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:30:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:30:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:30:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:30:22 GMT
USER fluent
# Tue, 03 Feb 2026 04:30:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:30:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31281d91ffa5f433313784df0c0ab0303ae74e32c5eda8b5ed5e2ebd226e1769`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 1.3 MB (1261309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d703736f2a80eda1164a8432ec78cbb829dbe3b051f6fb77c389472322fa01fb`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c91036fff8080ee027ae4f27750a5445ddcadec9de626473b6bdecfe894fc`  
		Last Modified: Tue, 03 Feb 2026 03:29:12 GMT  
		Size: 42.1 MB (42073926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed131edf8d7f65cd888be6678e899e156b9e716575f254ae37e5ba9f368acc`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb721bec1b751561b6777457ba90580423562c1aa7239410f12bba5d9201fca`  
		Last Modified: Tue, 03 Feb 2026 04:30:31 GMT  
		Size: 6.0 MB (5992899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551cdc25412e01b56a32cf31f8da37234b3859b3013e35daaff806b60cc00550`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f7e0cf6ef7ea5036dc344617893905cf6d6d512362eb3e38fc0d0dbc6bfc17`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97948803dcc2bcc57916b670d8982b6e3e12d244d9471073640caf04816c306`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:494d2cf3e7fac63e031e0c02319c428ce7420a9e254f5bb2c6e177f15bd2a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcd1a00cc12bca92e35286f8b0fe8d85c847108ab1c777c1f42d017794b5168`

```dockerfile
```

-	Layers:
	-	`sha256:fb768aabcf004fa31fe669d97982beccd8c2f5a8f37cc0122ef369dc39205c06`  
		Last Modified: Tue, 03 Feb 2026 04:30:31 GMT  
		Size: 2.3 MB (2280465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2c695d2b0f6ef93b2c0fc48f00af91038e73c664edc15c49233e7d78d4ca78`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 21.5 KB (21457 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca9739d6b026ec1d4cd350482fedc4374621d2428ab77e18051bdb8ca6c93a`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 1.3 MB (1287208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf308c9322d7b7ccb72a3b032126ea9174c0dd19d5133f792f459c5f0fec63`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077996a21b00611176c639502288dd2a7a31e063ef348d46a1652665d276aa0`  
		Last Modified: Tue, 13 Jan 2026 02:49:35 GMT  
		Size: 37.7 MB (37661435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f373e260e56fe68e120ff78469b633199ef4d7e6980f6c1706b0628c090ec`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b70dc93001436daee4f4c2269d3b473cc83687fd15af6b3b65b15d67a592ad`  
		Last Modified: Tue, 13 Jan 2026 04:00:39 GMT  
		Size: 6.0 MB (5970309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64083097cffea937936c9ec17bfa648c81bbc71f8d05d684b7afb9e52a48d5c5`  
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5966fa1c56255ac85fd3cda423eb24e7808ebd4ca2f9f0ea681e3e09bfc34`  
		Last Modified: Tue, 13 Jan 2026 04:00:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefc55a043cc735826153c6bbcbc2f26bc3b8b365fb9dd174493eeb4c568d44`  
		Last Modified: Tue, 13 Jan 2026 04:00:37 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 2.3 MB (2277355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0ea0b7db35baa06510b1a0264df2ddf0c3651935cfe0f32813ad862ea1efe8`  
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9a3cafd2ad15ecca523d44c12561730c9618fcb6a8a324c012616df63417cccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80944198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2391227cf9ff745e5a0ddc2e174b4f2162089c1f4a73ebfe775fe96933d8f3d7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:13:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 05:24:03 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 05:24:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 05:24:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 05:24:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 05:24:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:24:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 05:24:04 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 09:00:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 09:00:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 09:00:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 09:00:45 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 09:00:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 09:00:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 09:00:46 GMT
USER fluent
# Tue, 13 Jan 2026 09:00:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 09:00:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd359a7e5d3b012a0e1f773e5ca872b7185e1ae4c53f7a9a7d797ae3eaaf8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 1.3 MB (1309726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eeff64fa1ee2c5a20375771788d22ec3d5ad95481b75598a70ada63b47d8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5604be4a4b60f4fed68c22b913b07851aa0414cc66ee4da7ee7c4338b2e5d28e`  
		Last Modified: Tue, 13 Jan 2026 05:24:26 GMT  
		Size: 39.5 MB (39519922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc1dc23f8783cc9ad3639c62138f859289801c771b5a9e82fd86f8e4e4f7d19`  
		Last Modified: Tue, 13 Jan 2026 05:24:25 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e30a59d33d2a25b91e6031d498d0e8223513a391ec9a792eea32735baa9de15`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 6.5 MB (6516555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f924ba79838c3e65a0a1331631e11f5844fcff2d3c1c940dc123fab38974a2`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c3db13e0b69bf0fb77f89fca056dada7d7cf70bfe910ac9c2a95048d221003`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb4153c5f33f3ac2b2b9dd2e803c3ed885e8990d990b99f7d129ee38342af3c`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0032be699998ed132a2460102525b0fc79f3749b8ae840292df4cfbe7d33dbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a97bdbdb1fc3ecd09b897233c3be4d5e82e7331f90aa9d007be0b7e8e5f1f1`

```dockerfile
```

-	Layers:
	-	`sha256:ccfacc43efb7a135d5fb8cba44cce1125970f2e76f94c86a2e668fa770ee3eb9`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 2.3 MB (2283702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7b890f4811a2723a742990c05386c8fff28e65cec0ee2946431c1b38970752`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:b1c8103ef9d6bd1a2d4acaa83c631bdc92e00a34026c88d668605aaaf50a9084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76705553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80b4cea4899143ffdc5ffd2fa8c5c6324ee8452ca49c9136d94a09fcf89d1dc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:53:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:53:52 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 06:00:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 06:00:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 06:00:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 06:00:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 06:00:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 06:00:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 06:00:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 06:00:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 06:00:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 06:00:36 GMT
USER fluent
# Tue, 03 Feb 2026 06:00:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 06:00:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0ef58ef1eb78dd947e41fe50adfe7b4ab7ed59de6adb1cee9b213c29193b84`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 1.3 MB (1294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6191cacf2fcbd60736c6c6dd3a35edf5fb265ba19e0504896f4a96d590bdc0`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2e7a1acf75697b829c5674d2af59db59b82bd932f96d1c50df559112643e50`  
		Last Modified: Tue, 03 Feb 2026 04:54:07 GMT  
		Size: 39.2 MB (39191476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27dcf4be1994bc1f0cbe0b29edacbaeb7643532854664d63ed921b9823209fe`  
		Last Modified: Tue, 03 Feb 2026 04:54:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8836a2a3d5fe0612bd6f486ccf67502c90dca13b55f0ee3015dc8fc9b6dcb80d`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 6.4 MB (6379016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ab910ede55a870b32fe8533f6e8da853c247e99cabc2a0d54ea29e1f21a75a`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18813b9ae4d1bc8ed0dea132c93ede5766cd2fd64a961a8f60770e1163afd0a4`  
		Last Modified: Tue, 03 Feb 2026 06:00:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d235fff2840bba22a65cc11d16cfc6c02d9b103745e92481615dde3a9ec9bfca`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:833aa0335c34fbde7814ce09c890b3155346bc8500bd98a346ce1c02d8a7f823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f3e40c9d0bd52e3f4614bf12dbb9e2b426d8aa9e7c2e702cad2ffbec47004`

```dockerfile
```

-	Layers:
	-	`sha256:a03784ba6816bc7a3f5cc90a89bd87aeda3703bd11775b3e06f739dde63954f0`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 2.3 MB (2281638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39680257795ba8f20d5fa4200ee53f00d46bef5378ad0a8ad8fd43a097220b5d`  
		Last Modified: Tue, 03 Feb 2026 06:00:51 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.0-1.0`

```console
$ docker pull fluentd@sha256:af0791958bda6a479c153ca075b66f19cd40711fa78f77890c14e0e3f50a966c
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eef9b8933028d4d086fca9528ccc9271c5f7c65abfa73e952107ef4e71f5b`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 1.3 MB (1279374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef44c7bbb15316ed3c8b90e1149e7e65006f6a352bfbc150f83ba34cf36b8f0`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d36f3a5655a63fccdac1be1dea43008bf13f50700604d5bbb51dfd67c4f1`  
		Last Modified: Tue, 13 Jan 2026 03:17:24 GMT  
		Size: 42.1 MB (42112593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403786353912e853ee3b03de8484cf9cb0c6a860807846ff07bb720943ad0cc2`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95a20976cd45bd6c70aafe68db5deac22d7041dcc4332f23f4371cfb918ba2`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 6.0 MB (6001029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532f021056a355ffebc964ee6e349fc264a0ffdabb2e14ec25a50f2b008efe2`  
		Last Modified: Tue, 13 Jan 2026 05:00:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8358e169dbb7ee057d2e5fe1001b6db5516639c6e88ed047dca2a65dfb01d`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988474eade660a7633fbfdad69c9a561ab991db1686c4ea44d2227977121d7`  
		Last Modified: Tue, 13 Jan 2026 05:00:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 2.3 MB (2280167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d245ee90fda65ffc9ff75c6931bfb574b96d405448a7215873c5367f08bad`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:0268ca13bd306373fa628ffb063d494511eaea9240e44562752d0c95cbca83f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73024415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7328b17097e2e8bd9f392beb281688f548c4df6f7284c720119c0b2af899cd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:05:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:08:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:08:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:08:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:08:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:20:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:20:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 05:20:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:20:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:20:11 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:20:11 GMT
USER fluent
# Tue, 03 Feb 2026 05:20:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:20:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c14c6607560c7a97ca9cfcea3b52c3e76d7f20a7a35dfe9b77e8708dd1fb7a`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 1.3 MB (1263042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f3d0abef83d6f39ac1c802952a4c2d86bf87a3aab9c740d74354a361f3e897`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd1fa3197d5bf05a1ea42217fa36b4717385020eb13f031c4c543c880566c17`  
		Last Modified: Tue, 03 Feb 2026 04:08:14 GMT  
		Size: 37.9 MB (37905931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1bd1524e6a19a2549304082069b00ec1576b14900ad4203b654e6b5cd58179`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e401279a3be72d9dbf3322784bc98c9c917434f8ff60c4576b29520c00032c1`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 5.9 MB (5905492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9b508d832ed0b4b1485e4bd292145dd4102edda5951f954253bbae1a3074c9`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac904c03283287d26e5bd6fa8358575fe330fb80af609bf7864369f9eca5a3c`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0675a8863a728fff8eec1942fdb64861bf3eb25e8ca794b2b5b07ad7b2c7a0c`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3ede44144d8ac305efa5d19e232a56a17d887d125b42b67bfcc9fbc2cb1a2f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3397f404daf080cec4b573b13c94a3a2fdda180b8b8c17fa9986a4c930dbcbc5`

```dockerfile
```

-	Layers:
	-	`sha256:8a0a68521f31754df0c2f4f6c4bc5c1ef3a8de07b01f4be9342b91cb40d27c94`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 2.3 MB (2283164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d150826744b8296099adc8263b7ea42fd2b939265f06ff5e8c9f80130b46dbb6`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb89ad4eba0f6c13ed221ba61cd63256963a2ae6022c5eb1a90dfe213d338e`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 1.2 MB (1236555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4524518ebfe925ff0ba895a410f351e2ee7d22045883650d8b7fac782a9cc4c`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafc5c289841a0fbb484e454157cfd1cd3e738994188089f928286b34c74f8`  
		Last Modified: Tue, 13 Jan 2026 04:04:06 GMT  
		Size: 37.8 MB (37767155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c4e1fbfecc70f8903b4522859b5ef39a5906274e2351951079ed8f886585`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7740d7e2c777411352b0085fe0094c95668acdde8c6ece31de343123a5cf9`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 5.7 MB (5669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2b431fd4058cc969b8cbb21b31aacdf5b6c415776385b9bd855de095a86be`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0486e503a316218c72159c4aecfd966c0227bea5022343f9e65a9bab48e9a294`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a8b50351ca059aa0d8b903508c9a57aa8984f21e7a73c28431739b765cabf`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 2.3 MB (2281579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37545b709467be88ec29e37388b144288be9462833e3cab824fdb247fc368901`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:393b40c65ea83034dac8a29e04ded08acdd09b849edb2470c55d8f37006e8428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79470598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae22c0ff3b2b2d113e9093561de35f509074c56e9c45ff9feddcbf5ae577038c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:29:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:29:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:29:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:29:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:30:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:30:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:30:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:30:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:30:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:30:22 GMT
USER fluent
# Tue, 03 Feb 2026 04:30:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:30:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31281d91ffa5f433313784df0c0ab0303ae74e32c5eda8b5ed5e2ebd226e1769`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 1.3 MB (1261309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d703736f2a80eda1164a8432ec78cbb829dbe3b051f6fb77c389472322fa01fb`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c91036fff8080ee027ae4f27750a5445ddcadec9de626473b6bdecfe894fc`  
		Last Modified: Tue, 03 Feb 2026 03:29:12 GMT  
		Size: 42.1 MB (42073926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed131edf8d7f65cd888be6678e899e156b9e716575f254ae37e5ba9f368acc`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb721bec1b751561b6777457ba90580423562c1aa7239410f12bba5d9201fca`  
		Last Modified: Tue, 03 Feb 2026 04:30:31 GMT  
		Size: 6.0 MB (5992899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551cdc25412e01b56a32cf31f8da37234b3859b3013e35daaff806b60cc00550`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f7e0cf6ef7ea5036dc344617893905cf6d6d512362eb3e38fc0d0dbc6bfc17`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97948803dcc2bcc57916b670d8982b6e3e12d244d9471073640caf04816c306`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:494d2cf3e7fac63e031e0c02319c428ce7420a9e254f5bb2c6e177f15bd2a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcd1a00cc12bca92e35286f8b0fe8d85c847108ab1c777c1f42d017794b5168`

```dockerfile
```

-	Layers:
	-	`sha256:fb768aabcf004fa31fe669d97982beccd8c2f5a8f37cc0122ef369dc39205c06`  
		Last Modified: Tue, 03 Feb 2026 04:30:31 GMT  
		Size: 2.3 MB (2280465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2c695d2b0f6ef93b2c0fc48f00af91038e73c664edc15c49233e7d78d4ca78`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 21.5 KB (21457 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca9739d6b026ec1d4cd350482fedc4374621d2428ab77e18051bdb8ca6c93a`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 1.3 MB (1287208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf308c9322d7b7ccb72a3b032126ea9174c0dd19d5133f792f459c5f0fec63`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077996a21b00611176c639502288dd2a7a31e063ef348d46a1652665d276aa0`  
		Last Modified: Tue, 13 Jan 2026 02:49:35 GMT  
		Size: 37.7 MB (37661435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f373e260e56fe68e120ff78469b633199ef4d7e6980f6c1706b0628c090ec`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b70dc93001436daee4f4c2269d3b473cc83687fd15af6b3b65b15d67a592ad`  
		Last Modified: Tue, 13 Jan 2026 04:00:39 GMT  
		Size: 6.0 MB (5970309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64083097cffea937936c9ec17bfa648c81bbc71f8d05d684b7afb9e52a48d5c5`  
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5966fa1c56255ac85fd3cda423eb24e7808ebd4ca2f9f0ea681e3e09bfc34`  
		Last Modified: Tue, 13 Jan 2026 04:00:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefc55a043cc735826153c6bbcbc2f26bc3b8b365fb9dd174493eeb4c568d44`  
		Last Modified: Tue, 13 Jan 2026 04:00:37 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 2.3 MB (2277355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0ea0b7db35baa06510b1a0264df2ddf0c3651935cfe0f32813ad862ea1efe8`  
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9a3cafd2ad15ecca523d44c12561730c9618fcb6a8a324c012616df63417cccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80944198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2391227cf9ff745e5a0ddc2e174b4f2162089c1f4a73ebfe775fe96933d8f3d7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:13:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 05:24:03 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 05:24:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 05:24:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 05:24:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 05:24:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:24:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 05:24:04 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 09:00:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 09:00:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 09:00:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 09:00:45 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 09:00:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 09:00:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 09:00:46 GMT
USER fluent
# Tue, 13 Jan 2026 09:00:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 09:00:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd359a7e5d3b012a0e1f773e5ca872b7185e1ae4c53f7a9a7d797ae3eaaf8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 1.3 MB (1309726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eeff64fa1ee2c5a20375771788d22ec3d5ad95481b75598a70ada63b47d8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5604be4a4b60f4fed68c22b913b07851aa0414cc66ee4da7ee7c4338b2e5d28e`  
		Last Modified: Tue, 13 Jan 2026 05:24:26 GMT  
		Size: 39.5 MB (39519922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc1dc23f8783cc9ad3639c62138f859289801c771b5a9e82fd86f8e4e4f7d19`  
		Last Modified: Tue, 13 Jan 2026 05:24:25 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e30a59d33d2a25b91e6031d498d0e8223513a391ec9a792eea32735baa9de15`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 6.5 MB (6516555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f924ba79838c3e65a0a1331631e11f5844fcff2d3c1c940dc123fab38974a2`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c3db13e0b69bf0fb77f89fca056dada7d7cf70bfe910ac9c2a95048d221003`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb4153c5f33f3ac2b2b9dd2e803c3ed885e8990d990b99f7d129ee38342af3c`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0032be699998ed132a2460102525b0fc79f3749b8ae840292df4cfbe7d33dbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a97bdbdb1fc3ecd09b897233c3be4d5e82e7331f90aa9d007be0b7e8e5f1f1`

```dockerfile
```

-	Layers:
	-	`sha256:ccfacc43efb7a135d5fb8cba44cce1125970f2e76f94c86a2e668fa770ee3eb9`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 2.3 MB (2283702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7b890f4811a2723a742990c05386c8fff28e65cec0ee2946431c1b38970752`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:b1c8103ef9d6bd1a2d4acaa83c631bdc92e00a34026c88d668605aaaf50a9084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76705553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80b4cea4899143ffdc5ffd2fa8c5c6324ee8452ca49c9136d94a09fcf89d1dc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:53:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:53:52 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 06:00:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 06:00:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 06:00:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 06:00:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 06:00:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 06:00:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 06:00:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 06:00:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 06:00:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 06:00:36 GMT
USER fluent
# Tue, 03 Feb 2026 06:00:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 06:00:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0ef58ef1eb78dd947e41fe50adfe7b4ab7ed59de6adb1cee9b213c29193b84`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 1.3 MB (1294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6191cacf2fcbd60736c6c6dd3a35edf5fb265ba19e0504896f4a96d590bdc0`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2e7a1acf75697b829c5674d2af59db59b82bd932f96d1c50df559112643e50`  
		Last Modified: Tue, 03 Feb 2026 04:54:07 GMT  
		Size: 39.2 MB (39191476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27dcf4be1994bc1f0cbe0b29edacbaeb7643532854664d63ed921b9823209fe`  
		Last Modified: Tue, 03 Feb 2026 04:54:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8836a2a3d5fe0612bd6f486ccf67502c90dca13b55f0ee3015dc8fc9b6dcb80d`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 6.4 MB (6379016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ab910ede55a870b32fe8533f6e8da853c247e99cabc2a0d54ea29e1f21a75a`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18813b9ae4d1bc8ed0dea132c93ede5766cd2fd64a961a8f60770e1163afd0a4`  
		Last Modified: Tue, 03 Feb 2026 06:00:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d235fff2840bba22a65cc11d16cfc6c02d9b103745e92481615dde3a9ec9bfca`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:833aa0335c34fbde7814ce09c890b3155346bc8500bd98a346ce1c02d8a7f823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f3e40c9d0bd52e3f4614bf12dbb9e2b426d8aa9e7c2e702cad2ffbec47004`

```dockerfile
```

-	Layers:
	-	`sha256:a03784ba6816bc7a3f5cc90a89bd87aeda3703bd11775b3e06f739dde63954f0`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 2.3 MB (2281638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39680257795ba8f20d5fa4200ee53f00d46bef5378ad0a8ad8fd43a097220b5d`  
		Last Modified: Tue, 03 Feb 2026 06:00:51 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.1-debian-1.0`

```console
$ docker pull fluentd@sha256:af0791958bda6a479c153ca075b66f19cd40711fa78f77890c14e0e3f50a966c
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
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6eef9b8933028d4d086fca9528ccc9271c5f7c65abfa73e952107ef4e71f5b`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 1.3 MB (1279374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef44c7bbb15316ed3c8b90e1149e7e65006f6a352bfbc150f83ba34cf36b8f0`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ab2d36f3a5655a63fccdac1be1dea43008bf13f50700604d5bbb51dfd67c4f1`  
		Last Modified: Tue, 13 Jan 2026 03:17:24 GMT  
		Size: 42.1 MB (42112593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403786353912e853ee3b03de8484cf9cb0c6a860807846ff07bb720943ad0cc2`  
		Last Modified: Tue, 13 Jan 2026 03:17:23 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95a20976cd45bd6c70aafe68db5deac22d7041dcc4332f23f4371cfb918ba2`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 6.0 MB (6001029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e532f021056a355ffebc964ee6e349fc264a0ffdabb2e14ec25a50f2b008efe2`  
		Last Modified: Tue, 13 Jan 2026 05:00:17 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8358e169dbb7ee057d2e5fe1001b6db5516639c6e88ed047dca2a65dfb01d`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3988474eade660a7633fbfdad69c9a561ab991db1686c4ea44d2227977121d7`  
		Last Modified: Tue, 13 Jan 2026 05:00:17 GMT  
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
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 2.3 MB (2280167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:274d245ee90fda65ffc9ff75c6931bfb574b96d405448a7215873c5367f08bad`  
		Last Modified: Tue, 13 Jan 2026 05:00:16 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:0268ca13bd306373fa628ffb063d494511eaea9240e44562752d0c95cbca83f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73024415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7328b17097e2e8bd9f392beb281688f548c4df6f7284c720119c0b2af899cd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:05:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:05:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:08:04 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:08:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:08:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:08:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:08:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:08:04 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:20:11 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:20:11 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 05:20:11 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:20:11 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:20:11 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:20:11 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:20:11 GMT
USER fluent
# Tue, 03 Feb 2026 05:20:11 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:20:11 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c14c6607560c7a97ca9cfcea3b52c3e76d7f20a7a35dfe9b77e8708dd1fb7a`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 1.3 MB (1263042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f3d0abef83d6f39ac1c802952a4c2d86bf87a3aab9c740d74354a361f3e897`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd1fa3197d5bf05a1ea42217fa36b4717385020eb13f031c4c543c880566c17`  
		Last Modified: Tue, 03 Feb 2026 04:08:14 GMT  
		Size: 37.9 MB (37905931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1bd1524e6a19a2549304082069b00ec1576b14900ad4203b654e6b5cd58179`  
		Last Modified: Tue, 03 Feb 2026 04:08:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e401279a3be72d9dbf3322784bc98c9c917434f8ff60c4576b29520c00032c1`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 5.9 MB (5905492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9b508d832ed0b4b1485e4bd292145dd4102edda5951f954253bbae1a3074c9`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac904c03283287d26e5bd6fa8358575fe330fb80af609bf7864369f9eca5a3c`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0675a8863a728fff8eec1942fdb64861bf3eb25e8ca794b2b5b07ad7b2c7a0c`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3ede44144d8ac305efa5d19e232a56a17d887d125b42b67bfcc9fbc2cb1a2f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3397f404daf080cec4b573b13c94a3a2fdda180b8b8c17fa9986a4c930dbcbc5`

```dockerfile
```

-	Layers:
	-	`sha256:8a0a68521f31754df0c2f4f6c4bc5c1ef3a8de07b01f4be9342b91cb40d27c94`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
		Size: 2.3 MB (2283164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d150826744b8296099adc8263b7ea42fd2b939265f06ff5e8c9f80130b46dbb6`  
		Last Modified: Tue, 03 Feb 2026 05:20:19 GMT  
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
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cb89ad4eba0f6c13ed221ba61cd63256963a2ae6022c5eb1a90dfe213d338e`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 1.2 MB (1236555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4524518ebfe925ff0ba895a410f351e2ee7d22045883650d8b7fac782a9cc4c`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeafc5c289841a0fbb484e454157cfd1cd3e738994188089f928286b34c74f8`  
		Last Modified: Tue, 13 Jan 2026 04:04:06 GMT  
		Size: 37.8 MB (37767155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4c4e1fbfecc70f8903b4522859b5ef39a5906274e2351951079ed8f886585`  
		Last Modified: Tue, 13 Jan 2026 04:04:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce7740d7e2c777411352b0085fe0094c95668acdde8c6ece31de343123a5cf9`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 5.7 MB (5669196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef2b431fd4058cc969b8cbb21b31aacdf5b6c415776385b9bd855de095a86be`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0486e503a316218c72159c4aecfd966c0227bea5022343f9e65a9bab48e9a294`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8a8b50351ca059aa0d8b903508c9a57aa8984f21e7a73c28431739b765cabf`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 2.3 MB (2281579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37545b709467be88ec29e37388b144288be9462833e3cab824fdb247fc368901`  
		Last Modified: Tue, 13 Jan 2026 04:53:01 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:393b40c65ea83034dac8a29e04ded08acdd09b849edb2470c55d8f37006e8428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79470598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae22c0ff3b2b2d113e9093561de35f509074c56e9c45ff9feddcbf5ae577038c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:26:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:29:01 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:29:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:29:01 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:29:01 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:29:01 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:29:01 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:30:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:30:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:30:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:30:22 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:30:22 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:30:22 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:30:22 GMT
USER fluent
# Tue, 03 Feb 2026 04:30:22 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:30:22 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31281d91ffa5f433313784df0c0ab0303ae74e32c5eda8b5ed5e2ebd226e1769`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 1.3 MB (1261309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d703736f2a80eda1164a8432ec78cbb829dbe3b051f6fb77c389472322fa01fb`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c91036fff8080ee027ae4f27750a5445ddcadec9de626473b6bdecfe894fc`  
		Last Modified: Tue, 03 Feb 2026 03:29:12 GMT  
		Size: 42.1 MB (42073926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ed131edf8d7f65cd888be6678e899e156b9e716575f254ae37e5ba9f368acc`  
		Last Modified: Tue, 03 Feb 2026 03:29:11 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb721bec1b751561b6777457ba90580423562c1aa7239410f12bba5d9201fca`  
		Last Modified: Tue, 03 Feb 2026 04:30:31 GMT  
		Size: 6.0 MB (5992899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551cdc25412e01b56a32cf31f8da37234b3859b3013e35daaff806b60cc00550`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f7e0cf6ef7ea5036dc344617893905cf6d6d512362eb3e38fc0d0dbc6bfc17`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97948803dcc2bcc57916b670d8982b6e3e12d244d9471073640caf04816c306`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:494d2cf3e7fac63e031e0c02319c428ce7420a9e254f5bb2c6e177f15bd2a8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bcd1a00cc12bca92e35286f8b0fe8d85c847108ab1c777c1f42d017794b5168`

```dockerfile
```

-	Layers:
	-	`sha256:fb768aabcf004fa31fe669d97982beccd8c2f5a8f37cc0122ef369dc39205c06`  
		Last Modified: Tue, 03 Feb 2026 04:30:31 GMT  
		Size: 2.3 MB (2280465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe2c695d2b0f6ef93b2c0fc48f00af91038e73c664edc15c49233e7d78d4ca78`  
		Last Modified: Tue, 03 Feb 2026 04:30:30 GMT  
		Size: 21.5 KB (21457 bytes)  
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
		Last Modified: Tue, 13 Jan 2026 00:42:56 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ca9739d6b026ec1d4cd350482fedc4374621d2428ab77e18051bdb8ca6c93a`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 1.3 MB (1287208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caf308c9322d7b7ccb72a3b032126ea9174c0dd19d5133f792f459c5f0fec63`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b077996a21b00611176c639502288dd2a7a31e063ef348d46a1652665d276aa0`  
		Last Modified: Tue, 13 Jan 2026 02:49:35 GMT  
		Size: 37.7 MB (37661435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088f373e260e56fe68e120ff78469b633199ef4d7e6980f6c1706b0628c090ec`  
		Last Modified: Tue, 13 Jan 2026 02:49:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b70dc93001436daee4f4c2269d3b473cc83687fd15af6b3b65b15d67a592ad`  
		Last Modified: Tue, 13 Jan 2026 04:00:39 GMT  
		Size: 6.0 MB (5970309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64083097cffea937936c9ec17bfa648c81bbc71f8d05d684b7afb9e52a48d5c5`  
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b5966fa1c56255ac85fd3cda423eb24e7808ebd4ca2f9f0ea681e3e09bfc34`  
		Last Modified: Tue, 13 Jan 2026 04:00:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feefc55a043cc735826153c6bbcbc2f26bc3b8b365fb9dd174493eeb4c568d44`  
		Last Modified: Tue, 13 Jan 2026 04:00:37 GMT  
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
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 2.3 MB (2277355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce0ea0b7db35baa06510b1a0264df2ddf0c3651935cfe0f32813ad862ea1efe8`  
		Last Modified: Tue, 13 Jan 2026 04:00:36 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:9a3cafd2ad15ecca523d44c12561730c9618fcb6a8a324c012616df63417cccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80944198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2391227cf9ff745e5a0ddc2e174b4f2162089c1f4a73ebfe775fe96933d8f3d7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:13:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:13:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 13 Jan 2026 05:24:03 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 13 Jan 2026 05:24:03 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 13 Jan 2026 05:24:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 13 Jan 2026 05:24:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 13 Jan 2026 05:24:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 13 Jan 2026 05:24:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:24:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 13 Jan 2026 05:24:04 GMT
CMD ["irb"]
# Tue, 13 Jan 2026 09:00:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 13 Jan 2026 09:00:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 13 Jan 2026 09:00:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 13 Jan 2026 09:00:45 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 13 Jan 2026 09:00:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 13 Jan 2026 09:00:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 13 Jan 2026 09:00:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 13 Jan 2026 09:00:46 GMT
USER fluent
# Tue, 13 Jan 2026 09:00:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 13 Jan 2026 09:00:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd359a7e5d3b012a0e1f773e5ca872b7185e1ae4c53f7a9a7d797ae3eaaf8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 1.3 MB (1309726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49eeff64fa1ee2c5a20375771788d22ec3d5ad95481b75598a70ada63b47d8fb`  
		Last Modified: Tue, 13 Jan 2026 05:19:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5604be4a4b60f4fed68c22b913b07851aa0414cc66ee4da7ee7c4338b2e5d28e`  
		Last Modified: Tue, 13 Jan 2026 05:24:26 GMT  
		Size: 39.5 MB (39519922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc1dc23f8783cc9ad3639c62138f859289801c771b5a9e82fd86f8e4e4f7d19`  
		Last Modified: Tue, 13 Jan 2026 05:24:25 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e30a59d33d2a25b91e6031d498d0e8223513a391ec9a792eea32735baa9de15`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 6.5 MB (6516555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f924ba79838c3e65a0a1331631e11f5844fcff2d3c1c940dc123fab38974a2`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c3db13e0b69bf0fb77f89fca056dada7d7cf70bfe910ac9c2a95048d221003`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb4153c5f33f3ac2b2b9dd2e803c3ed885e8990d990b99f7d129ee38342af3c`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0032be699998ed132a2460102525b0fc79f3749b8ae840292df4cfbe7d33dbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a97bdbdb1fc3ecd09b897233c3be4d5e82e7331f90aa9d007be0b7e8e5f1f1`

```dockerfile
```

-	Layers:
	-	`sha256:ccfacc43efb7a135d5fb8cba44cce1125970f2e76f94c86a2e668fa770ee3eb9`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 2.3 MB (2283702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7b890f4811a2723a742990c05386c8fff28e65cec0ee2946431c1b38970752`  
		Last Modified: Tue, 13 Jan 2026 09:01:10 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:b1c8103ef9d6bd1a2d4acaa83c631bdc92e00a34026c88d668605aaaf50a9084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76705553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80b4cea4899143ffdc5ffd2fa8c5c6324ee8452ca49c9136d94a09fcf89d1dc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:49:44 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:53:51 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:53:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:53:51 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:53:51 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:53:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:53:52 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 06:00:35 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 06:00:35 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 06:00:35 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 06:00:35 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 06:00:35 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 06:00:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 06:00:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 06:00:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 06:00:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 06:00:36 GMT
USER fluent
# Tue, 03 Feb 2026 06:00:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 06:00:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0ef58ef1eb78dd947e41fe50adfe7b4ab7ed59de6adb1cee9b213c29193b84`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 1.3 MB (1294514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6191cacf2fcbd60736c6c6dd3a35edf5fb265ba19e0504896f4a96d590bdc0`  
		Last Modified: Tue, 03 Feb 2026 04:52:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2e7a1acf75697b829c5674d2af59db59b82bd932f96d1c50df559112643e50`  
		Last Modified: Tue, 03 Feb 2026 04:54:07 GMT  
		Size: 39.2 MB (39191476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27dcf4be1994bc1f0cbe0b29edacbaeb7643532854664d63ed921b9823209fe`  
		Last Modified: Tue, 03 Feb 2026 04:54:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8836a2a3d5fe0612bd6f486ccf67502c90dca13b55f0ee3015dc8fc9b6dcb80d`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 6.4 MB (6379016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ab910ede55a870b32fe8533f6e8da853c247e99cabc2a0d54ea29e1f21a75a`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18813b9ae4d1bc8ed0dea132c93ede5766cd2fd64a961a8f60770e1163afd0a4`  
		Last Modified: Tue, 03 Feb 2026 06:00:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d235fff2840bba22a65cc11d16cfc6c02d9b103745e92481615dde3a9ec9bfca`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:833aa0335c34fbde7814ce09c890b3155346bc8500bd98a346ce1c02d8a7f823
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f3e40c9d0bd52e3f4614bf12dbb9e2b426d8aa9e7c2e702cad2ffbec47004`

```dockerfile
```

-	Layers:
	-	`sha256:a03784ba6816bc7a3f5cc90a89bd87aeda3703bd11775b3e06f739dde63954f0`  
		Last Modified: Tue, 03 Feb 2026 06:00:50 GMT  
		Size: 2.3 MB (2281638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39680257795ba8f20d5fa4200ee53f00d46bef5378ad0a8ad8fd43a097220b5d`  
		Last Modified: Tue, 03 Feb 2026 06:00:51 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
