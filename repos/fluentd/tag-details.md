<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.11-debian-1.0`](#fluentdv11611-debian-10)
-	[`fluentd:v1.19-1`](#fluentdv119-1)
-	[`fluentd:v1.19-debian-1`](#fluentdv119-debian-1)
-	[`fluentd:v1.19.2-1.0`](#fluentdv1192-10)
-	[`fluentd:v1.19.2-debian-1.0`](#fluentdv1192-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:aa9b6c04232a11144fa83bffa8902e2779edf94c8aff76d5bea42a8db5965c26
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
$ docker pull fluentd@sha256:86e84bbd6c545a47659b7ee6fad003f49a97de4b123d3a6d1fb68f5542d59435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79227327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a0780d380896e171f5bf348d0dc0e6c368155349908f1bf89d9baf2a1cad62`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:22:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:22:30 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 20:22:30 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 20:22:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:22:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:22:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:22:31 GMT
USER fluent
# Tue, 24 Feb 2026 20:22:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95c885d11163cea6141f2874f7609fd353fae57178c697f1a7d40224f7b00cc`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 1.3 MB (1279331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7f5fbc95c257016cbdb5dfe0a0139978a0a4a0d17362943647c993cd4bcb99`  
		Last Modified: Tue, 24 Feb 2026 19:49:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05f4e549e9c58aeab34c05f03badc598c63a0b59ae9c2fe69be781ab5544df`  
		Last Modified: Tue, 24 Feb 2026 19:49:39 GMT  
		Size: 42.1 MB (42112489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce46bb75e106e62f4498c163d02fd7018cc5ceaa37cf6b822414c2107df184`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f59026a1925dd53f562c18d3b963c4a30e709dc70ae319df12164c9ab8ff9`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 6.1 MB (6054480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada8589f55043b5e553c835963c974db9e9d8842e4333c7b6003ec903edef689`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a121bb92b77148244102bcd1a61443fc53ce646403d9b52c35aca9feea6e74`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baebd31418b4c9c62b6aab7926059fc5c79306c5d0580e654134017802fa6d6`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:e35e8cd467bb2f2ba07e7351ce23dccbfe36f290bea9e917f8ad955d2bc47527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baec12c16182f271c21dba4a627dad83ea637f492e558a2def52c57372669c0`

```dockerfile
```

-	Layers:
	-	`sha256:87beb35f6ddcf4b58a92b15ae5b3c11e235b8de2461b91c3627e12496fa07f77`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 2.3 MB (2281482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f392ca696149469d3691c7ffdbffb55dba0a7cc874998211f69c4b033b7d24`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:702bb1b758b2b0b86544a326a57afe656f1da4018d2f2ac5e22a9596d9ea5dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73075764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52d7f1c907ee2f76702409fbfe17af5316afdb353b4746714b8f7394312884a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:54:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:54:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 21:54:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:54:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:54:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:54:58 GMT
USER fluent
# Tue, 24 Feb 2026 21:54:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:54:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc96269d7ff6661f7c783aa28ef266b6a3454b0b7270f35fd67c75efbb126325`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 1.3 MB (1262995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dde3052860b01def3c7729ab7e0b552cfc8471229c632727c524ba36ffa87c`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feb54b5087fc558951fafdb4a294dc5d0cfd9f91b23c76b4e5f03fb58403146`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 37.9 MB (37906244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd1652237e976a13ba3e6c119a312c9ef9b52d4d968f91702f2ed8dac11a6d`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8f4af827fa0ee9a1256892f1bbf83c4271c6a35814b9292176c3c078b13f5b`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 6.0 MB (5956521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fc31c05c8248f02920d77d8c9ba45d5403895207860b0ed4c01a5e2b6e86d6`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f480ee64da643f3dd1a9521699efb88c5788cc57f46d3c16546f8d1e0fd581a`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794edd3187fbf592f533456f685e8461ec4a4f97ab6d80e3f2777fc727af72f3`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:aeff6eb65638d187ee9dfc2632bd9a6fe5aa475c7732e02050a037648f7bd08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d7bc32560f9f9f482c4f0d1edf21542d17c45a3a16f10e6120f92b58bb2b61`

```dockerfile
```

