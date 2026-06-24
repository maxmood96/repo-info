## `fluentd:latest`

```console
$ docker pull fluentd@sha256:53ee500fb9f4a7ae83d3afeb25614b8e77d2c8e2d9f053617e6cd771d860d0ee
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
$ docker pull fluentd@sha256:447d736c26ad97aa5cdf263cd93166022133522a4abdcfa24c2bb7b442411469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79266377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4846ddec837a51f79cb6aff1957f995e8b03df510f0cd9fbab965b93ad3b79e7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:10:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:10:27 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 24 Jun 2026 02:12:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:12:48 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 24 Jun 2026 02:12:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 24 Jun 2026 02:12:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 24 Jun 2026 02:12:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 24 Jun 2026 02:12:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Jun 2026 02:12:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Jun 2026 02:12:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:12:48 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 24 Jun 2026 02:12:48 GMT
CMD ["irb"]
# Wed, 24 Jun 2026 02:47:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 24 Jun 2026 02:47:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 24 Jun 2026 02:47:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 24 Jun 2026 02:47:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 24 Jun 2026 02:47:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 24 Jun 2026 02:47:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 24 Jun 2026 02:47:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 24 Jun 2026 02:47:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 24 Jun 2026 02:47:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 24 Jun 2026 02:47:41 GMT
USER fluent
# Wed, 24 Jun 2026 02:47:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 24 Jun 2026 02:47:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e913b512d07c87e9abc1ba3e1cf375fd823c36df6e89124e4d4fe6a1be6194ac`  
		Last Modified: Wed, 24 Jun 2026 02:12:57 GMT  
		Size: 1.3 MB (1279947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec845402f25565d76e4def7b2766d51872aa83cb345533f62b68c46ed419b8`  
		Last Modified: Wed, 24 Jun 2026 02:12:57 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceef8f047d4b8e22321755ecb524c3567f66902127ae454c2623ece462186f2`  
		Last Modified: Wed, 24 Jun 2026 02:12:58 GMT  
		Size: 42.1 MB (42127201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05f870cc3d13d22f4950c0f13e754a7454afb145a36e4d4df06601c2af07481`  
		Last Modified: Wed, 24 Jun 2026 02:12:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cfa72105c5bf901d4cc5b4128bff604976700290b6d88a0ba6ef0b1c0575b2`  
		Last Modified: Wed, 24 Jun 2026 02:47:50 GMT  
		Size: 6.1 MB (6071417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0f6c8084605c5cc15d9c2b98d2c98d227d6d3e213415f72205b12da4bf7216`  
		Last Modified: Wed, 24 Jun 2026 02:47:50 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a3859e32f4bd0426a5c320915409a847a6501cbd4002fa85ead98025009328`  
		Last Modified: Wed, 24 Jun 2026 02:47:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2626d53f8bfd19c7165187a6e840c07eca00a02a95386a3ee2534def8fbbd35`  
		Last Modified: Wed, 24 Jun 2026 02:47:50 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:40fd5b13c1321a3fd48c86e95ec544ec17ec384c5f73e3e097521abad78e8e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265c039b50784031cc4fcf8398589afec86a31a9623dd7bcbb81af6baeb97b51`

```dockerfile
```

-	Layers:
	-	`sha256:aaf366152bf4d48f7a9af63cdbc34c5c60378ba9035a14ee4c0d445ce9dfea3f`  
		Last Modified: Wed, 24 Jun 2026 02:47:50 GMT  
		Size: 2.3 MB (2281853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a26e440ef78ce597dbf079473f26a66898899ded58b9795a5dee17169fa17089`  
		Last Modified: Wed, 24 Jun 2026 02:47:49 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:7c081b0ce2510dc1f2873a902941049ca54e4c5b1e8018db5ae8d3aaf29e1680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73121420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3346d899b9c9f7bff375745dc80ad4dbf83f7ee398ddc5d911ed5451fd456366`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:58:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:58:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 24 Jun 2026 03:05:08 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 03:05:08 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 24 Jun 2026 03:05:08 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 24 Jun 2026 03:05:08 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 24 Jun 2026 03:05:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 24 Jun 2026 03:05:08 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Jun 2026 03:05:08 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Jun 2026 03:05:08 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:05:08 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 24 Jun 2026 03:05:08 GMT
CMD ["irb"]
# Wed, 24 Jun 2026 04:16:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 24 Jun 2026 04:16:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 24 Jun 2026 04:16:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 24 Jun 2026 04:16:56 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 24 Jun 2026 04:16:56 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 24 Jun 2026 04:16:56 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 24 Jun 2026 04:16:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 24 Jun 2026 04:16:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 24 Jun 2026 04:16:56 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 24 Jun 2026 04:16:56 GMT
USER fluent
# Wed, 24 Jun 2026 04:16:56 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 24 Jun 2026 04:16:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:da43bc6a07a9cd7cc23faa538adc0797482747316b5a85b9f3f94ed17f6c1a2a`  
		Last Modified: Wed, 24 Jun 2026 00:28:12 GMT  
		Size: 28.0 MB (27959221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db95c4bc3f97dedc3f9e582ff5202f6b57d3e71aee467bcb84fce8f713bcb58`  
		Last Modified: Wed, 24 Jun 2026 03:02:02 GMT  
		Size: 1.3 MB (1263754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d162856780ab716a2defc7af4021c7a2258bf3dd0aa3523e7ee7ec7e59fc12`  
		Last Modified: Wed, 24 Jun 2026 03:02:03 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d801c52bb435d91b085b7a083f8b6f4ebcfd7e8cc0c0046ea8170727cabd89`  
		Last Modified: Wed, 24 Jun 2026 03:05:18 GMT  
		Size: 37.9 MB (37924243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f693f5a33c8359c6129ee6f4ac9a9a62fc91cdbffd733284e96e80aa3f07dfe`  
		Last Modified: Wed, 24 Jun 2026 03:05:16 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9353fb717d4660562ef27ba4dbce51284cc5dac0d885fc4a6832c8fd49ce52fc`  
		Last Modified: Wed, 24 Jun 2026 04:17:04 GMT  
		Size: 6.0 MB (5971812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8598c57615846c47e3d2890ba60948ae6ad9af3934c4c0cd725353df4b631b`  
		Last Modified: Wed, 24 Jun 2026 04:17:04 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473de20bdab17c5018cf828569a37d7f22956d4e69d05965511cc0cb9895124f`  
		Last Modified: Wed, 24 Jun 2026 04:17:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7080a95a78ffa7b0bf6be64464829663c648dc7eb54231c3a28a5df7ae0c4992`  
		Last Modified: Wed, 24 Jun 2026 04:17:04 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:bb37d376473721d32a514aef92d52ea27a97db140ab4a8ac5566b5f2facf2971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96803c34820a3d26ed61c00db5e38afeff657634fd99f001a7275ebba6d2e950`

```dockerfile
```

-	Layers:
	-	`sha256:7b54224a1bae6da4c0890fc89e42019dd185a46712fdc631638a877101abd462`  
		Last Modified: Wed, 24 Jun 2026 04:17:04 GMT  
		Size: 2.3 MB (2284824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e5789cb369ef5c018ef1dfdcef1f98584854be1d31f945bf10004d26532542`  
		Last Modified: Wed, 24 Jun 2026 04:17:04 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:3f46cb6af9c1c7f2a6d7a9adc433f2b05b22480d7edc213f4f52ab3aee622c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70970257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aaf2581107ae14592d77700ac21447fdf43e00ab98b3cd45176d02e2ef0ba36`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 03:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:33:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 24 Jun 2026 03:36:33 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 03:36:33 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 24 Jun 2026 03:36:33 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 24 Jun 2026 03:36:33 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 24 Jun 2026 03:36:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 24 Jun 2026 03:36:33 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Jun 2026 03:36:33 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Jun 2026 03:36:33 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 03:36:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 24 Jun 2026 03:36:33 GMT
CMD ["irb"]
# Wed, 24 Jun 2026 04:28:03 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 24 Jun 2026 04:28:03 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 24 Jun 2026 04:28:03 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 24 Jun 2026 04:28:03 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 24 Jun 2026 04:28:03 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 24 Jun 2026 04:28:03 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 24 Jun 2026 04:28:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 24 Jun 2026 04:28:03 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 24 Jun 2026 04:28:03 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 24 Jun 2026 04:28:03 GMT
USER fluent
# Wed, 24 Jun 2026 04:28:03 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 24 Jun 2026 04:28:03 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e32a2a4f925fa9fa2afa539d0e1655064de0b6f4216b35c8b8245446e291c0d`  
		Last Modified: Wed, 24 Jun 2026 03:36:42 GMT  
		Size: 1.2 MB (1237620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6832d720b0871aa4eb1872eb676002a164e02ddc57d3db6ff869807addc1aeb`  
		Last Modified: Wed, 24 Jun 2026 03:36:41 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e7016de36815869540d026f85636e3c36faf34dd311eed7f9d363a06fe41d7`  
		Last Modified: Wed, 24 Jun 2026 03:36:43 GMT  
		Size: 37.8 MB (37781611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d813cab5790f8f491561dc617634f70949c8a8485ae398ef41c827df4fd20aa0`  
		Last Modified: Wed, 24 Jun 2026 03:36:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dd6e8ba9427d95760da765f16d02878a91445f2068b0f74754c22310348e9f`  
		Last Modified: Wed, 24 Jun 2026 04:28:11 GMT  
		Size: 5.7 MB (5737580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12e1c3223ff90c08367f39a41e5bbab2c5dd21030142bcbfaf94473bb12cf324`  
		Last Modified: Wed, 24 Jun 2026 04:28:11 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc50ffe4983fe32ddaf6e1055d46fa33c2e0017e63dc91fbac4d8cd4e647d9d3`  
		Last Modified: Wed, 24 Jun 2026 04:28:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29568ed27afce3eab92e5267950bd9fd5c9f12ddfb43995881d7071e79c14143`  
		Last Modified: Wed, 24 Jun 2026 04:28:11 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:7bec207dca78b8721a1c10e72cd75b52835b2f884ff5a3b3ee1bad768c7e3695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa0fbfc6d162e9db69aa7e523d8a37207399e5a0be188fa0c0d21b24157249e`

```dockerfile
```

-	Layers:
	-	`sha256:97bdc3e341e8bbaae1c46de221e04cc91b94bd06eda081bc993f3a61f610f96c`  
		Last Modified: Wed, 24 Jun 2026 04:28:11 GMT  
		Size: 2.3 MB (2283265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:213bf44c540994487ac05d2d1abb98206d99221e64d43ada8906bb078005bea3`  
		Last Modified: Wed, 24 Jun 2026 04:28:10 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:1110d9590b6848109ccba7083539c78e14be84ed6eba2d73c74d20d3af0a2dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79556244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8be14c969896b8b60957670d17a13a908e4fd90f95b81b661c0c5cb143298f2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:17:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 24 Jun 2026 02:19:54 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:19:54 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 24 Jun 2026 02:19:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 24 Jun 2026 02:19:54 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 24 Jun 2026 02:19:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 24 Jun 2026 02:19:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Jun 2026 02:19:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Jun 2026 02:19:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:19:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 24 Jun 2026 02:19:54 GMT
CMD ["irb"]
# Wed, 24 Jun 2026 03:26:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 24 Jun 2026 03:26:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 24 Jun 2026 03:26:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 24 Jun 2026 03:26:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 24 Jun 2026 03:26:19 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 24 Jun 2026 03:26:19 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 24 Jun 2026 03:26:19 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 24 Jun 2026 03:26:19 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 24 Jun 2026 03:26:19 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 24 Jun 2026 03:26:19 GMT
USER fluent
# Wed, 24 Jun 2026 03:26:19 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 24 Jun 2026 03:26:19 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf759fde2d69dc6950e0d37d48dc26ef8b26ae51931b32e3e4740bae7a6e8e8`  
		Last Modified: Wed, 24 Jun 2026 02:20:04 GMT  
		Size: 1.3 MB (1261934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eaade87d8ac9af7935a34d7009dde906fbb9587384f0e8ae826f15524bcd34`  
		Last Modified: Wed, 24 Jun 2026 02:20:04 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3275d25a5f42a9784aa64eee923aebe7decf9e9862841d1d22f651005f508a7`  
		Last Modified: Wed, 24 Jun 2026 02:20:05 GMT  
		Size: 42.1 MB (42078916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c19bfd430bafc02fb0894068d6bedd5b6689f125083bd5cd2fbc1ec5e8f14b`  
		Last Modified: Wed, 24 Jun 2026 02:20:04 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbe8a0e1733d400befb0f6a5fbb8a3dfec7e1144955299ab73f8c9e14dd861`  
		Last Modified: Wed, 24 Jun 2026 03:26:28 GMT  
		Size: 6.1 MB (6064447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4753b00080a1db090a8d37cd60964d08e5edcf172ab61d304c3e287a44657114`  
		Last Modified: Wed, 24 Jun 2026 03:26:27 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a43e4fb229381f9362b69ba5ba97f6bcc77523aa781e1af7becbd9919a0b5b`  
		Last Modified: Wed, 24 Jun 2026 03:26:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64a6049ed7edf141079631d28c0f926073297e9f89b544ba49e6e4cba9d2083`  
		Last Modified: Wed, 24 Jun 2026 03:26:27 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:b9f44af47a947b2f2ee80cdedf900c612becf0737e9662472d8c78009f1843f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff31a345fe25d98320e37e774dfa6eb506659d9c44eaaeb0123e0d246b79cf55`

```dockerfile
```

-	Layers:
	-	`sha256:90771836964609baaf1213b22ef8d0c8401e8d36885db83c85ba19413b6756d8`  
		Last Modified: Wed, 24 Jun 2026 03:26:27 GMT  
		Size: 2.3 MB (2282117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881a67d3cc7980f7fc01f64b2ff7a96137eda9806751fd0120a2bb5409aad4ea`  
		Last Modified: Wed, 24 Jun 2026 03:26:27 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:f4d3f1d4059a8f19f19332620d887ab2001e9d69662d3cea331f1924b8a15d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76295467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7532d9f8f81f3dc216d8b1559080449769018c2e93ac3752126e6313ad208918`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:10:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:10:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 24 Jun 2026 02:12:36 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:12:36 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 24 Jun 2026 02:12:36 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 24 Jun 2026 02:12:36 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 24 Jun 2026 02:12:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 24 Jun 2026 02:12:36 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Jun 2026 02:12:36 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Jun 2026 02:12:36 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:12:36 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 24 Jun 2026 02:12:36 GMT
CMD ["irb"]
# Wed, 24 Jun 2026 02:52:32 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 24 Jun 2026 02:52:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 24 Jun 2026 02:52:32 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 24 Jun 2026 02:52:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 24 Jun 2026 02:52:32 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 24 Jun 2026 02:52:32 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 24 Jun 2026 02:52:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 24 Jun 2026 02:52:32 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 24 Jun 2026 02:52:32 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 24 Jun 2026 02:52:32 GMT
USER fluent
# Wed, 24 Jun 2026 02:52:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 24 Jun 2026 02:52:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c682104c40c9341fc21831790fba470fe5957b47e3c0ad8f662138ce2699c4`  
		Last Modified: Wed, 24 Jun 2026 02:12:44 GMT  
		Size: 1.3 MB (1287817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd59d99af79ce94e82baf5b38bbf1f55ba5800dfc2ea339bcc7625c957f3300`  
		Last Modified: Wed, 24 Jun 2026 02:12:44 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173a07eb5c284fb2e1d13a759728001dddd819b7bdabd8a420126a99696034e`  
		Last Modified: Wed, 24 Jun 2026 02:12:46 GMT  
		Size: 37.7 MB (37661995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68189011e57f35acf96a78a7970324a3cdcfdd97a9860a56e431e93430c064d`  
		Last Modified: Wed, 24 Jun 2026 02:12:44 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89365b69a728f26f441fb3f49dcc02d1f5093791fa8c0f4d6cdce907cfca4b49`  
		Last Modified: Wed, 24 Jun 2026 02:52:41 GMT  
		Size: 6.0 MB (6042052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c039235d33e542d1b56b36868d8f445ce28d410142c9bdf672ec68ede723dab7`  
		Last Modified: Wed, 24 Jun 2026 02:52:41 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423088c2614b024848675d88d6c77137e344ab5a841c6aea70d2225e75199d77`  
		Last Modified: Wed, 24 Jun 2026 02:52:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7e7018cea0fa812a50ed77478a9cb0a0bb9495341d6ad542f14d723b563e83`  
		Last Modified: Wed, 24 Jun 2026 02:52:41 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:811ab9da9261bcd06d20b3fea03e0367de67eb5164d8923c9a4d505399aafff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26594397d817628f9039e31111c9ae23d00e9152624fb99d9bbd29a7bb36438`

```dockerfile
```

-	Layers:
	-	`sha256:4326f04ff624e709142019c312528853f9e60062ff624384444c9847712462d9`  
		Last Modified: Wed, 24 Jun 2026 02:52:41 GMT  
		Size: 2.3 MB (2279041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82aa0eec2d94042a2d26ac6536da438fec6064cb2733a4c8e393bc3920127e93`  
		Last Modified: Wed, 24 Jun 2026 02:52:41 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:099333ce1e2c3e852d7a9c612cd4fbc47bb16e3700b98b948642b23142a79480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81042955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e608d30afccf837655e24bfdc59f8c76adbc7e1625fc456c5ed08457b8a2ca8f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 08:52:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 08:52:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 09:03:22 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 09:03:22 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 09:03:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 09:03:22 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 09:03:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 09:03:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 09:03:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 09:03:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:03:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 09:03:22 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 12:33:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 12:33:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 12:33:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 12:33:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 12:33:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 12:33:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 12:33:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 12:33:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 12:33:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 12:33:20 GMT
USER fluent
# Thu, 11 Jun 2026 12:33:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 12:33:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83c673edc1c2d725fa2ef6b8959d16ccc8a733e791039eba82297519e842d77`  
		Last Modified: Thu, 11 Jun 2026 08:56:35 GMT  
		Size: 1.3 MB (1310330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cf349dc2ac17b389c3f3ab5c204ae1396cdd7aef51d6dc463f3bd821d41588`  
		Last Modified: Thu, 11 Jun 2026 08:56:35 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47e0628203a64668c25dd6fe0bfe6049dcb9c38f6bda81093ed9c461b73ff8e`  
		Last Modified: Thu, 11 Jun 2026 09:03:41 GMT  
		Size: 39.5 MB (39532698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8608fcbd585bea54b6209ce592feff08a3a5d8fa2232409a70e5840f89168c`  
		Last Modified: Thu, 11 Jun 2026 09:03:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6244a0e1343982f4b9497fdec6a8a5f301da36864d05e53ad1fb173da4bdd267`  
		Last Modified: Thu, 11 Jun 2026 12:33:37 GMT  
		Size: 6.6 MB (6591190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1dc1f8da062974fec08638cdf21cc1ba62800e3ce3bf018dcc4cd8b8307a92`  
		Last Modified: Thu, 11 Jun 2026 12:33:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e7c2e20d69e27607af4ae19787cdd27168b774efed3f4ed40d409b276937a9`  
		Last Modified: Thu, 11 Jun 2026 12:33:36 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fee49fb55e6487066533b2839cea8ddbcffb6848897386c6b16236e94c0c31`  
		Last Modified: Thu, 11 Jun 2026 12:33:36 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:7eca66441606e08652b77bd7f1549f0fba7787c5e99c97154eb4812ecae502bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f00e7c012a26c24f9cc96561351a1d347383a872fd10fcc6aae81e0e8e361a8`

```dockerfile
```

-	Layers:
	-	`sha256:887101c86baf0001987685c94963f295fd726b41517327f3b6b4952c26fef758`  
		Last Modified: Thu, 11 Jun 2026 12:33:36 GMT  
		Size: 2.3 MB (2285388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01f195272d68f02a6bc4dd3d41be592c68dd9da6bae4d8132770d811bf6e8ed`  
		Last Modified: Thu, 11 Jun 2026 12:33:36 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:8e1b956471e2a4f2eb4f9c92ec157543f9ab2847bb28529c6d3cdf77e0a52e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76805582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e63ab4423596cee91c1e55a206a2f6a3500149d8a4f61f592f2455f9b580703`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 03:57:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:57:51 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 24 Jun 2026 04:04:12 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 04:04:12 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 24 Jun 2026 04:04:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 24 Jun 2026 04:04:12 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 24 Jun 2026 04:04:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 24 Jun 2026 04:04:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 24 Jun 2026 04:04:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 24 Jun 2026 04:04:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:04:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 24 Jun 2026 04:04:12 GMT
CMD ["irb"]
# Wed, 24 Jun 2026 05:10:03 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 24 Jun 2026 05:10:03 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 24 Jun 2026 05:10:03 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 24 Jun 2026 05:10:03 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 24 Jun 2026 05:10:03 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 24 Jun 2026 05:10:03 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 24 Jun 2026 05:10:03 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 24 Jun 2026 05:10:03 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 24 Jun 2026 05:10:03 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 24 Jun 2026 05:10:03 GMT
USER fluent
# Wed, 24 Jun 2026 05:10:03 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 24 Jun 2026 05:10:03 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cec6b891317ab02e06d809653d065f108aab74b4570d3da613df7a30b973f3e`  
		Last Modified: Wed, 24 Jun 2026 04:00:53 GMT  
		Size: 1.3 MB (1294934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51a16c82807c979dd8c1cd8835e6f6c8b04ca0a4227de178a7bf40a7bf2e37c`  
		Last Modified: Wed, 24 Jun 2026 04:00:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2951b746a57e55d8c8827a0a82618e964ea45a04d043afe32bc7752f3ddf865c`  
		Last Modified: Wed, 24 Jun 2026 04:04:26 GMT  
		Size: 39.2 MB (39207776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2dc408b4486dc719a33e54625b6f1d46fff493669d5d7fbf1c057888e7b11c`  
		Last Modified: Wed, 24 Jun 2026 04:04:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d6e4e508e58afc7bc18da6a7a66dcb749d371d21b5db29ef3d61cd3edc75d4`  
		Last Modified: Wed, 24 Jun 2026 05:10:16 GMT  
		Size: 6.4 MB (6449096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cf32ef63e8b5c9f6e16105a0ea5d1f280cf0cb1bdb98583e0d94b759d721ca`  
		Last Modified: Wed, 24 Jun 2026 05:10:16 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9866366a3c26b0da02dd9d821e8129c3e01367ac750641e7a5169335a9c8a4b`  
		Last Modified: Wed, 24 Jun 2026 05:10:16 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b708b0993b958d812a2261b360c4c6f2e9efdf97bab020af8ce8dde105e5b6b`  
		Last Modified: Wed, 24 Jun 2026 05:10:16 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:81181d66f1352e041cc93f8e4cca68304fb1565c13ba5e7f7ce85b8371535be5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940a7509f2a5d4761573bee523a7f8923e14c887536b0804efaa28166ce00a01`

```dockerfile
```

-	Layers:
	-	`sha256:c03e9a738b8ef80502b2c7c2c72adb8cdc6079e0b7abaaf818bcd2c08474c456`  
		Last Modified: Wed, 24 Jun 2026 05:10:16 GMT  
		Size: 2.3 MB (2283298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a97eea95a1c86d82ac0a69a54d4052bb1d29cd55c3f5deb29ac4ee1cc87c4f9f`  
		Last Modified: Wed, 24 Jun 2026 05:10:16 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