-	Layers:
	-	`sha256:c5516e6bf9c46bc32b1d45a4de020a57104bea2b0d21a174426bc1b3b3e5a2aa`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 2.3 MB (2284453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61ab6a4efa546f12948f77ab6e386e9c29a6aa900ea73c9b8357b1bdb43c43e3`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:249cd06a9583c174022bc1662a638183730f2eb3cf11ad58645af47ac58d552d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70944650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a202282d8340e112924e8c4e6b6f741d47d8511e6d65071ccf02ee62a9164`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 21:09:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:09:12 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 22:00:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 22:00:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 22:00:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 22:00:49 GMT
USER fluent
# Tue, 24 Feb 2026 22:00:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 22:00:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14feba02466030de4233bb2b9b4ae7bb8d22598db9db35967cc9269952aa2190`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 1.2 MB (1236637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991f1e7bee0c079b1385009eded49ec5445b76573d3c6311e6d7a8472bbeebd`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f4b57fa9f91ef9277385833d43232d221aae42613777d8a1984c4d140abdf8`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 37.8 MB (37767330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865adf2d3ca7b76be7f98186142a67e87adc8e14da1a9c847d4838d387f91d2f`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6215cd02e856f3f916f009645d1930216f1ea5046f717331deb0b0c628c0cb1f`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 5.7 MB (5724546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbcfa781ef6a32d1924052e879b40cf20670dc5460b896852bb939d35097f6`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f810d4742ff15c72ffa1d88314e0af2232943762e952ba81264158f7c11a5e7`  
		Last Modified: Tue, 24 Feb 2026 22:00:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0491a7058409e826832ddd60b3500d0531fbf847813171676e8df47d10e7e60f`  
		Last Modified: Tue, 24 Feb 2026 22:01:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:616d833662b654cfdaefcd601933ef26a2c132b460c51932d43532a964e574aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141883a718ab52bba48c5df7dee9157f0bbb26b80a0830cac65470df72d406af`

```dockerfile
```

-	Layers:
	-	`sha256:3e6cabc9f406ac1d02f047192c16317f3ae30604e3c63cfd48324204afffb01d`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 2.3 MB (2282894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3db94822a243938772aec32d2ec10453a6f7b111f889e584043a103671ac7d69`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:828404f45a0b0a32fec514fa74e419ac06f5a23433cd5d604319cc175e82d054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79521874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d16ebbf1045c14f44b80173504653196573d47d64c6678c057ce7b6f3daa26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:38:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:38:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 21:38:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:38:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:38:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:38:23 GMT
USER fluent
# Tue, 24 Feb 2026 21:38:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f75b690a5fd55169fbad21a29d8ed315a9d4042c310b1bf6f573673b222fc`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 1.3 MB (1261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c26ba3937fd2b59db15d9b6d2d658d4dd4063b544cfdc5543f937af1ae20ee`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af054951d688ba98eecceef225934514c1bce049b94d72213bb07dbde8fb87`  
		Last Modified: Tue, 24 Feb 2026 20:01:00 GMT  
		Size: 42.1 MB (42074135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639b1a194a41b5d55ce4d7d2ec84ba51375ae840f4a37543134a924795e35a07`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a08ed296b9681998efe65e6e0547331e19e4c85d582e56ee946b40f75bc53e`  
		Last Modified: Tue, 24 Feb 2026 21:38:32 GMT  
		Size: 6.0 MB (6043953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51dce7afff466c28dbaf5e1b0183007860bc4d1b1ab4f805ff142df8b02efc`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c445911edf772b7b26b1a963f84eb02edbb6edf42beff8deb7d06eb236bf3`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205244818e9d9295806167b757eeccf4c11d403b60d31509b2934897f702154`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:ca791e8bd0f179910fdb549ce401bc962cc8bb5ad45ced6d1882cef650ede648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78018d21a04e4f823186dd34a8c235892d68b619bbd54d8343306f0feb00f0f2`

```dockerfile
```

-	Layers:
	-	`sha256:23aa4569b3fa9dc8f92fd32abf7c895fd4d19a8e8aa44bbc2fa60dd79a77028f`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 2.3 MB (2281754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50619cb3792635e604919c80a6837451d9333523df0b41771df7d709c5f105ad`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 21.5 KB (21455 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:d4e441291fbcc948534053a6429efb66080283ffde02d2ff0ed8c733968d9de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985aeed61e2de83466ff38ae8525b6052c73fe6a2c5dbe6fafccf426c3526b10`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:51:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:45 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:14:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:14:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 20:14:50 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:14:50 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:14:50 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:14:50 GMT
USER fluent
# Tue, 24 Feb 2026 20:14:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:14:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a892ff57419277a7fa8ad912b1813f1159602bd6d8068badf5bfb1d62a14993f`  
		Last Modified: Tue, 24 Feb 2026 19:51:53 GMT  
		Size: 1.3 MB (1287332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbea3e8ba0db554c2fac0167ff3e4daf51f3fbd5bc330d7217898dd5c65f7d2`  
		Last Modified: Tue, 24 Feb 2026 19:51:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2d9cc1d12b4edaca10bae974eeb96048293aec72576d8c3e8254d4431ce48c`  
		Last Modified: Tue, 24 Feb 2026 19:51:54 GMT  
		Size: 37.7 MB (37661562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee811540cac1162511fd45e13f42fe19541d1f73c7d8a45b816037c2d0668a`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fb7539d7a3851caa96e2bcccbb66a68fcf4dac4973414f51370ae37c4622ea`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 6.0 MB (6025681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25798218224060dbc499d8986f06d2eb074d58bf9345da4f05f6ed75f35fbc62`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed273dda7a96de12238121a09a97770b30f1889adddd7a0d5ffadceba370b6b`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0aa78822ed9aa54b3dfb41392b36b646e4f9bc15bb3037b819fad46d8f4fcf`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:a8ce02d3271a6c38e6ac9845cc16d1c54480c4d0b2d183fb82b7d091b9387294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b96e28b5c2f4a99203e65e38ac879bef38fbdb184706b87fc865ed232d9ee3`

```dockerfile
```

-	Layers:
	-	`sha256:a48b838e0998fb5c2903ba45219be4a3b3db2a074344147cbfcb58b4d84339bb`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 2.3 MB (2278670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587f45001b4aef0def6ce0691f65c51db7c9f957fe89daf5806210568c13de31`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:3e85b7afdefefc0ceed38702aa8c6e83e6d900b88a7bba22e2988cc09521c314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81007295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92db795cc55a308b287141133fb2ebb98c3099b9cf82951c8aff9c3aaa3d8a3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:04:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 09:04:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
CMD ["irb"]
# Fri, 13 Feb 2026 18:50:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 13 Feb 2026 18:50:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Fri, 13 Feb 2026 18:50:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 13 Feb 2026 18:50:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 13 Feb 2026 18:51:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 13 Feb 2026 18:51:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 13 Feb 2026 18:51:00 GMT
USER fluent
# Fri, 13 Feb 2026 18:51:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 13 Feb 2026 18:51:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6be1f9ad8d9708d6d1dd902519422f937c816172bb2279df8827177290ce2c7`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 1.3 MB (1309384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69016493cd4b81c51b0ebe7726a06117b8c667e58289628f10d4662f959eb918`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae5d6a287ac9deb00e76ee4f5bc8133dfa2ad449e09b28cbcef3715fe45f124`  
		Last Modified: Tue, 03 Feb 2026 09:09:01 GMT  
		Size: 39.5 MB (39519472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9277fefce554077ed90bf6814e28a9db303a96069b78e13ebbb958a92daa6d2d`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb39087a75c520eecf6fa1d6cca6b087321ba9c79cb338599d9739d4491b11`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 6.6 MB (6575848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19afb70fa211158dd4f6a97285e69a623a026dc5cbeb9c946cc0d9597470585`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff208f82e22958984a23e4b02712a779bdb4570c8422c467e124a8b264b0bb43`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9649c1f8ea25246f0060ad4dff7af4b5afe7280fec821c3bb316ce49cd25e607`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:372534f2d3f54414e8b10d874b438910a672bfe189b65a56796669b17fba2c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3279a02c907e4d5bf163f52ce92ba2acd37a5dc3693c358ad599f1dae6dc53`

```dockerfile
```

-	Layers:
	-	`sha256:772508226cfbbcde2d89894fbb9d6bfa67f21f85f9c7820774e4c4024df3c785`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 2.3 MB (2285017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f660251e609f7c92dcf6085728502cdc3bdec0fc40fde1ae3dcbe42b7e15d262`  
		Last Modified: Fri, 13 Feb 2026 18:51:19 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:325c4ac442f736c13b434e56b7fde81681f7b089bb9a88139c4c8089520b06dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76758781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4123c819169f7a1c43c68cdbf71bc0fce9aeea2a49950405f4f3c7953a3d6d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:02:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 25 Feb 2026 01:32:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:32:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 01:32:11 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 02:39:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 02:39:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 25 Feb 2026 02:39:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 25 Feb 2026 02:39:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 02:39:37 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 02:39:37 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 02:39:37 GMT
USER fluent
# Wed, 25 Feb 2026 02:39:37 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 02:39:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4914443d3c4184b2c3ca5f7f265c77f7783c5fe40f5ff77daa520ded4b0a2c`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 1.3 MB (1294517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def914eff926e8e33e8d2ea6891e3ece82a54502d942da1cf995fac0cf626932`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fad6ee4d8be5d7dbfd8551d2a5d070571e5d13c57cfc9d2618d596970e34c`  
		Last Modified: Wed, 25 Feb 2026 01:32:41 GMT  
		Size: 39.2 MB (39192544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb56a57c12ad1160bc0ee7c91d149dab3f7a2a858afd9771d4f967a14a4533a`  
		Last Modified: Wed, 25 Feb 2026 01:32:39 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d528a35268e8e46fa75fdda5d210e6dbbb535b26387f024349e2351e5455edfd`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 6.4 MB (6431145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4914220566b082bf5096917093d86a2f05c15edd3bf91a0aebf285700aef707f`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a611c57f9809a0ad97f6a54adfb486209c5531824142c8a9f79fe2238b7953`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c41433679913e9f12adb749646999e0194b8012806661df0a3a786f5e6deea9`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:45ce6eafa5ff53cc997cf7bf28d3a7cd68637982865c75eaa2b9962145a945ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b56380c11cf0412a468c8aa4e2a1884f4b5ea388938a8fb40abafee4a64259`

```dockerfile
```

-	Layers:
	-	`sha256:fa1aca00461b819cd8ecd3a4ffe90129f1108cb248f3958784a2f61d22396899`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 2.3 MB (2282927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ad2111eaf7ad708910e559db08048a2777e2fa6a210307b46f77f9c393b797`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:d2da1198df50261b8d16093e72b668ff061c5d546f5c54c4347612b4d87237ef
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
$ docker pull fluentd@sha256:4771f99b3a0503b5f8ea0aebf183750b9ce43ed3a05ce8781531da406a3a9b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82052691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6913e6da5ea421435e3eda6ae6f6d8538532a259063eb31d0b0d52cd3a68563e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:49:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:49:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 19:51:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:22:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:22:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 20:22:23 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 20:22:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:22:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:22:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:22:23 GMT
USER fluent
# Tue, 24 Feb 2026 20:22:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df150c11f2d58174c3aae4f604576f28b185b28a616fe846715511ed0f352827`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 3.5 MB (3510182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ec15dd55a363b0c43f66110f30b067c2de0afae2c49fe4e1b69b4ab7991116`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4928b0a24e7aecbedd132a84cade78772c1b4bbfcc2e6092a03853a9dac3a3`  
		Last Modified: Tue, 24 Feb 2026 19:52:03 GMT  
		Size: 36.0 MB (36010873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a29a156687ac9ec641538d5375f0856632e3417fcad442c59ce5ecad97014d`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e29c7a5c16cb97f5cb44bbf2b0a3880e500b981ac81d6136ac0d6f397198095`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 14.3 MB (14292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5014efb356efee47753666b4ffdbe57af7f6d225b0276c700a1e1d028902a8c9`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae20c2ec95b5fd71a79cec01786d4b3ab525face8e909732bfb02e9db534b32`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8ecfe875da7355a981424f702e7ab999d742571212d4871f58d0b15a0d9f92`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:27fa70ae9e522f092017fcfa2d46d520511cc6a0c58547977cef315d61498d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778a0710dd9381f25082d5506f5b4929230c561b9c6cb4641df7e844c5fdc5b`

```dockerfile
```

-	Layers:
	-	`sha256:f0ddd225c0b68c934863f47ef5b1d58a2b491b20f5724431a4fc6ecfca3f7d1e`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae75545ce8a06fb0cf663745b8c622999210bac34e6b381ba033544a9d379c4`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 21.1 KB (21071 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d2d8eb7b5d6b6ee0824a8eac544b9ec87f8b2a559cca755e4a5d9eaa5c227661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75450577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84266c09879b21def70ebcba34f1f323fb275b9d977f060dfe6ad5c4f4eb23d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:40:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:40:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 20:42:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:42:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:42:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:42:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:54:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:54:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 21:54:41 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 21:54:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:54:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:54:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:54:41 GMT
USER fluent
# Tue, 24 Feb 2026 21:54:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:54:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0355804b1a863607635e8e60f82ed6fec21aeb11cd0f281ea39f54208fab3bb7`  
		Last Modified: Tue, 24 Feb 2026 18:41:57 GMT  
		Size: 25.8 MB (25765637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3eecc313abaf89f694406c0f1fcf4bb7ae74557455bf5d9df9661bd30185e`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 3.1 MB (3081092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de71683607fd2d40421fde9555243a10bc991cc34665772f5076f51820c98e37`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362d4d1eed694fdbcec1d943ce7b1e98cbb2c1ad48d3e647ba1a09bf1b8244e`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 32.3 MB (32331019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1afd6aa174dc2b046476cf27e76cee1cafda009dffa6906571cdaa4d530a52`  
		Last Modified: Tue, 24 Feb 2026 20:42:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52a17ce755df3d0c91f11aa754ef1c72396853ecaa5630242702b0e627ae78a`  
		Last Modified: Tue, 24 Feb 2026 21:54:50 GMT  
		Size: 14.3 MB (14270433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9570ac50ead433b23781f3e31a9ab171b183e0294710a24bf4edf3f66fd403b6`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f070a174fbddbfe1df03c2269983985072081cc6500426a3e8964fca59c08f`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d553391c9fed1836291de7c8f673b8ad6eeda4af2d7f43d2ef52b170e9ef49e`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9b15b7fd80216027ccf3376da5c43355e7aab18a48c94402cb0741eef06e0e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59b7dda6c296f596a2198d566310724eb1706c0563d1d980abea0dee67a308e`

```dockerfile
```

-	Layers:
	-	`sha256:f545739d6026404686095c3900d847a818ea4e5dc0c7bfb545962c528aa45a03`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 2.7 MB (2674277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccd05a58686bab81efdd0be5560999d58c57ba74f5bca494348b2c435ba5a37`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 21.1 KB (21148 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:51332f4710759ac1bcd42f09508fed0d458d6626321adc4b5b5e7ce7000d9e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73227327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4da8dd161bec02c3770d8da8c0bab3cb26ca4d512bb21aefdf93cde6736b69f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:08:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:08:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 21:10:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:10:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:10:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:10:22 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 22:00:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 22:00:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 22:00:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 22:00:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 22:00:49 GMT
USER fluent
# Tue, 24 Feb 2026 22:00:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 22:00:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181815e651be48f7e0fbc65e79272338249cc4825fc8fb8d39e40e6206f8dc88`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 2.9 MB (2913768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07adaf3cb294573dec3eaf97db055d58921f4b821cab9877be5cb40a718a134`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ce340f292387a0bc0b908fe2b2b1b642907fb498c28a05e7fc9b06b3d1c024`  
		Last Modified: Tue, 24 Feb 2026 21:10:31 GMT  
		Size: 32.2 MB (32168041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99bc1ac1583e8e092909d0d3c2c9219be66af29ccf3f8047eabfcd104191f86`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c493bdbc8c593f0f92d04ef24d0fb241bc89253415d11b73ae7376e631bbe1d`  
		Last Modified: Tue, 24 Feb 2026 22:01:00 GMT  
		Size: 14.2 MB (14201729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbcfa781ef6a32d1924052e879b40cf20670dc5460b896852bb939d35097f6`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d8fe43c9f1949bc70ba61c37b1f6dfba74b3dadef3bfc3276c06393669629`  
		Last Modified: Tue, 24 Feb 2026 22:00:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef48f0f4f167872496d02434df4f78ffc601fd9b3cfd0e5084a38dcee17dfcd5`  
		Last Modified: Tue, 24 Feb 2026 22:01:02 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3a132251f9a5ebf77c40c2bb76e5f4a775673d99efec076c17409bb0a027af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1fccab6e8e77f90628b336eda8b365a115aede522ccf210a7df18f4a0993bc`

```dockerfile
```

-	Layers:
	-	`sha256:ef83f68dbae07b06ed5be279e4fcd2b54788396ac6a853dbf4ce9f79b021abd6`  
		Last Modified: Tue, 24 Feb 2026 22:01:11 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f20d0220a8d7d02f0ce981d622fb8293876536f21dbb822a520ce1954f57bb4`  
		Last Modified: Tue, 24 Feb 2026 22:01:11 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7040043d4a50aa3e045ec0c0bf1e59ee80554641fd45ad8db1a50a709d8e9baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81670612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15440eb9f2c5a93491df065cf4a69a61d0cb03cfeeecfbfc302978338c95464`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:59:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 20:01:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:01:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:01:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:38:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:38:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 21:38:25 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 21:38:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:38:25 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:38:25 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:38:25 GMT
USER fluent
# Tue, 24 Feb 2026 21:38:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a6a207c45083e2aa3cda7da1a0180e6755cd4bb26c170a1f3760fe5bb4d45c`  
		Last Modified: Tue, 24 Feb 2026 20:01:34 GMT  
		Size: 3.3 MB (3341511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c113a5f4448070219ca58e995aaa6d5837eb674822494cd99ada8e20e5ae657a`  
		Last Modified: Tue, 24 Feb 2026 20:01:33 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28198b8b91be8fbf9abc3de9a3f968e48296bb9fbec2c8191bc44e151b9c58dc`  
		Last Modified: Tue, 24 Feb 2026 20:01:34 GMT  
		Size: 35.9 MB (35911763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ff80bd722a6c168e8aaac8bd77c49137a2803149ddb3db43d6daa65c02328e`  
		Last Modified: Tue, 24 Feb 2026 20:01:33 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be27fcae1cae3e6ea9f5c8ba393cf3f95c332a14527581a06c7092610f2b57`  
		Last Modified: Tue, 24 Feb 2026 21:38:38 GMT  
		Size: 14.3 MB (14298864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7ce0476c9336412c661397d95033d94258000afa9072a7c76500c9aa3850d4`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efee239239a544a65959d9d868adca407f05a9c825678de07fd9ebed726cb4a`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa98943c28255aace405a4febfa3e5481226b13e1377d811ed0b7d5cc50ad7d6`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:80f98fd9ff202a89bbce13ae8f00cf91a89ab9756f9f36d892f3c3b6ba08b1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3086a2fe2c83218e8388b72dbbd990614f326a3df0ca4e50b53bbe830e81ff`

```dockerfile
```

-	Layers:
	-	`sha256:d1729083e144550a50e5125994d665085a0511312e4eb74a87c3f0226c21262d`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 2.7 MB (2670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0394b9abb40256f20fb5740c00032f1216c1c590288ebdee67e9cb854e375f`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 21.2 KB (21167 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:5c4f6ffad93fbad17d6aa131216428e1c15644a4903cdb41f62536a4428fd296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78983951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207f915b460d5665d0a02b673c850e5e842591604a447db314e19b0d580bba2e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:50:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 19:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:52:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:52:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:14:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:14:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 20:14:43 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 20:14:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:14:43 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:14:43 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:14:43 GMT
USER fluent
# Tue, 24 Feb 2026 20:14:43 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:14:43 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc97e1b8827deb66c8f55b63aa24a717166c23c116bfd32fbd210f382acecdf`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 3.5 MB (3512925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17762cd40b5013880f2dc74d7021819b98739a6250505c6d6bad05beb0baba3`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57afe41774a91d5bf4827fd241077ca7fd3aa50bbe5c7d27d3487ee987de1380`  
		Last Modified: Tue, 24 Feb 2026 19:52:17 GMT  
		Size: 32.2 MB (32163465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e92ca4f16ad2c4f2c1e21f71b07ebc1a54c39ecf03d4123e2195457b6d7a4f5`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7f26d050631b1598d9563e0ebc9413bba3819d6d8800733ed659015cee7c95`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 14.1 MB (14083462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab423f0cf0e00bb38746a54ac895cc370be34077dba1ebd5dac64fdd14eda`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccb2f2eba9b30c0067b2d308ca5a1430a1861e6fa16743fb3b8bb1198917c83`  
		Last Modified: Tue, 24 Feb 2026 20:14:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a12c5a6f6001ec1271796c5d8756d429f533928dd1339bc921c2ca0f8f2e767`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2ed16d2be1481d029c17cd7582c6d7d5216d4bd26615e300f655ddd8f00bfdee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820d87dc396a6dfd3ad9d5335e7e95d50587dce35b25f781b48f1b3b430e4cc`

```dockerfile
```

-	Layers:
	-	`sha256:44c55ddf3bc8749a5defb8ecbf589437309c16ecebdc474d4195e0f604821ce0`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e74b71ed7da334df84404550da95607f6a249bd0c7be0718ed69c1a594bfbe`  
		Last Modified: Tue, 24 Feb 2026 20:14:51 GMT  
		Size: 21.0 KB (21048 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:816226b07b90f84016be1328a9f3507e26b6cb66578da92290bd1831340087c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84311789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4076c70acc476b7dcaace335f523a9cb665fe1bfecc55d2807f1966ecc5ccac`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 08:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 08:58:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 09:23:26 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 09:23:26 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 09:23:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 09:23:26 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 09:23:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 09:23:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 09:23:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 09:23:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:23:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 09:23:26 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 12:56:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 12:56:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 12:56:13 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 12:56:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 12:56:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 12:56:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 12:56:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 12:56:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 12:56:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 12:56:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 12:56:14 GMT
USER fluent
# Tue, 03 Feb 2026 12:56:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 12:56:14 GMT
CMD ["fluentd"]
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
	-	`sha256:7587171a4e629afb8dfff49f88e0e8350eb9c14f7193943860172be3bfb7a0b1`  
		Last Modified: Tue, 03 Feb 2026 09:23:47 GMT  
		Size: 33.8 MB (33835373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94869493584d5b727bcda6a2a93c575474b6f8179584ecadc24f1976353f7a3`  
		Last Modified: Tue, 03 Feb 2026 09:23:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d604f17bcaf377736a812a439aa41739027dffd88b28601cbc377131dc5a0f`  
		Last Modified: Tue, 03 Feb 2026 12:56:36 GMT  
		Size: 14.7 MB (14694522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198c70af543b0996c912f2776157aff7e21133ce11c579fe38572df44fc4b412`  
		Last Modified: Tue, 03 Feb 2026 12:56:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7858fa7f32b098adfe2abf4ad896a6095bfa8af1e2a8207bc4a9cd12309a221e`  
		Last Modified: Tue, 03 Feb 2026 12:56:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2be0185de3db75a1ebb6ad19140bb6543d12f82ff03cf77026fcc406fde83df`  
		Last Modified: Tue, 03 Feb 2026 12:56:36 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8f83b89eacdc68069c996c9785bb19a3e17e64e29ab41221dfd471950abde9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b96dde2f57ea1b4ff5a69b724c753cfbf9777dbec8f226ec81b4b00f3bd7459`

```dockerfile
```

-	Layers:
	-	`sha256:36274d2419f74c4a6796c67f5c55f19de80b8111f0940e0dfa50250388c6913a`  
		Last Modified: Tue, 03 Feb 2026 12:56:36 GMT  
		Size: 2.7 MB (2674899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038e108fb3ab6172e65294742ead6b0632b2120f3a8c6e66f4603ef98528db9e`  
		Last Modified: Tue, 03 Feb 2026 12:56:35 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:a39bcfa77efc7af7c937a08d332b07eb6ffee006aaafb9cd9b2d3c79f432cc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77599356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9df9d9b17e23c2dac02ed0c379d82b513e8b55c9e1fbe660cf61cad7cda9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 22:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:56:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 23:07:32 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 23:07:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 23:07:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 23:07:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 23:07:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:07:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 23:07:33 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 02:39:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 02:39:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 25 Feb 2026 02:39:21 GMT
ENV TINI_VERSION=0.18.0
# Wed, 25 Feb 2026 02:39:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 25 Feb 2026 02:39:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 02:39:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 02:39:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 02:39:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 02:39:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 02:39:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 02:39:23 GMT
USER fluent
# Wed, 25 Feb 2026 02:39:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 02:39:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee0a8590e769ec84c9c999b84ef7c697884603dfeac17e2f74cb19194158987`  
		Last Modified: Tue, 24 Feb 2026 23:02:46 GMT  
		Size: 3.2 MB (3171209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba25f0557aafc3759d760486d757d65a9bb3e1c108c3458785dc2ff39fc676f`  
		Last Modified: Tue, 24 Feb 2026 23:02:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8f23b843a21ce3f239a4d6af280bf2729dc51d0ac0483462479fae094340c`  
		Last Modified: Tue, 24 Feb 2026 23:07:52 GMT  
		Size: 33.1 MB (33104236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf4ff6bfa8f17cec32e84126297cd2c142213d9e37f0d2ffd9e7795450567b1`  
		Last Modified: Tue, 24 Feb 2026 23:07:50 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be13b0e8917723a0af24cbc141920b530c9a24cbe9d72925549598334842e639`  
		Last Modified: Wed, 25 Feb 2026 02:39:43 GMT  
		Size: 14.4 MB (14429986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831b0786c75adf02326337327216b324d581bb04e65603b8fc1dbd4a43135884`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08315f43215c0225ec306a8a7c05a553aeb6b2d2284697ad375315c7700738c0`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84550c0ddc77f8b63a983e57aadb590d16013d0a2b85a5d3cbe7dc9c29ec81ca`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9df0560ccf9cc0eb9a0040a1553bbd954239feadbac3cade9b4300aa6cc969ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1e46b02eaf9f954b5ac4771b7efae352a149c78ea63c9a8cbbb716083e91da`

```dockerfile
```

-	Layers:
	-	`sha256:50f8c4edc2f854be02126e76fddc0f06a70ce49cd96b71d70cf1ce2855500131`  
		Last Modified: Wed, 25 Feb 2026 02:39:43 GMT  
		Size: 2.7 MB (2667307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18427afb6fd0aaec0ae12fd27cdd134735954f8ad9f215bec007f6742693b4f0`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.11-debian-1.0`

```console
$ docker pull fluentd@sha256:d2da1198df50261b8d16093e72b668ff061c5d546f5c54c4347612b4d87237ef
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
$ docker pull fluentd@sha256:4771f99b3a0503b5f8ea0aebf183750b9ce43ed3a05ce8781531da406a3a9b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82052691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6913e6da5ea421435e3eda6ae6f6d8538532a259063eb31d0b0d52cd3a68563e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:49:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:49:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 19:51:53 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 19:51:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:53 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:22:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:22:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 20:22:23 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 20:22:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:22:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:22:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:22:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:22:23 GMT
USER fluent
# Tue, 24 Feb 2026 20:22:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df150c11f2d58174c3aae4f604576f28b185b28a616fe846715511ed0f352827`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 3.5 MB (3510182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ec15dd55a363b0c43f66110f30b067c2de0afae2c49fe4e1b69b4ab7991116`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4928b0a24e7aecbedd132a84cade78772c1b4bbfcc2e6092a03853a9dac3a3`  
		Last Modified: Tue, 24 Feb 2026 19:52:03 GMT  
		Size: 36.0 MB (36010873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a29a156687ac9ec641538d5375f0856632e3417fcad442c59ce5ecad97014d`  
		Last Modified: Tue, 24 Feb 2026 19:52:02 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e29c7a5c16cb97f5cb44bbf2b0a3880e500b981ac81d6136ac0d6f397198095`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 14.3 MB (14292967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5014efb356efee47753666b4ffdbe57af7f6d225b0276c700a1e1d028902a8c9`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae20c2ec95b5fd71a79cec01786d4b3ab525face8e909732bfb02e9db534b32`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8ecfe875da7355a981424f702e7ab999d742571212d4871f58d0b15a0d9f92`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:27fa70ae9e522f092017fcfa2d46d520511cc6a0c58547977cef315d61498d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7778a0710dd9381f25082d5506f5b4929230c561b9c6cb4641df7e844c5fdc5b`

```dockerfile
```

-	Layers:
	-	`sha256:f0ddd225c0b68c934863f47ef5b1d58a2b491b20f5724431a4fc6ecfca3f7d1e`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae75545ce8a06fb0cf663745b8c622999210bac34e6b381ba033544a9d379c4`  
		Last Modified: Tue, 24 Feb 2026 20:22:32 GMT  
		Size: 21.1 KB (21071 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:d2d8eb7b5d6b6ee0824a8eac544b9ec87f8b2a559cca755e4a5d9eaa5c227661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75450577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84266c09879b21def70ebcba34f1f323fb275b9d977f060dfe6ad5c4f4eb23d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:40:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:40:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 20:42:33 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 20:42:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:42:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:42:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:42:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:42:33 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:54:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:54:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 21:54:41 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 21:54:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:54:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:54:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:54:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:54:41 GMT
USER fluent
# Tue, 24 Feb 2026 21:54:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:54:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0355804b1a863607635e8e60f82ed6fec21aeb11cd0f281ea39f54208fab3bb7`  
		Last Modified: Tue, 24 Feb 2026 18:41:57 GMT  
		Size: 25.8 MB (25765637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc3eecc313abaf89f694406c0f1fcf4bb7ae74557455bf5d9df9661bd30185e`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 3.1 MB (3081092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de71683607fd2d40421fde9555243a10bc991cc34665772f5076f51820c98e37`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362d4d1eed694fdbcec1d943ce7b1e98cbb2c1ad48d3e647ba1a09bf1b8244e`  
		Last Modified: Tue, 24 Feb 2026 20:42:42 GMT  
		Size: 32.3 MB (32331019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1afd6aa174dc2b046476cf27e76cee1cafda009dffa6906571cdaa4d530a52`  
		Last Modified: Tue, 24 Feb 2026 20:42:41 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52a17ce755df3d0c91f11aa754ef1c72396853ecaa5630242702b0e627ae78a`  
		Last Modified: Tue, 24 Feb 2026 21:54:50 GMT  
		Size: 14.3 MB (14270433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9570ac50ead433b23781f3e31a9ab171b183e0294710a24bf4edf3f66fd403b6`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f070a174fbddbfe1df03c2269983985072081cc6500426a3e8964fca59c08f`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d553391c9fed1836291de7c8f673b8ad6eeda4af2d7f43d2ef52b170e9ef49e`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9b15b7fd80216027ccf3376da5c43355e7aab18a48c94402cb0741eef06e0e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59b7dda6c296f596a2198d566310724eb1706c0563d1d980abea0dee67a308e`

```dockerfile
```

-	Layers:
	-	`sha256:f545739d6026404686095c3900d847a818ea4e5dc0c7bfb545962c528aa45a03`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 2.7 MB (2674277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccd05a58686bab81efdd0be5560999d58c57ba74f5bca494348b2c435ba5a37`  
		Last Modified: Tue, 24 Feb 2026 21:54:49 GMT  
		Size: 21.1 KB (21148 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:51332f4710759ac1bcd42f09508fed0d458d6626321adc4b5b5e7ce7000d9e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73227327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4da8dd161bec02c3770d8da8c0bab3cb26ca4d512bb21aefdf93cde6736b69f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:08:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:08:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 21:10:21 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 21:10:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:10:21 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:10:21 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:10:21 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:10:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:10:22 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 22:00:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 22:00:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 22:00:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 22:00:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 22:00:49 GMT
USER fluent
# Tue, 24 Feb 2026 22:00:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 22:00:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181815e651be48f7e0fbc65e79272338249cc4825fc8fb8d39e40e6206f8dc88`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 2.9 MB (2913768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07adaf3cb294573dec3eaf97db055d58921f4b821cab9877be5cb40a718a134`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ce340f292387a0bc0b908fe2b2b1b642907fb498c28a05e7fc9b06b3d1c024`  
		Last Modified: Tue, 24 Feb 2026 21:10:31 GMT  
		Size: 32.2 MB (32168041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99bc1ac1583e8e092909d0d3c2c9219be66af29ccf3f8047eabfcd104191f86`  
		Last Modified: Tue, 24 Feb 2026 21:10:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c493bdbc8c593f0f92d04ef24d0fb241bc89253415d11b73ae7376e631bbe1d`  
		Last Modified: Tue, 24 Feb 2026 22:01:00 GMT  
		Size: 14.2 MB (14201729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbcfa781ef6a32d1924052e879b40cf20670dc5460b896852bb939d35097f6`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d8fe43c9f1949bc70ba61c37b1f6dfba74b3dadef3bfc3276c06393669629`  
		Last Modified: Tue, 24 Feb 2026 22:00:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef48f0f4f167872496d02434df4f78ffc601fd9b3cfd0e5084a38dcee17dfcd5`  
		Last Modified: Tue, 24 Feb 2026 22:01:02 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3a132251f9a5ebf77c40c2bb76e5f4a775673d99efec076c17409bb0a027af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1fccab6e8e77f90628b336eda8b365a115aede522ccf210a7df18f4a0993bc`

```dockerfile
```

-	Layers:
	-	`sha256:ef83f68dbae07b06ed5be279e4fcd2b54788396ac6a853dbf4ce9f79b021abd6`  
		Last Modified: Tue, 24 Feb 2026 22:01:11 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f20d0220a8d7d02f0ce981d622fb8293876536f21dbb822a520ce1954f57bb4`  
		Last Modified: Tue, 24 Feb 2026 22:01:11 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:7040043d4a50aa3e045ec0c0bf1e59ee80554641fd45ad8db1a50a709d8e9baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81670612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15440eb9f2c5a93491df065cf4a69a61d0cb03cfeeecfbfc302978338c95464`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:59:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:59:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 20:01:24 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 20:01:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:01:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:01:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:01:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:01:24 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:38:25 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:38:25 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 21:38:25 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 21:38:25 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:38:25 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:38:25 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:38:25 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:38:25 GMT
USER fluent
# Tue, 24 Feb 2026 21:38:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a6a207c45083e2aa3cda7da1a0180e6755cd4bb26c170a1f3760fe5bb4d45c`  
		Last Modified: Tue, 24 Feb 2026 20:01:34 GMT  
		Size: 3.3 MB (3341511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c113a5f4448070219ca58e995aaa6d5837eb674822494cd99ada8e20e5ae657a`  
		Last Modified: Tue, 24 Feb 2026 20:01:33 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28198b8b91be8fbf9abc3de9a3f968e48296bb9fbec2c8191bc44e151b9c58dc`  
		Last Modified: Tue, 24 Feb 2026 20:01:34 GMT  
		Size: 35.9 MB (35911763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ff80bd722a6c168e8aaac8bd77c49137a2803149ddb3db43d6daa65c02328e`  
		Last Modified: Tue, 24 Feb 2026 20:01:33 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be27fcae1cae3e6ea9f5c8ba393cf3f95c332a14527581a06c7092610f2b57`  
		Last Modified: Tue, 24 Feb 2026 21:38:38 GMT  
		Size: 14.3 MB (14298864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7ce0476c9336412c661397d95033d94258000afa9072a7c76500c9aa3850d4`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efee239239a544a65959d9d868adca407f05a9c825678de07fd9ebed726cb4a`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa98943c28255aace405a4febfa3e5481226b13e1377d811ed0b7d5cc50ad7d6`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:80f98fd9ff202a89bbce13ae8f00cf91a89ab9756f9f36d892f3c3b6ba08b1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb3086a2fe2c83218e8388b72dbbd990614f326a3df0ca4e50b53bbe830e81ff`

```dockerfile
```

-	Layers:
	-	`sha256:d1729083e144550a50e5125994d665085a0511312e4eb74a87c3f0226c21262d`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 2.7 MB (2670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0394b9abb40256f20fb5740c00032f1216c1c590288ebdee67e9cb854e375f`  
		Last Modified: Tue, 24 Feb 2026 21:38:37 GMT  
		Size: 21.2 KB (21167 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:5c4f6ffad93fbad17d6aa131216428e1c15644a4903cdb41f62536a4428fd296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78983951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207f915b460d5665d0a02b673c850e5e842591604a447db314e19b0d580bba2e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:50:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:50:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 19:52:08 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 19:52:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:52:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:52:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:52:08 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:14:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:14:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 24 Feb 2026 20:14:43 GMT
ENV TINI_VERSION=0.18.0
# Tue, 24 Feb 2026 20:14:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:14:43 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:14:43 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:14:43 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:14:43 GMT
USER fluent
# Tue, 24 Feb 2026 20:14:43 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:14:43 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc97e1b8827deb66c8f55b63aa24a717166c23c116bfd32fbd210f382acecdf`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 3.5 MB (3512925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17762cd40b5013880f2dc74d7021819b98739a6250505c6d6bad05beb0baba3`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57afe41774a91d5bf4827fd241077ca7fd3aa50bbe5c7d27d3487ee987de1380`  
		Last Modified: Tue, 24 Feb 2026 19:52:17 GMT  
		Size: 32.2 MB (32163465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e92ca4f16ad2c4f2c1e21f71b07ebc1a54c39ecf03d4123e2195457b6d7a4f5`  
		Last Modified: Tue, 24 Feb 2026 19:52:16 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7f26d050631b1598d9563e0ebc9413bba3819d6d8800733ed659015cee7c95`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 14.1 MB (14083462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab423f0cf0e00bb38746a54ac895cc370be34077dba1ebd5dac64fdd14eda`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccb2f2eba9b30c0067b2d308ca5a1430a1861e6fa16743fb3b8bb1198917c83`  
		Last Modified: Tue, 24 Feb 2026 20:14:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a12c5a6f6001ec1271796c5d8756d429f533928dd1339bc921c2ca0f8f2e767`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2ed16d2be1481d029c17cd7582c6d7d5216d4bd26615e300f655ddd8f00bfdee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6820d87dc396a6dfd3ad9d5335e7e95d50587dce35b25f781b48f1b3b430e4cc`

```dockerfile
```

-	Layers:
	-	`sha256:44c55ddf3bc8749a5defb8ecbf589437309c16ecebdc474d4195e0f604821ce0`  
		Last Modified: Tue, 24 Feb 2026 20:14:52 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95e74b71ed7da334df84404550da95607f6a249bd0c7be0718ed69c1a594bfbe`  
		Last Modified: Tue, 24 Feb 2026 20:14:51 GMT  
		Size: 21.0 KB (21048 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:816226b07b90f84016be1328a9f3507e26b6cb66578da92290bd1831340087c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84311789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4076c70acc476b7dcaace335f523a9cb665fe1bfecc55d2807f1966ecc5ccac`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 08:58:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 08:58:55 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 09:23:26 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 09:23:26 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 09:23:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 09:23:26 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 09:23:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 09:23:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 09:23:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 09:23:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:23:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 09:23:26 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 12:56:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 12:56:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 12:56:13 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 12:56:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 12:56:13 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 12:56:13 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 12:56:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 12:56:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 12:56:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 12:56:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 12:56:14 GMT
USER fluent
# Tue, 03 Feb 2026 12:56:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 12:56:14 GMT
CMD ["fluentd"]
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
	-	`sha256:7587171a4e629afb8dfff49f88e0e8350eb9c14f7193943860172be3bfb7a0b1`  
		Last Modified: Tue, 03 Feb 2026 09:23:47 GMT  
		Size: 33.8 MB (33835373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94869493584d5b727bcda6a2a93c575474b6f8179584ecadc24f1976353f7a3`  
		Last Modified: Tue, 03 Feb 2026 09:23:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d604f17bcaf377736a812a439aa41739027dffd88b28601cbc377131dc5a0f`  
		Last Modified: Tue, 03 Feb 2026 12:56:36 GMT  
		Size: 14.7 MB (14694522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198c70af543b0996c912f2776157aff7e21133ce11c579fe38572df44fc4b412`  
		Last Modified: Tue, 03 Feb 2026 12:56:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7858fa7f32b098adfe2abf4ad896a6095bfa8af1e2a8207bc4a9cd12309a221e`  
		Last Modified: Tue, 03 Feb 2026 12:56:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2be0185de3db75a1ebb6ad19140bb6543d12f82ff03cf77026fcc406fde83df`  
		Last Modified: Tue, 03 Feb 2026 12:56:36 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8f83b89eacdc68069c996c9785bb19a3e17e64e29ab41221dfd471950abde9db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b96dde2f57ea1b4ff5a69b724c753cfbf9777dbec8f226ec81b4b00f3bd7459`

```dockerfile
```

-	Layers:
	-	`sha256:36274d2419f74c4a6796c67f5c55f19de80b8111f0940e0dfa50250388c6913a`  
		Last Modified: Tue, 03 Feb 2026 12:56:36 GMT  
		Size: 2.7 MB (2674899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038e108fb3ab6172e65294742ead6b0632b2120f3a8c6e66f4603ef98528db9e`  
		Last Modified: Tue, 03 Feb 2026 12:56:35 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:a39bcfa77efc7af7c937a08d332b07eb6ffee006aaafb9cd9b2d3c79f432cc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77599356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9df9d9b17e23c2dac02ed0c379d82b513e8b55c9e1fbe660cf61cad7cda9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 22:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:56:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 23:07:32 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 24 Feb 2026 23:07:32 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 24 Feb 2026 23:07:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 23:07:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 23:07:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 23:07:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:07:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 23:07:33 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 02:39:21 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 02:39:21 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Wed, 25 Feb 2026 02:39:21 GMT
ENV TINI_VERSION=0.18.0
# Wed, 25 Feb 2026 02:39:21 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Wed, 25 Feb 2026 02:39:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 02:39:22 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 02:39:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 02:39:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 02:39:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 02:39:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 02:39:23 GMT
USER fluent
# Wed, 25 Feb 2026 02:39:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 02:39:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee0a8590e769ec84c9c999b84ef7c697884603dfeac17e2f74cb19194158987`  
		Last Modified: Tue, 24 Feb 2026 23:02:46 GMT  
		Size: 3.2 MB (3171209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba25f0557aafc3759d760486d757d65a9bb3e1c108c3458785dc2ff39fc676f`  
		Last Modified: Tue, 24 Feb 2026 23:02:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8f23b843a21ce3f239a4d6af280bf2729dc51d0ac0483462479fae094340c`  
		Last Modified: Tue, 24 Feb 2026 23:07:52 GMT  
		Size: 33.1 MB (33104236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf4ff6bfa8f17cec32e84126297cd2c142213d9e37f0d2ffd9e7795450567b1`  
		Last Modified: Tue, 24 Feb 2026 23:07:50 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be13b0e8917723a0af24cbc141920b530c9a24cbe9d72925549598334842e639`  
		Last Modified: Wed, 25 Feb 2026 02:39:43 GMT  
		Size: 14.4 MB (14429986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831b0786c75adf02326337327216b324d581bb04e65603b8fc1dbd4a43135884`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08315f43215c0225ec306a8a7c05a553aeb6b2d2284697ad375315c7700738c0`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84550c0ddc77f8b63a983e57aadb590d16013d0a2b85a5d3cbe7dc9c29ec81ca`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9df0560ccf9cc0eb9a0040a1553bbd954239feadbac3cade9b4300aa6cc969ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1e46b02eaf9f954b5ac4771b7efae352a149c78ea63c9a8cbbb716083e91da`

```dockerfile
```

-	Layers:
	-	`sha256:50f8c4edc2f854be02126e76fddc0f06a70ce49cd96b71d70cf1ce2855500131`  
		Last Modified: Wed, 25 Feb 2026 02:39:43 GMT  
		Size: 2.7 MB (2667307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18427afb6fd0aaec0ae12fd27cdd134735954f8ad9f215bec007f6742693b4f0`  
		Last Modified: Wed, 25 Feb 2026 02:39:42 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:aa9b6c04232a11144fa83bffa8902e2779edf94c8aff76d5bea42a8db5965c26
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
$ docker pull fluentd@sha256:86e84bbd6c545a47659b7ee6fad003f49a97de4b123d3a6d1fb68f5542d59435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79227327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a0780d380896e171f5bf348d0dc0e6c368155349908f1bf89d9baf2a1cad62`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:22:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:22:30 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 20:22:30 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 20:22:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:22:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:22:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:22:31 GMT
USER fluent
# Tue, 24 Feb 2026 20:22:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95c885d11163cea6141f2874f7609fd353fae57178c697f1a7d40224f7b00cc`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 1.3 MB (1279331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7f5fbc95c257016cbdb5dfe0a0139978a0a4a0d17362943647c993cd4bcb99`  
		Last Modified: Tue, 24 Feb 2026 19:49:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05f4e549e9c58aeab34c05f03badc598c63a0b59ae9c2fe69be781ab5544df`  
		Last Modified: Tue, 24 Feb 2026 19:49:39 GMT  
		Size: 42.1 MB (42112489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce46bb75e106e62f4498c163d02fd7018cc5ceaa37cf6b822414c2107df184`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f59026a1925dd53f562c18d3b963c4a30e709dc70ae319df12164c9ab8ff9`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 6.1 MB (6054480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada8589f55043b5e553c835963c974db9e9d8842e4333c7b6003ec903edef689`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a121bb92b77148244102bcd1a61443fc53ce646403d9b52c35aca9feea6e74`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baebd31418b4c9c62b6aab7926059fc5c79306c5d0580e654134017802fa6d6`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e35e8cd467bb2f2ba07e7351ce23dccbfe36f290bea9e917f8ad955d2bc47527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baec12c16182f271c21dba4a627dad83ea637f492e558a2def52c57372669c0`

```dockerfile
```

-	Layers:
	-	`sha256:87beb35f6ddcf4b58a92b15ae5b3c11e235b8de2461b91c3627e12496fa07f77`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 2.3 MB (2281482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f392ca696149469d3691c7ffdbffb55dba0a7cc874998211f69c4b033b7d24`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:702bb1b758b2b0b86544a326a57afe656f1da4018d2f2ac5e22a9596d9ea5dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73075764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52d7f1c907ee2f76702409fbfe17af5316afdb353b4746714b8f7394312884a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:54:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:54:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 21:54:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:54:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:54:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:54:58 GMT
USER fluent
# Tue, 24 Feb 2026 21:54:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:54:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc96269d7ff6661f7c783aa28ef266b6a3454b0b7270f35fd67c75efbb126325`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 1.3 MB (1262995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dde3052860b01def3c7729ab7e0b552cfc8471229c632727c524ba36ffa87c`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feb54b5087fc558951fafdb4a294dc5d0cfd9f91b23c76b4e5f03fb58403146`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 37.9 MB (37906244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd1652237e976a13ba3e6c119a312c9ef9b52d4d968f91702f2ed8dac11a6d`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8f4af827fa0ee9a1256892f1bbf83c4271c6a35814b9292176c3c078b13f5b`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 6.0 MB (5956521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fc31c05c8248f02920d77d8c9ba45d5403895207860b0ed4c01a5e2b6e86d6`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f480ee64da643f3dd1a9521699efb88c5788cc57f46d3c16546f8d1e0fd581a`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794edd3187fbf592f533456f685e8461ec4a4f97ab6d80e3f2777fc727af72f3`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:aeff6eb65638d187ee9dfc2632bd9a6fe5aa475c7732e02050a037648f7bd08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d7bc32560f9f9f482c4f0d1edf21542d17c45a3a16f10e6120f92b58bb2b61`

```dockerfile
```

-	Layers:
	-	`sha256:c5516e6bf9c46bc32b1d45a4de020a57104bea2b0d21a174426bc1b3b3e5a2aa`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 2.3 MB (2284453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61ab6a4efa546f12948f77ab6e386e9c29a6aa900ea73c9b8357b1bdb43c43e3`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:249cd06a9583c174022bc1662a638183730f2eb3cf11ad58645af47ac58d552d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70944650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a202282d8340e112924e8c4e6b6f741d47d8511e6d65071ccf02ee62a9164`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 21:09:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:09:12 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 22:00:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 22:00:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 22:00:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 22:00:49 GMT
USER fluent
# Tue, 24 Feb 2026 22:00:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 22:00:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14feba02466030de4233bb2b9b4ae7bb8d22598db9db35967cc9269952aa2190`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 1.2 MB (1236637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991f1e7bee0c079b1385009eded49ec5445b76573d3c6311e6d7a8472bbeebd`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f4b57fa9f91ef9277385833d43232d221aae42613777d8a1984c4d140abdf8`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 37.8 MB (37767330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865adf2d3ca7b76be7f98186142a67e87adc8e14da1a9c847d4838d387f91d2f`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6215cd02e856f3f916f009645d1930216f1ea5046f717331deb0b0c628c0cb1f`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 5.7 MB (5724546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbcfa781ef6a32d1924052e879b40cf20670dc5460b896852bb939d35097f6`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f810d4742ff15c72ffa1d88314e0af2232943762e952ba81264158f7c11a5e7`  
		Last Modified: Tue, 24 Feb 2026 22:00:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0491a7058409e826832ddd60b3500d0531fbf847813171676e8df47d10e7e60f`  
		Last Modified: Tue, 24 Feb 2026 22:01:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:616d833662b654cfdaefcd601933ef26a2c132b460c51932d43532a964e574aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141883a718ab52bba48c5df7dee9157f0bbb26b80a0830cac65470df72d406af`

```dockerfile
```

-	Layers:
	-	`sha256:3e6cabc9f406ac1d02f047192c16317f3ae30604e3c63cfd48324204afffb01d`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 2.3 MB (2282894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3db94822a243938772aec32d2ec10453a6f7b111f889e584043a103671ac7d69`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:828404f45a0b0a32fec514fa74e419ac06f5a23433cd5d604319cc175e82d054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79521874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d16ebbf1045c14f44b80173504653196573d47d64c6678c057ce7b6f3daa26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:38:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:38:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 21:38:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:38:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:38:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:38:23 GMT
USER fluent
# Tue, 24 Feb 2026 21:38:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f75b690a5fd55169fbad21a29d8ed315a9d4042c310b1bf6f573673b222fc`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 1.3 MB (1261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c26ba3937fd2b59db15d9b6d2d658d4dd4063b544cfdc5543f937af1ae20ee`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af054951d688ba98eecceef225934514c1bce049b94d72213bb07dbde8fb87`  
		Last Modified: Tue, 24 Feb 2026 20:01:00 GMT  
		Size: 42.1 MB (42074135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639b1a194a41b5d55ce4d7d2ec84ba51375ae840f4a37543134a924795e35a07`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a08ed296b9681998efe65e6e0547331e19e4c85d582e56ee946b40f75bc53e`  
		Last Modified: Tue, 24 Feb 2026 21:38:32 GMT  
		Size: 6.0 MB (6043953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51dce7afff466c28dbaf5e1b0183007860bc4d1b1ab4f805ff142df8b02efc`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c445911edf772b7b26b1a963f84eb02edbb6edf42beff8deb7d06eb236bf3`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205244818e9d9295806167b757eeccf4c11d403b60d31509b2934897f702154`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ca791e8bd0f179910fdb549ce401bc962cc8bb5ad45ced6d1882cef650ede648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78018d21a04e4f823186dd34a8c235892d68b619bbd54d8343306f0feb00f0f2`

```dockerfile
```

-	Layers:
	-	`sha256:23aa4569b3fa9dc8f92fd32abf7c895fd4d19a8e8aa44bbc2fa60dd79a77028f`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 2.3 MB (2281754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50619cb3792635e604919c80a6837451d9333523df0b41771df7d709c5f105ad`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 21.5 KB (21455 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:d4e441291fbcc948534053a6429efb66080283ffde02d2ff0ed8c733968d9de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985aeed61e2de83466ff38ae8525b6052c73fe6a2c5dbe6fafccf426c3526b10`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:51:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:45 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:14:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:14:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 20:14:50 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:14:50 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:14:50 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:14:50 GMT
USER fluent
# Tue, 24 Feb 2026 20:14:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:14:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a892ff57419277a7fa8ad912b1813f1159602bd6d8068badf5bfb1d62a14993f`  
		Last Modified: Tue, 24 Feb 2026 19:51:53 GMT  
		Size: 1.3 MB (1287332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbea3e8ba0db554c2fac0167ff3e4daf51f3fbd5bc330d7217898dd5c65f7d2`  
		Last Modified: Tue, 24 Feb 2026 19:51:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2d9cc1d12b4edaca10bae974eeb96048293aec72576d8c3e8254d4431ce48c`  
		Last Modified: Tue, 24 Feb 2026 19:51:54 GMT  
		Size: 37.7 MB (37661562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee811540cac1162511fd45e13f42fe19541d1f73c7d8a45b816037c2d0668a`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fb7539d7a3851caa96e2bcccbb66a68fcf4dac4973414f51370ae37c4622ea`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 6.0 MB (6025681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25798218224060dbc499d8986f06d2eb074d58bf9345da4f05f6ed75f35fbc62`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed273dda7a96de12238121a09a97770b30f1889adddd7a0d5ffadceba370b6b`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0aa78822ed9aa54b3dfb41392b36b646e4f9bc15bb3037b819fad46d8f4fcf`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a8ce02d3271a6c38e6ac9845cc16d1c54480c4d0b2d183fb82b7d091b9387294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b96e28b5c2f4a99203e65e38ac879bef38fbdb184706b87fc865ed232d9ee3`

```dockerfile
```

-	Layers:
	-	`sha256:a48b838e0998fb5c2903ba45219be4a3b3db2a074344147cbfcb58b4d84339bb`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 2.3 MB (2278670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587f45001b4aef0def6ce0691f65c51db7c9f957fe89daf5806210568c13de31`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:3e85b7afdefefc0ceed38702aa8c6e83e6d900b88a7bba22e2988cc09521c314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81007295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92db795cc55a308b287141133fb2ebb98c3099b9cf82951c8aff9c3aaa3d8a3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:04:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 09:04:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
CMD ["irb"]
# Fri, 13 Feb 2026 18:50:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 13 Feb 2026 18:50:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Fri, 13 Feb 2026 18:50:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 13 Feb 2026 18:50:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 13 Feb 2026 18:51:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 13 Feb 2026 18:51:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 13 Feb 2026 18:51:00 GMT
USER fluent
# Fri, 13 Feb 2026 18:51:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 13 Feb 2026 18:51:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6be1f9ad8d9708d6d1dd902519422f937c816172bb2279df8827177290ce2c7`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 1.3 MB (1309384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69016493cd4b81c51b0ebe7726a06117b8c667e58289628f10d4662f959eb918`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae5d6a287ac9deb00e76ee4f5bc8133dfa2ad449e09b28cbcef3715fe45f124`  
		Last Modified: Tue, 03 Feb 2026 09:09:01 GMT  
		Size: 39.5 MB (39519472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9277fefce554077ed90bf6814e28a9db303a96069b78e13ebbb958a92daa6d2d`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb39087a75c520eecf6fa1d6cca6b087321ba9c79cb338599d9739d4491b11`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 6.6 MB (6575848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19afb70fa211158dd4f6a97285e69a623a026dc5cbeb9c946cc0d9597470585`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff208f82e22958984a23e4b02712a779bdb4570c8422c467e124a8b264b0bb43`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9649c1f8ea25246f0060ad4dff7af4b5afe7280fec821c3bb316ce49cd25e607`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:372534f2d3f54414e8b10d874b438910a672bfe189b65a56796669b17fba2c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3279a02c907e4d5bf163f52ce92ba2acd37a5dc3693c358ad599f1dae6dc53`

```dockerfile
```

-	Layers:
	-	`sha256:772508226cfbbcde2d89894fbb9d6bfa67f21f85f9c7820774e4c4024df3c785`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 2.3 MB (2285017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f660251e609f7c92dcf6085728502cdc3bdec0fc40fde1ae3dcbe42b7e15d262`  
		Last Modified: Fri, 13 Feb 2026 18:51:19 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; s390x

```console
$ docker pull fluentd@sha256:325c4ac442f736c13b434e56b7fde81681f7b089bb9a88139c4c8089520b06dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76758781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4123c819169f7a1c43c68cdbf71bc0fce9aeea2a49950405f4f3c7953a3d6d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:02:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 25 Feb 2026 01:32:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:32:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 01:32:11 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 02:39:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 02:39:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 25 Feb 2026 02:39:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 25 Feb 2026 02:39:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 02:39:37 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 02:39:37 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 02:39:37 GMT
USER fluent
# Wed, 25 Feb 2026 02:39:37 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 02:39:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4914443d3c4184b2c3ca5f7f265c77f7783c5fe40f5ff77daa520ded4b0a2c`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 1.3 MB (1294517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def914eff926e8e33e8d2ea6891e3ece82a54502d942da1cf995fac0cf626932`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fad6ee4d8be5d7dbfd8551d2a5d070571e5d13c57cfc9d2618d596970e34c`  
		Last Modified: Wed, 25 Feb 2026 01:32:41 GMT  
		Size: 39.2 MB (39192544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb56a57c12ad1160bc0ee7c91d149dab3f7a2a858afd9771d4f967a14a4533a`  
		Last Modified: Wed, 25 Feb 2026 01:32:39 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d528a35268e8e46fa75fdda5d210e6dbbb535b26387f024349e2351e5455edfd`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 6.4 MB (6431145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4914220566b082bf5096917093d86a2f05c15edd3bf91a0aebf285700aef707f`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a611c57f9809a0ad97f6a54adfb486209c5531824142c8a9f79fe2238b7953`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c41433679913e9f12adb749646999e0194b8012806661df0a3a786f5e6deea9`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:45ce6eafa5ff53cc997cf7bf28d3a7cd68637982865c75eaa2b9962145a945ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b56380c11cf0412a468c8aa4e2a1884f4b5ea388938a8fb40abafee4a64259`

```dockerfile
```

-	Layers:
	-	`sha256:fa1aca00461b819cd8ecd3a4ffe90129f1108cb248f3958784a2f61d22396899`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 2.3 MB (2282927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ad2111eaf7ad708910e559db08048a2777e2fa6a210307b46f77f9c393b797`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:aa9b6c04232a11144fa83bffa8902e2779edf94c8aff76d5bea42a8db5965c26
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
$ docker pull fluentd@sha256:86e84bbd6c545a47659b7ee6fad003f49a97de4b123d3a6d1fb68f5542d59435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79227327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a0780d380896e171f5bf348d0dc0e6c368155349908f1bf89d9baf2a1cad62`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:22:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:22:30 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 20:22:30 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 20:22:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:22:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:22:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:22:31 GMT
USER fluent
# Tue, 24 Feb 2026 20:22:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95c885d11163cea6141f2874f7609fd353fae57178c697f1a7d40224f7b00cc`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 1.3 MB (1279331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7f5fbc95c257016cbdb5dfe0a0139978a0a4a0d17362943647c993cd4bcb99`  
		Last Modified: Tue, 24 Feb 2026 19:49:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05f4e549e9c58aeab34c05f03badc598c63a0b59ae9c2fe69be781ab5544df`  
		Last Modified: Tue, 24 Feb 2026 19:49:39 GMT  
		Size: 42.1 MB (42112489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce46bb75e106e62f4498c163d02fd7018cc5ceaa37cf6b822414c2107df184`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f59026a1925dd53f562c18d3b963c4a30e709dc70ae319df12164c9ab8ff9`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 6.1 MB (6054480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada8589f55043b5e553c835963c974db9e9d8842e4333c7b6003ec903edef689`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a121bb92b77148244102bcd1a61443fc53ce646403d9b52c35aca9feea6e74`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baebd31418b4c9c62b6aab7926059fc5c79306c5d0580e654134017802fa6d6`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e35e8cd467bb2f2ba07e7351ce23dccbfe36f290bea9e917f8ad955d2bc47527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baec12c16182f271c21dba4a627dad83ea637f492e558a2def52c57372669c0`

```dockerfile
```

-	Layers:
	-	`sha256:87beb35f6ddcf4b58a92b15ae5b3c11e235b8de2461b91c3627e12496fa07f77`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 2.3 MB (2281482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f392ca696149469d3691c7ffdbffb55dba0a7cc874998211f69c4b033b7d24`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:702bb1b758b2b0b86544a326a57afe656f1da4018d2f2ac5e22a9596d9ea5dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73075764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52d7f1c907ee2f76702409fbfe17af5316afdb353b4746714b8f7394312884a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:54:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:54:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 21:54:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:54:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:54:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:54:58 GMT
USER fluent
# Tue, 24 Feb 2026 21:54:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:54:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc96269d7ff6661f7c783aa28ef266b6a3454b0b7270f35fd67c75efbb126325`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 1.3 MB (1262995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dde3052860b01def3c7729ab7e0b552cfc8471229c632727c524ba36ffa87c`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feb54b5087fc558951fafdb4a294dc5d0cfd9f91b23c76b4e5f03fb58403146`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 37.9 MB (37906244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd1652237e976a13ba3e6c119a312c9ef9b52d4d968f91702f2ed8dac11a6d`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8f4af827fa0ee9a1256892f1bbf83c4271c6a35814b9292176c3c078b13f5b`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 6.0 MB (5956521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fc31c05c8248f02920d77d8c9ba45d5403895207860b0ed4c01a5e2b6e86d6`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f480ee64da643f3dd1a9521699efb88c5788cc57f46d3c16546f8d1e0fd581a`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794edd3187fbf592f533456f685e8461ec4a4f97ab6d80e3f2777fc727af72f3`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:aeff6eb65638d187ee9dfc2632bd9a6fe5aa475c7732e02050a037648f7bd08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d7bc32560f9f9f482c4f0d1edf21542d17c45a3a16f10e6120f92b58bb2b61`

```dockerfile
```

-	Layers:
	-	`sha256:c5516e6bf9c46bc32b1d45a4de020a57104bea2b0d21a174426bc1b3b3e5a2aa`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 2.3 MB (2284453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61ab6a4efa546f12948f77ab6e386e9c29a6aa900ea73c9b8357b1bdb43c43e3`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:249cd06a9583c174022bc1662a638183730f2eb3cf11ad58645af47ac58d552d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70944650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a202282d8340e112924e8c4e6b6f741d47d8511e6d65071ccf02ee62a9164`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 21:09:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:09:12 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 22:00:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 22:00:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 22:00:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 22:00:49 GMT
USER fluent
# Tue, 24 Feb 2026 22:00:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 22:00:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14feba02466030de4233bb2b9b4ae7bb8d22598db9db35967cc9269952aa2190`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 1.2 MB (1236637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991f1e7bee0c079b1385009eded49ec5445b76573d3c6311e6d7a8472bbeebd`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f4b57fa9f91ef9277385833d43232d221aae42613777d8a1984c4d140abdf8`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 37.8 MB (37767330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865adf2d3ca7b76be7f98186142a67e87adc8e14da1a9c847d4838d387f91d2f`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6215cd02e856f3f916f009645d1930216f1ea5046f717331deb0b0c628c0cb1f`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 5.7 MB (5724546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbcfa781ef6a32d1924052e879b40cf20670dc5460b896852bb939d35097f6`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f810d4742ff15c72ffa1d88314e0af2232943762e952ba81264158f7c11a5e7`  
		Last Modified: Tue, 24 Feb 2026 22:00:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0491a7058409e826832ddd60b3500d0531fbf847813171676e8df47d10e7e60f`  
		Last Modified: Tue, 24 Feb 2026 22:01:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:616d833662b654cfdaefcd601933ef26a2c132b460c51932d43532a964e574aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141883a718ab52bba48c5df7dee9157f0bbb26b80a0830cac65470df72d406af`

```dockerfile
```

-	Layers:
	-	`sha256:3e6cabc9f406ac1d02f047192c16317f3ae30604e3c63cfd48324204afffb01d`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 2.3 MB (2282894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3db94822a243938772aec32d2ec10453a6f7b111f889e584043a103671ac7d69`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:828404f45a0b0a32fec514fa74e419ac06f5a23433cd5d604319cc175e82d054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79521874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d16ebbf1045c14f44b80173504653196573d47d64c6678c057ce7b6f3daa26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:38:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:38:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 21:38:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:38:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:38:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:38:23 GMT
USER fluent
# Tue, 24 Feb 2026 21:38:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f75b690a5fd55169fbad21a29d8ed315a9d4042c310b1bf6f573673b222fc`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 1.3 MB (1261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c26ba3937fd2b59db15d9b6d2d658d4dd4063b544cfdc5543f937af1ae20ee`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af054951d688ba98eecceef225934514c1bce049b94d72213bb07dbde8fb87`  
		Last Modified: Tue, 24 Feb 2026 20:01:00 GMT  
		Size: 42.1 MB (42074135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639b1a194a41b5d55ce4d7d2ec84ba51375ae840f4a37543134a924795e35a07`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a08ed296b9681998efe65e6e0547331e19e4c85d582e56ee946b40f75bc53e`  
		Last Modified: Tue, 24 Feb 2026 21:38:32 GMT  
		Size: 6.0 MB (6043953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51dce7afff466c28dbaf5e1b0183007860bc4d1b1ab4f805ff142df8b02efc`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c445911edf772b7b26b1a963f84eb02edbb6edf42beff8deb7d06eb236bf3`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205244818e9d9295806167b757eeccf4c11d403b60d31509b2934897f702154`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ca791e8bd0f179910fdb549ce401bc962cc8bb5ad45ced6d1882cef650ede648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78018d21a04e4f823186dd34a8c235892d68b619bbd54d8343306f0feb00f0f2`

```dockerfile
```

-	Layers:
	-	`sha256:23aa4569b3fa9dc8f92fd32abf7c895fd4d19a8e8aa44bbc2fa60dd79a77028f`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 2.3 MB (2281754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50619cb3792635e604919c80a6837451d9333523df0b41771df7d709c5f105ad`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 21.5 KB (21455 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:d4e441291fbcc948534053a6429efb66080283ffde02d2ff0ed8c733968d9de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985aeed61e2de83466ff38ae8525b6052c73fe6a2c5dbe6fafccf426c3526b10`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:51:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:45 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:14:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:14:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 20:14:50 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:14:50 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:14:50 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:14:50 GMT
USER fluent
# Tue, 24 Feb 2026 20:14:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:14:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a892ff57419277a7fa8ad912b1813f1159602bd6d8068badf5bfb1d62a14993f`  
		Last Modified: Tue, 24 Feb 2026 19:51:53 GMT  
		Size: 1.3 MB (1287332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbea3e8ba0db554c2fac0167ff3e4daf51f3fbd5bc330d7217898dd5c65f7d2`  
		Last Modified: Tue, 24 Feb 2026 19:51:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2d9cc1d12b4edaca10bae974eeb96048293aec72576d8c3e8254d4431ce48c`  
		Last Modified: Tue, 24 Feb 2026 19:51:54 GMT  
		Size: 37.7 MB (37661562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee811540cac1162511fd45e13f42fe19541d1f73c7d8a45b816037c2d0668a`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fb7539d7a3851caa96e2bcccbb66a68fcf4dac4973414f51370ae37c4622ea`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 6.0 MB (6025681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25798218224060dbc499d8986f06d2eb074d58bf9345da4f05f6ed75f35fbc62`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed273dda7a96de12238121a09a97770b30f1889adddd7a0d5ffadceba370b6b`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0aa78822ed9aa54b3dfb41392b36b646e4f9bc15bb3037b819fad46d8f4fcf`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a8ce02d3271a6c38e6ac9845cc16d1c54480c4d0b2d183fb82b7d091b9387294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b96e28b5c2f4a99203e65e38ac879bef38fbdb184706b87fc865ed232d9ee3`

```dockerfile
```

-	Layers:
	-	`sha256:a48b838e0998fb5c2903ba45219be4a3b3db2a074344147cbfcb58b4d84339bb`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 2.3 MB (2278670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587f45001b4aef0def6ce0691f65c51db7c9f957fe89daf5806210568c13de31`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:3e85b7afdefefc0ceed38702aa8c6e83e6d900b88a7bba22e2988cc09521c314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81007295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92db795cc55a308b287141133fb2ebb98c3099b9cf82951c8aff9c3aaa3d8a3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:04:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 09:04:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
CMD ["irb"]
# Fri, 13 Feb 2026 18:50:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 13 Feb 2026 18:50:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Fri, 13 Feb 2026 18:50:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 13 Feb 2026 18:50:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 13 Feb 2026 18:51:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 13 Feb 2026 18:51:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 13 Feb 2026 18:51:00 GMT
USER fluent
# Fri, 13 Feb 2026 18:51:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 13 Feb 2026 18:51:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6be1f9ad8d9708d6d1dd902519422f937c816172bb2279df8827177290ce2c7`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 1.3 MB (1309384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69016493cd4b81c51b0ebe7726a06117b8c667e58289628f10d4662f959eb918`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae5d6a287ac9deb00e76ee4f5bc8133dfa2ad449e09b28cbcef3715fe45f124`  
		Last Modified: Tue, 03 Feb 2026 09:09:01 GMT  
		Size: 39.5 MB (39519472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9277fefce554077ed90bf6814e28a9db303a96069b78e13ebbb958a92daa6d2d`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb39087a75c520eecf6fa1d6cca6b087321ba9c79cb338599d9739d4491b11`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 6.6 MB (6575848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19afb70fa211158dd4f6a97285e69a623a026dc5cbeb9c946cc0d9597470585`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff208f82e22958984a23e4b02712a779bdb4570c8422c467e124a8b264b0bb43`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9649c1f8ea25246f0060ad4dff7af4b5afe7280fec821c3bb316ce49cd25e607`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:372534f2d3f54414e8b10d874b438910a672bfe189b65a56796669b17fba2c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3279a02c907e4d5bf163f52ce92ba2acd37a5dc3693c358ad599f1dae6dc53`

```dockerfile
```

-	Layers:
	-	`sha256:772508226cfbbcde2d89894fbb9d6bfa67f21f85f9c7820774e4c4024df3c785`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 2.3 MB (2285017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f660251e609f7c92dcf6085728502cdc3bdec0fc40fde1ae3dcbe42b7e15d262`  
		Last Modified: Fri, 13 Feb 2026 18:51:19 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:325c4ac442f736c13b434e56b7fde81681f7b089bb9a88139c4c8089520b06dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76758781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4123c819169f7a1c43c68cdbf71bc0fce9aeea2a49950405f4f3c7953a3d6d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:02:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 25 Feb 2026 01:32:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:32:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 01:32:11 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 02:39:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 02:39:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 25 Feb 2026 02:39:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 25 Feb 2026 02:39:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 02:39:37 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 02:39:37 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 02:39:37 GMT
USER fluent
# Wed, 25 Feb 2026 02:39:37 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 02:39:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4914443d3c4184b2c3ca5f7f265c77f7783c5fe40f5ff77daa520ded4b0a2c`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 1.3 MB (1294517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def914eff926e8e33e8d2ea6891e3ece82a54502d942da1cf995fac0cf626932`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fad6ee4d8be5d7dbfd8551d2a5d070571e5d13c57cfc9d2618d596970e34c`  
		Last Modified: Wed, 25 Feb 2026 01:32:41 GMT  
		Size: 39.2 MB (39192544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb56a57c12ad1160bc0ee7c91d149dab3f7a2a858afd9771d4f967a14a4533a`  
		Last Modified: Wed, 25 Feb 2026 01:32:39 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d528a35268e8e46fa75fdda5d210e6dbbb535b26387f024349e2351e5455edfd`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 6.4 MB (6431145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4914220566b082bf5096917093d86a2f05c15edd3bf91a0aebf285700aef707f`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a611c57f9809a0ad97f6a54adfb486209c5531824142c8a9f79fe2238b7953`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c41433679913e9f12adb749646999e0194b8012806661df0a3a786f5e6deea9`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:45ce6eafa5ff53cc997cf7bf28d3a7cd68637982865c75eaa2b9962145a945ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b56380c11cf0412a468c8aa4e2a1884f4b5ea388938a8fb40abafee4a64259`

```dockerfile
```

-	Layers:
	-	`sha256:fa1aca00461b819cd8ecd3a4ffe90129f1108cb248f3958784a2f61d22396899`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 2.3 MB (2282927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ad2111eaf7ad708910e559db08048a2777e2fa6a210307b46f77f9c393b797`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-1.0`

```console
$ docker pull fluentd@sha256:aa9b6c04232a11144fa83bffa8902e2779edf94c8aff76d5bea42a8db5965c26
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

### `fluentd:v1.19.2-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:86e84bbd6c545a47659b7ee6fad003f49a97de4b123d3a6d1fb68f5542d59435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79227327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a0780d380896e171f5bf348d0dc0e6c368155349908f1bf89d9baf2a1cad62`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:22:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:22:30 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 20:22:30 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 20:22:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:22:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:22:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:22:31 GMT
USER fluent
# Tue, 24 Feb 2026 20:22:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95c885d11163cea6141f2874f7609fd353fae57178c697f1a7d40224f7b00cc`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 1.3 MB (1279331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7f5fbc95c257016cbdb5dfe0a0139978a0a4a0d17362943647c993cd4bcb99`  
		Last Modified: Tue, 24 Feb 2026 19:49:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05f4e549e9c58aeab34c05f03badc598c63a0b59ae9c2fe69be781ab5544df`  
		Last Modified: Tue, 24 Feb 2026 19:49:39 GMT  
		Size: 42.1 MB (42112489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce46bb75e106e62f4498c163d02fd7018cc5ceaa37cf6b822414c2107df184`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f59026a1925dd53f562c18d3b963c4a30e709dc70ae319df12164c9ab8ff9`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 6.1 MB (6054480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada8589f55043b5e553c835963c974db9e9d8842e4333c7b6003ec903edef689`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a121bb92b77148244102bcd1a61443fc53ce646403d9b52c35aca9feea6e74`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baebd31418b4c9c62b6aab7926059fc5c79306c5d0580e654134017802fa6d6`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e35e8cd467bb2f2ba07e7351ce23dccbfe36f290bea9e917f8ad955d2bc47527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baec12c16182f271c21dba4a627dad83ea637f492e558a2def52c57372669c0`

```dockerfile
```

-	Layers:
	-	`sha256:87beb35f6ddcf4b58a92b15ae5b3c11e235b8de2461b91c3627e12496fa07f77`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 2.3 MB (2281482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f392ca696149469d3691c7ffdbffb55dba0a7cc874998211f69c4b033b7d24`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:702bb1b758b2b0b86544a326a57afe656f1da4018d2f2ac5e22a9596d9ea5dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73075764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52d7f1c907ee2f76702409fbfe17af5316afdb353b4746714b8f7394312884a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:54:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:54:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 21:54:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:54:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:54:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:54:58 GMT
USER fluent
# Tue, 24 Feb 2026 21:54:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:54:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc96269d7ff6661f7c783aa28ef266b6a3454b0b7270f35fd67c75efbb126325`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 1.3 MB (1262995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dde3052860b01def3c7729ab7e0b552cfc8471229c632727c524ba36ffa87c`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feb54b5087fc558951fafdb4a294dc5d0cfd9f91b23c76b4e5f03fb58403146`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 37.9 MB (37906244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd1652237e976a13ba3e6c119a312c9ef9b52d4d968f91702f2ed8dac11a6d`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8f4af827fa0ee9a1256892f1bbf83c4271c6a35814b9292176c3c078b13f5b`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 6.0 MB (5956521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fc31c05c8248f02920d77d8c9ba45d5403895207860b0ed4c01a5e2b6e86d6`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f480ee64da643f3dd1a9521699efb88c5788cc57f46d3c16546f8d1e0fd581a`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794edd3187fbf592f533456f685e8461ec4a4f97ab6d80e3f2777fc727af72f3`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:aeff6eb65638d187ee9dfc2632bd9a6fe5aa475c7732e02050a037648f7bd08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d7bc32560f9f9f482c4f0d1edf21542d17c45a3a16f10e6120f92b58bb2b61`

```dockerfile
```

-	Layers:
	-	`sha256:c5516e6bf9c46bc32b1d45a4de020a57104bea2b0d21a174426bc1b3b3e5a2aa`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 2.3 MB (2284453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61ab6a4efa546f12948f77ab6e386e9c29a6aa900ea73c9b8357b1bdb43c43e3`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:249cd06a9583c174022bc1662a638183730f2eb3cf11ad58645af47ac58d552d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70944650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a202282d8340e112924e8c4e6b6f741d47d8511e6d65071ccf02ee62a9164`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 21:09:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:09:12 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 22:00:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 22:00:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 22:00:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 22:00:49 GMT
USER fluent
# Tue, 24 Feb 2026 22:00:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 22:00:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14feba02466030de4233bb2b9b4ae7bb8d22598db9db35967cc9269952aa2190`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 1.2 MB (1236637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991f1e7bee0c079b1385009eded49ec5445b76573d3c6311e6d7a8472bbeebd`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f4b57fa9f91ef9277385833d43232d221aae42613777d8a1984c4d140abdf8`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 37.8 MB (37767330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865adf2d3ca7b76be7f98186142a67e87adc8e14da1a9c847d4838d387f91d2f`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6215cd02e856f3f916f009645d1930216f1ea5046f717331deb0b0c628c0cb1f`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 5.7 MB (5724546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbcfa781ef6a32d1924052e879b40cf20670dc5460b896852bb939d35097f6`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f810d4742ff15c72ffa1d88314e0af2232943762e952ba81264158f7c11a5e7`  
		Last Modified: Tue, 24 Feb 2026 22:00:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0491a7058409e826832ddd60b3500d0531fbf847813171676e8df47d10e7e60f`  
		Last Modified: Tue, 24 Feb 2026 22:01:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:616d833662b654cfdaefcd601933ef26a2c132b460c51932d43532a964e574aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141883a718ab52bba48c5df7dee9157f0bbb26b80a0830cac65470df72d406af`

```dockerfile
```

-	Layers:
	-	`sha256:3e6cabc9f406ac1d02f047192c16317f3ae30604e3c63cfd48324204afffb01d`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 2.3 MB (2282894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3db94822a243938772aec32d2ec10453a6f7b111f889e584043a103671ac7d69`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:828404f45a0b0a32fec514fa74e419ac06f5a23433cd5d604319cc175e82d054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79521874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d16ebbf1045c14f44b80173504653196573d47d64c6678c057ce7b6f3daa26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:38:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:38:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 21:38:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:38:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:38:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:38:23 GMT
USER fluent
# Tue, 24 Feb 2026 21:38:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f75b690a5fd55169fbad21a29d8ed315a9d4042c310b1bf6f573673b222fc`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 1.3 MB (1261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c26ba3937fd2b59db15d9b6d2d658d4dd4063b544cfdc5543f937af1ae20ee`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af054951d688ba98eecceef225934514c1bce049b94d72213bb07dbde8fb87`  
		Last Modified: Tue, 24 Feb 2026 20:01:00 GMT  
		Size: 42.1 MB (42074135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639b1a194a41b5d55ce4d7d2ec84ba51375ae840f4a37543134a924795e35a07`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a08ed296b9681998efe65e6e0547331e19e4c85d582e56ee946b40f75bc53e`  
		Last Modified: Tue, 24 Feb 2026 21:38:32 GMT  
		Size: 6.0 MB (6043953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51dce7afff466c28dbaf5e1b0183007860bc4d1b1ab4f805ff142df8b02efc`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c445911edf772b7b26b1a963f84eb02edbb6edf42beff8deb7d06eb236bf3`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205244818e9d9295806167b757eeccf4c11d403b60d31509b2934897f702154`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ca791e8bd0f179910fdb549ce401bc962cc8bb5ad45ced6d1882cef650ede648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78018d21a04e4f823186dd34a8c235892d68b619bbd54d8343306f0feb00f0f2`

```dockerfile
```

-	Layers:
	-	`sha256:23aa4569b3fa9dc8f92fd32abf7c895fd4d19a8e8aa44bbc2fa60dd79a77028f`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 2.3 MB (2281754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50619cb3792635e604919c80a6837451d9333523df0b41771df7d709c5f105ad`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 21.5 KB (21455 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:d4e441291fbcc948534053a6429efb66080283ffde02d2ff0ed8c733968d9de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985aeed61e2de83466ff38ae8525b6052c73fe6a2c5dbe6fafccf426c3526b10`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:51:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:45 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:14:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:14:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 20:14:50 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:14:50 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:14:50 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:14:50 GMT
USER fluent
# Tue, 24 Feb 2026 20:14:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:14:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a892ff57419277a7fa8ad912b1813f1159602bd6d8068badf5bfb1d62a14993f`  
		Last Modified: Tue, 24 Feb 2026 19:51:53 GMT  
		Size: 1.3 MB (1287332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbea3e8ba0db554c2fac0167ff3e4daf51f3fbd5bc330d7217898dd5c65f7d2`  
		Last Modified: Tue, 24 Feb 2026 19:51:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2d9cc1d12b4edaca10bae974eeb96048293aec72576d8c3e8254d4431ce48c`  
		Last Modified: Tue, 24 Feb 2026 19:51:54 GMT  
		Size: 37.7 MB (37661562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee811540cac1162511fd45e13f42fe19541d1f73c7d8a45b816037c2d0668a`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fb7539d7a3851caa96e2bcccbb66a68fcf4dac4973414f51370ae37c4622ea`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 6.0 MB (6025681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25798218224060dbc499d8986f06d2eb074d58bf9345da4f05f6ed75f35fbc62`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed273dda7a96de12238121a09a97770b30f1889adddd7a0d5ffadceba370b6b`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0aa78822ed9aa54b3dfb41392b36b646e4f9bc15bb3037b819fad46d8f4fcf`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a8ce02d3271a6c38e6ac9845cc16d1c54480c4d0b2d183fb82b7d091b9387294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b96e28b5c2f4a99203e65e38ac879bef38fbdb184706b87fc865ed232d9ee3`

```dockerfile
```

-	Layers:
	-	`sha256:a48b838e0998fb5c2903ba45219be4a3b3db2a074344147cbfcb58b4d84339bb`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 2.3 MB (2278670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587f45001b4aef0def6ce0691f65c51db7c9f957fe89daf5806210568c13de31`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:3e85b7afdefefc0ceed38702aa8c6e83e6d900b88a7bba22e2988cc09521c314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81007295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92db795cc55a308b287141133fb2ebb98c3099b9cf82951c8aff9c3aaa3d8a3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:04:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 09:04:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
CMD ["irb"]
# Fri, 13 Feb 2026 18:50:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 13 Feb 2026 18:50:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Fri, 13 Feb 2026 18:50:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 13 Feb 2026 18:50:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 13 Feb 2026 18:51:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 13 Feb 2026 18:51:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 13 Feb 2026 18:51:00 GMT
USER fluent
# Fri, 13 Feb 2026 18:51:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 13 Feb 2026 18:51:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6be1f9ad8d9708d6d1dd902519422f937c816172bb2279df8827177290ce2c7`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 1.3 MB (1309384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69016493cd4b81c51b0ebe7726a06117b8c667e58289628f10d4662f959eb918`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae5d6a287ac9deb00e76ee4f5bc8133dfa2ad449e09b28cbcef3715fe45f124`  
		Last Modified: Tue, 03 Feb 2026 09:09:01 GMT  
		Size: 39.5 MB (39519472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9277fefce554077ed90bf6814e28a9db303a96069b78e13ebbb958a92daa6d2d`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb39087a75c520eecf6fa1d6cca6b087321ba9c79cb338599d9739d4491b11`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 6.6 MB (6575848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19afb70fa211158dd4f6a97285e69a623a026dc5cbeb9c946cc0d9597470585`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff208f82e22958984a23e4b02712a779bdb4570c8422c467e124a8b264b0bb43`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9649c1f8ea25246f0060ad4dff7af4b5afe7280fec821c3bb316ce49cd25e607`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:372534f2d3f54414e8b10d874b438910a672bfe189b65a56796669b17fba2c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3279a02c907e4d5bf163f52ce92ba2acd37a5dc3693c358ad599f1dae6dc53`

```dockerfile
```

-	Layers:
	-	`sha256:772508226cfbbcde2d89894fbb9d6bfa67f21f85f9c7820774e4c4024df3c785`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 2.3 MB (2285017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f660251e609f7c92dcf6085728502cdc3bdec0fc40fde1ae3dcbe42b7e15d262`  
		Last Modified: Fri, 13 Feb 2026 18:51:19 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:325c4ac442f736c13b434e56b7fde81681f7b089bb9a88139c4c8089520b06dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76758781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4123c819169f7a1c43c68cdbf71bc0fce9aeea2a49950405f4f3c7953a3d6d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:02:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 25 Feb 2026 01:32:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:32:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 01:32:11 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 02:39:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 02:39:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 25 Feb 2026 02:39:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 25 Feb 2026 02:39:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 02:39:37 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 02:39:37 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 02:39:37 GMT
USER fluent
# Wed, 25 Feb 2026 02:39:37 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 02:39:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4914443d3c4184b2c3ca5f7f265c77f7783c5fe40f5ff77daa520ded4b0a2c`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 1.3 MB (1294517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def914eff926e8e33e8d2ea6891e3ece82a54502d942da1cf995fac0cf626932`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fad6ee4d8be5d7dbfd8551d2a5d070571e5d13c57cfc9d2618d596970e34c`  
		Last Modified: Wed, 25 Feb 2026 01:32:41 GMT  
		Size: 39.2 MB (39192544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb56a57c12ad1160bc0ee7c91d149dab3f7a2a858afd9771d4f967a14a4533a`  
		Last Modified: Wed, 25 Feb 2026 01:32:39 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d528a35268e8e46fa75fdda5d210e6dbbb535b26387f024349e2351e5455edfd`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 6.4 MB (6431145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4914220566b082bf5096917093d86a2f05c15edd3bf91a0aebf285700aef707f`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a611c57f9809a0ad97f6a54adfb486209c5531824142c8a9f79fe2238b7953`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c41433679913e9f12adb749646999e0194b8012806661df0a3a786f5e6deea9`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:45ce6eafa5ff53cc997cf7bf28d3a7cd68637982865c75eaa2b9962145a945ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b56380c11cf0412a468c8aa4e2a1884f4b5ea388938a8fb40abafee4a64259`

```dockerfile
```

-	Layers:
	-	`sha256:fa1aca00461b819cd8ecd3a4ffe90129f1108cb248f3958784a2f61d22396899`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 2.3 MB (2282927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ad2111eaf7ad708910e559db08048a2777e2fa6a210307b46f77f9c393b797`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-debian-1.0`

```console
$ docker pull fluentd@sha256:aa9b6c04232a11144fa83bffa8902e2779edf94c8aff76d5bea42a8db5965c26
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

### `fluentd:v1.19.2-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:86e84bbd6c545a47659b7ee6fad003f49a97de4b123d3a6d1fb68f5542d59435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79227327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a0780d380896e171f5bf348d0dc0e6c368155349908f1bf89d9baf2a1cad62`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:47:10 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:49:28 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:49:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:49:28 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:49:28 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:22:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:22:30 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 20:22:30 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 20:22:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:22:31 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:22:31 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:22:31 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:22:31 GMT
USER fluent
# Tue, 24 Feb 2026 20:22:31 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:22:31 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95c885d11163cea6141f2874f7609fd353fae57178c697f1a7d40224f7b00cc`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 1.3 MB (1279331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7f5fbc95c257016cbdb5dfe0a0139978a0a4a0d17362943647c993cd4bcb99`  
		Last Modified: Tue, 24 Feb 2026 19:49:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a05f4e549e9c58aeab34c05f03badc598c63a0b59ae9c2fe69be781ab5544df`  
		Last Modified: Tue, 24 Feb 2026 19:49:39 GMT  
		Size: 42.1 MB (42112489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce46bb75e106e62f4498c163d02fd7018cc5ceaa37cf6b822414c2107df184`  
		Last Modified: Tue, 24 Feb 2026 19:49:38 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f59026a1925dd53f562c18d3b963c4a30e709dc70ae319df12164c9ab8ff9`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 6.1 MB (6054480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada8589f55043b5e553c835963c974db9e9d8842e4333c7b6003ec903edef689`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a121bb92b77148244102bcd1a61443fc53ce646403d9b52c35aca9feea6e74`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5baebd31418b4c9c62b6aab7926059fc5c79306c5d0580e654134017802fa6d6`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e35e8cd467bb2f2ba07e7351ce23dccbfe36f290bea9e917f8ad955d2bc47527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baec12c16182f271c21dba4a627dad83ea637f492e558a2def52c57372669c0`

```dockerfile
```

-	Layers:
	-	`sha256:87beb35f6ddcf4b58a92b15ae5b3c11e235b8de2461b91c3627e12496fa07f77`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 2.3 MB (2281482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f392ca696149469d3691c7ffdbffb55dba0a7cc874998211f69c4b033b7d24`  
		Last Modified: Tue, 24 Feb 2026 20:22:39 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:702bb1b758b2b0b86544a326a57afe656f1da4018d2f2ac5e22a9596d9ea5dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73075764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52d7f1c907ee2f76702409fbfe17af5316afdb353b4746714b8f7394312884a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:34:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:37:27 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:37:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:37:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:37:27 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:54:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:54:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 21:54:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:54:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:54:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:54:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:54:58 GMT
USER fluent
# Tue, 24 Feb 2026 21:54:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:54:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc96269d7ff6661f7c783aa28ef266b6a3454b0b7270f35fd67c75efbb126325`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 1.3 MB (1262995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dde3052860b01def3c7729ab7e0b552cfc8471229c632727c524ba36ffa87c`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feb54b5087fc558951fafdb4a294dc5d0cfd9f91b23c76b4e5f03fb58403146`  
		Last Modified: Tue, 24 Feb 2026 20:37:36 GMT  
		Size: 37.9 MB (37906244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfd1652237e976a13ba3e6c119a312c9ef9b52d4d968f91702f2ed8dac11a6d`  
		Last Modified: Tue, 24 Feb 2026 20:37:35 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8f4af827fa0ee9a1256892f1bbf83c4271c6a35814b9292176c3c078b13f5b`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 6.0 MB (5956521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49fc31c05c8248f02920d77d8c9ba45d5403895207860b0ed4c01a5e2b6e86d6`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f480ee64da643f3dd1a9521699efb88c5788cc57f46d3c16546f8d1e0fd581a`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794edd3187fbf592f533456f685e8461ec4a4f97ab6d80e3f2777fc727af72f3`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:aeff6eb65638d187ee9dfc2632bd9a6fe5aa475c7732e02050a037648f7bd08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d7bc32560f9f9f482c4f0d1edf21542d17c45a3a16f10e6120f92b58bb2b61`

```dockerfile
```

-	Layers:
	-	`sha256:c5516e6bf9c46bc32b1d45a4de020a57104bea2b0d21a174426bc1b3b3e5a2aa`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 2.3 MB (2284453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61ab6a4efa546f12948f77ab6e386e9c29a6aa900ea73c9b8357b1bdb43c43e3`  
		Last Modified: Tue, 24 Feb 2026 21:55:06 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:249cd06a9583c174022bc1662a638183730f2eb3cf11ad58645af47ac58d552d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70944650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a202282d8340e112924e8c4e6b6f741d47d8511e6d65071ccf02ee62a9164`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:06:31 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 21:09:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 21:09:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 21:09:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 21:09:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 21:09:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 21:09:12 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 22:00:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 22:00:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 22:00:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 22:00:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 22:00:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 22:00:49 GMT
USER fluent
# Tue, 24 Feb 2026 22:00:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 22:00:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14feba02466030de4233bb2b9b4ae7bb8d22598db9db35967cc9269952aa2190`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 1.2 MB (1236637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991f1e7bee0c079b1385009eded49ec5445b76573d3c6311e6d7a8472bbeebd`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f4b57fa9f91ef9277385833d43232d221aae42613777d8a1984c4d140abdf8`  
		Last Modified: Tue, 24 Feb 2026 21:09:21 GMT  
		Size: 37.8 MB (37767330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865adf2d3ca7b76be7f98186142a67e87adc8e14da1a9c847d4838d387f91d2f`  
		Last Modified: Tue, 24 Feb 2026 21:09:20 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6215cd02e856f3f916f009645d1930216f1ea5046f717331deb0b0c628c0cb1f`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 5.7 MB (5724546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cbcfa781ef6a32d1924052e879b40cf20670dc5460b896852bb939d35097f6`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f810d4742ff15c72ffa1d88314e0af2232943762e952ba81264158f7c11a5e7`  
		Last Modified: Tue, 24 Feb 2026 22:00:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0491a7058409e826832ddd60b3500d0531fbf847813171676e8df47d10e7e60f`  
		Last Modified: Tue, 24 Feb 2026 22:01:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:616d833662b654cfdaefcd601933ef26a2c132b460c51932d43532a964e574aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141883a718ab52bba48c5df7dee9157f0bbb26b80a0830cac65470df72d406af`

```dockerfile
```

-	Layers:
	-	`sha256:3e6cabc9f406ac1d02f047192c16317f3ae30604e3c63cfd48324204afffb01d`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 2.3 MB (2282894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3db94822a243938772aec32d2ec10453a6f7b111f889e584043a103671ac7d69`  
		Last Modified: Tue, 24 Feb 2026 22:01:01 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:828404f45a0b0a32fec514fa74e419ac06f5a23433cd5d604319cc175e82d054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79521874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d16ebbf1045c14f44b80173504653196573d47d64c6678c057ce7b6f3daa26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:37 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 20:00:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 20:00:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:00:10 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 20:00:10 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 21:38:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 21:38:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 21:38:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 21:38:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 21:38:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 21:38:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 21:38:23 GMT
USER fluent
# Tue, 24 Feb 2026 21:38:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 21:38:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f75b690a5fd55169fbad21a29d8ed315a9d4042c310b1bf6f573673b222fc`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 1.3 MB (1261292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c26ba3937fd2b59db15d9b6d2d658d4dd4063b544cfdc5543f937af1ae20ee`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af054951d688ba98eecceef225934514c1bce049b94d72213bb07dbde8fb87`  
		Last Modified: Tue, 24 Feb 2026 20:01:00 GMT  
		Size: 42.1 MB (42074135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639b1a194a41b5d55ce4d7d2ec84ba51375ae840f4a37543134a924795e35a07`  
		Last Modified: Tue, 24 Feb 2026 20:00:46 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a08ed296b9681998efe65e6e0547331e19e4c85d582e56ee946b40f75bc53e`  
		Last Modified: Tue, 24 Feb 2026 21:38:32 GMT  
		Size: 6.0 MB (6043953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b51dce7afff466c28dbaf5e1b0183007860bc4d1b1ab4f805ff142df8b02efc`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c445911edf772b7b26b1a963f84eb02edbb6edf42beff8deb7d06eb236bf3`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1205244818e9d9295806167b757eeccf4c11d403b60d31509b2934897f702154`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ca791e8bd0f179910fdb549ce401bc962cc8bb5ad45ced6d1882cef650ede648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78018d21a04e4f823186dd34a8c235892d68b619bbd54d8343306f0feb00f0f2`

```dockerfile
```

-	Layers:
	-	`sha256:23aa4569b3fa9dc8f92fd32abf7c895fd4d19a8e8aa44bbc2fa60dd79a77028f`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 2.3 MB (2281754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50619cb3792635e604919c80a6837451d9333523df0b41771df7d709c5f105ad`  
		Last Modified: Tue, 24 Feb 2026 21:38:31 GMT  
		Size: 21.5 KB (21455 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:d4e441291fbcc948534053a6429efb66080283ffde02d2ff0ed8c733968d9de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:985aeed61e2de83466ff38ae8525b6052c73fe6a2c5dbe6fafccf426c3526b10`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:49:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 24 Feb 2026 19:51:44 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 24 Feb 2026 19:51:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 24 Feb 2026 19:51:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 24 Feb 2026 19:51:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:51:45 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 24 Feb 2026 19:51:45 GMT
CMD ["irb"]
# Tue, 24 Feb 2026 20:14:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 24 Feb 2026 20:14:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 24 Feb 2026 20:14:50 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 24 Feb 2026 20:14:50 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 24 Feb 2026 20:14:50 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 24 Feb 2026 20:14:50 GMT
USER fluent
# Tue, 24 Feb 2026 20:14:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 24 Feb 2026 20:14:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a892ff57419277a7fa8ad912b1813f1159602bd6d8068badf5bfb1d62a14993f`  
		Last Modified: Tue, 24 Feb 2026 19:51:53 GMT  
		Size: 1.3 MB (1287332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbea3e8ba0db554c2fac0167ff3e4daf51f3fbd5bc330d7217898dd5c65f7d2`  
		Last Modified: Tue, 24 Feb 2026 19:51:40 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2d9cc1d12b4edaca10bae974eeb96048293aec72576d8c3e8254d4431ce48c`  
		Last Modified: Tue, 24 Feb 2026 19:51:54 GMT  
		Size: 37.7 MB (37661562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ee811540cac1162511fd45e13f42fe19541d1f73c7d8a45b816037c2d0668a`  
		Last Modified: Tue, 24 Feb 2026 19:51:52 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fb7539d7a3851caa96e2bcccbb66a68fcf4dac4973414f51370ae37c4622ea`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 6.0 MB (6025681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25798218224060dbc499d8986f06d2eb074d58bf9345da4f05f6ed75f35fbc62`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed273dda7a96de12238121a09a97770b30f1889adddd7a0d5ffadceba370b6b`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0aa78822ed9aa54b3dfb41392b36b646e4f9bc15bb3037b819fad46d8f4fcf`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a8ce02d3271a6c38e6ac9845cc16d1c54480c4d0b2d183fb82b7d091b9387294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b96e28b5c2f4a99203e65e38ac879bef38fbdb184706b87fc865ed232d9ee3`

```dockerfile
```

-	Layers:
	-	`sha256:a48b838e0998fb5c2903ba45219be4a3b3db2a074344147cbfcb58b4d84339bb`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 2.3 MB (2278670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:587f45001b4aef0def6ce0691f65c51db7c9f957fe89daf5806210568c13de31`  
		Last Modified: Tue, 24 Feb 2026 20:14:58 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:3e85b7afdefefc0ceed38702aa8c6e83e6d900b88a7bba22e2988cc09521c314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81007295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92db795cc55a308b287141133fb2ebb98c3099b9cf82951c8aff9c3aaa3d8a3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:04:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 09:04:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 09:08:39 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 09:08:39 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:08:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 09:08:39 GMT
CMD ["irb"]
# Fri, 13 Feb 2026 18:50:59 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 13 Feb 2026 18:50:59 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Fri, 13 Feb 2026 18:50:59 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Fri, 13 Feb 2026 18:50:59 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 13 Feb 2026 18:51:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 13 Feb 2026 18:51:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 13 Feb 2026 18:51:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 13 Feb 2026 18:51:00 GMT
USER fluent
# Fri, 13 Feb 2026 18:51:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 13 Feb 2026 18:51:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1aee42d34fb7e3a2db6f83f2a84e17846ac990ed8ecf693a309ae759efdbdaa3`  
		Last Modified: Tue, 03 Feb 2026 01:16:35 GMT  
		Size: 33.6 MB (33600184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6be1f9ad8d9708d6d1dd902519422f937c816172bb2279df8827177290ce2c7`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 1.3 MB (1309384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69016493cd4b81c51b0ebe7726a06117b8c667e58289628f10d4662f959eb918`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eae5d6a287ac9deb00e76ee4f5bc8133dfa2ad449e09b28cbcef3715fe45f124`  
		Last Modified: Tue, 03 Feb 2026 09:09:01 GMT  
		Size: 39.5 MB (39519472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9277fefce554077ed90bf6814e28a9db303a96069b78e13ebbb958a92daa6d2d`  
		Last Modified: Tue, 03 Feb 2026 09:09:00 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceb39087a75c520eecf6fa1d6cca6b087321ba9c79cb338599d9739d4491b11`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 6.6 MB (6575848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19afb70fa211158dd4f6a97285e69a623a026dc5cbeb9c946cc0d9597470585`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff208f82e22958984a23e4b02712a779bdb4570c8422c467e124a8b264b0bb43`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9649c1f8ea25246f0060ad4dff7af4b5afe7280fec821c3bb316ce49cd25e607`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:372534f2d3f54414e8b10d874b438910a672bfe189b65a56796669b17fba2c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3279a02c907e4d5bf163f52ce92ba2acd37a5dc3693c358ad599f1dae6dc53`

```dockerfile
```

-	Layers:
	-	`sha256:772508226cfbbcde2d89894fbb9d6bfa67f21f85f9c7820774e4c4024df3c785`  
		Last Modified: Fri, 13 Feb 2026 18:51:20 GMT  
		Size: 2.3 MB (2285017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f660251e609f7c92dcf6085728502cdc3bdec0fc40fde1ae3dcbe42b7e15d262`  
		Last Modified: Fri, 13 Feb 2026 18:51:19 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:325c4ac442f736c13b434e56b7fde81681f7b089bb9a88139c4c8089520b06dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76758781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4123c819169f7a1c43c68cdbf71bc0fce9aeea2a49950405f4f3c7953a3d6d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:02:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV LANG=C.UTF-8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 25 Feb 2026 01:32:10 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 25 Feb 2026 01:32:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 25 Feb 2026 01:32:10 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 25 Feb 2026 01:32:10 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:32:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 25 Feb 2026 01:32:11 GMT
CMD ["irb"]
# Wed, 25 Feb 2026 02:39:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 25 Feb 2026 02:39:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 25 Feb 2026 02:39:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 25 Feb 2026 02:39:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 25 Feb 2026 02:39:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 25 Feb 2026 02:39:37 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 25 Feb 2026 02:39:37 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 25 Feb 2026 02:39:37 GMT
USER fluent
# Wed, 25 Feb 2026 02:39:37 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 25 Feb 2026 02:39:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4914443d3c4184b2c3ca5f7f265c77f7783c5fe40f5ff77daa520ded4b0a2c`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 1.3 MB (1294517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def914eff926e8e33e8d2ea6891e3ece82a54502d942da1cf995fac0cf626932`  
		Last Modified: Tue, 24 Feb 2026 23:08:11 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038fad6ee4d8be5d7dbfd8551d2a5d070571e5d13c57cfc9d2618d596970e34c`  
		Last Modified: Wed, 25 Feb 2026 01:32:41 GMT  
		Size: 39.2 MB (39192544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb56a57c12ad1160bc0ee7c91d149dab3f7a2a858afd9771d4f967a14a4533a`  
		Last Modified: Wed, 25 Feb 2026 01:32:39 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d528a35268e8e46fa75fdda5d210e6dbbb535b26387f024349e2351e5455edfd`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 6.4 MB (6431145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4914220566b082bf5096917093d86a2f05c15edd3bf91a0aebf285700aef707f`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a611c57f9809a0ad97f6a54adfb486209c5531824142c8a9f79fe2238b7953`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c41433679913e9f12adb749646999e0194b8012806661df0a3a786f5e6deea9`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:45ce6eafa5ff53cc997cf7bf28d3a7cd68637982865c75eaa2b9962145a945ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b56380c11cf0412a468c8aa4e2a1884f4b5ea388938a8fb40abafee4a64259`

```dockerfile
```

-	Layers:
	-	`sha256:fa1aca00461b819cd8ecd3a4ffe90129f1108cb248f3958784a2f61d22396899`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 2.3 MB (2282927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6ad2111eaf7ad708910e559db08048a2777e2fa6a210307b46f77f9c393b797`  
		Last Modified: Wed, 25 Feb 2026 02:39:53 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
