<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.19-1`](#fluentdv119-1)
-	[`fluentd:v1.19-debian-1`](#fluentdv119-debian-1)
-	[`fluentd:v1.19.2-1.0`](#fluentdv1192-10)
-	[`fluentd:v1.19.2-debian-1.0`](#fluentdv1192-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:1e238cce77fbe4c957e7efda342faba1c19441db6bee4cba89e3610c6eb2bdd5
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
$ docker pull fluentd@sha256:6475829b7644defa046da01f90644ec117e006c368e7ac87ada0befab5a5248b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76294002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7858c18ede6e8ab322771d1f42d6d8d3966f70b311c95e149a063fdef7df770`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:10:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 01:13:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:13:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 02:41:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 02:41:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 02:41:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 02:41:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 02:41:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 02:41:06 GMT
USER fluent
# Thu, 11 Jun 2026 02:41:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 02:41:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559b3beccacfe2507c7675689b3dcf322080300e5521890dbe4f42f508741680`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 1.3 MB (1287796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509d10f08039e48d3ade7bbe7dff9f8ee7ee76ef13f936e404824c8068446c1`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfedbe7d55d7141e3d1a588485f0412ed89261ab791f2535218e85ec39cca8d`  
		Last Modified: Thu, 11 Jun 2026 01:13:36 GMT  
		Size: 37.7 MB (37661759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ec848032e463e5e2f43d2446bedda0d5fa4791a14a5bb0c774cbb9859ee684`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bcced4715bf20e33ddc912bddb71c911c1a2277865c382c6ff541e989c6b1e`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 6.0 MB (6040858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a514740bdb40ab9a6879bc860fdf279b03d5545529f34304f363dd8a014d2ce2`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96470ce34b035b1163c61af6fb9f6569c31cdd64812278ea7e18fd3b9b3cc4fc`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dc96bea851f897f04bb4e7ccaabce918dad8900d0e7fcdf05dc7ba0b94a6c1`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:24b786d935282875dc6b7162dabf3073788072a892a0093df4c2fcba89ee83af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2537f501fef0d86e5db0aa6af2c284368f3945c25cc54095ecdfab7135a73f`

```dockerfile
```

-	Layers:
	-	`sha256:25a31722ecad71526d5b03e0cf5da4798100a7f8758b7d3a583e378d2aa2442a`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 2.3 MB (2279041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bc518b644a1a3387e522fc15e481921ad250dfa9a2e186f0310b82ecddd10d`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
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
$ docker pull fluentd@sha256:20559f80aca1d03f9616c249daa8564ad7826db94e79a781b5383a8d9e2cffd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76814516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7fcf8c858da3b2c3a2fd1abddb0c7f6a696c6c6ff5a57e3aa061f203dd285d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:55:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:55:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 03:02:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 03:02:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 03:02:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:02:13 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 04:02:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 04:02:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 04:02:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 04:02:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 04:02:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 04:02:40 GMT
USER fluent
# Thu, 11 Jun 2026 04:02:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 04:02:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04b17d55015cef06ef07e9fb2fe3d7c817f54396d865c92c6a4fa5c4c9e9d0`  
		Last Modified: Thu, 11 Jun 2026 02:58:58 GMT  
		Size: 1.3 MB (1294918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9c84bf624656635c57e41b1246f77049d77c0dd6fefa9dcd6322009a2d6c0`  
		Last Modified: Thu, 11 Jun 2026 02:58:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67491b3c08aa81e3ffc7d706f180fa9361772999367dd9bf8d40309d1f7befe`  
		Last Modified: Thu, 11 Jun 2026 03:02:29 GMT  
		Size: 39.2 MB (39217690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d230f4d88a954662423ef62595d6fcad5668b6cb3dfb9c100a31231da54857`  
		Last Modified: Thu, 11 Jun 2026 03:02:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223343b9f7a5ff99779445b1b4a073ce3175f42fe34198eef4148f105a7fd228`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 6.4 MB (6448164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b08ea2373cabdf05df4da7786a810af865963f98eed9f473ba4ee0c0aa631ba`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cf132b1b39c3e52d83989a6b52be0f7fc8726a1cc26fe78dfdc3e50eeb63ce`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce5b372c35d91a79642056162a37cfd0ee518457b74b9cd492cfb5220699ac2`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:a47ddc3a3027055e40c8cfae8b782e0136290e14223aa8cd0359abf38ffa435f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1201b05cd4d2fa066dc6b4bf0c4f46f39f642509c778165f0dad04b2b975de`

```dockerfile
```

-	Layers:
	-	`sha256:d31301b16bbb97954f1849c6c10530d930e0669591ae97392a1287684e98acf8`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 2.3 MB (2283298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7265756a9f8219dfe82b262db584f0070f6617559d11880276c6a5e201b121fb`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:1e238cce77fbe4c957e7efda342faba1c19441db6bee4cba89e3610c6eb2bdd5
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

### `fluentd:v1.19-1` - unknown; unknown

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

### `fluentd:v1.19-1` - linux; arm variant v5

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

### `fluentd:v1.19-1` - unknown; unknown

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

### `fluentd:v1.19-1` - linux; arm variant v7

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

### `fluentd:v1.19-1` - unknown; unknown

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

### `fluentd:v1.19-1` - linux; arm64 variant v8

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

### `fluentd:v1.19-1` - unknown; unknown

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

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:6475829b7644defa046da01f90644ec117e006c368e7ac87ada0befab5a5248b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76294002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7858c18ede6e8ab322771d1f42d6d8d3966f70b311c95e149a063fdef7df770`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:10:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 01:13:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:13:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 02:41:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 02:41:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 02:41:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 02:41:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 02:41:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 02:41:06 GMT
USER fluent
# Thu, 11 Jun 2026 02:41:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 02:41:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559b3beccacfe2507c7675689b3dcf322080300e5521890dbe4f42f508741680`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 1.3 MB (1287796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509d10f08039e48d3ade7bbe7dff9f8ee7ee76ef13f936e404824c8068446c1`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfedbe7d55d7141e3d1a588485f0412ed89261ab791f2535218e85ec39cca8d`  
		Last Modified: Thu, 11 Jun 2026 01:13:36 GMT  
		Size: 37.7 MB (37661759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ec848032e463e5e2f43d2446bedda0d5fa4791a14a5bb0c774cbb9859ee684`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bcced4715bf20e33ddc912bddb71c911c1a2277865c382c6ff541e989c6b1e`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 6.0 MB (6040858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a514740bdb40ab9a6879bc860fdf279b03d5545529f34304f363dd8a014d2ce2`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96470ce34b035b1163c61af6fb9f6569c31cdd64812278ea7e18fd3b9b3cc4fc`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dc96bea851f897f04bb4e7ccaabce918dad8900d0e7fcdf05dc7ba0b94a6c1`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:24b786d935282875dc6b7162dabf3073788072a892a0093df4c2fcba89ee83af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2537f501fef0d86e5db0aa6af2c284368f3945c25cc54095ecdfab7135a73f`

```dockerfile
```

-	Layers:
	-	`sha256:25a31722ecad71526d5b03e0cf5da4798100a7f8758b7d3a583e378d2aa2442a`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 2.3 MB (2279041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bc518b644a1a3387e522fc15e481921ad250dfa9a2e186f0310b82ecddd10d`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

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

### `fluentd:v1.19-1` - unknown; unknown

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

### `fluentd:v1.19-1` - linux; s390x

```console
$ docker pull fluentd@sha256:20559f80aca1d03f9616c249daa8564ad7826db94e79a781b5383a8d9e2cffd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76814516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7fcf8c858da3b2c3a2fd1abddb0c7f6a696c6c6ff5a57e3aa061f203dd285d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:55:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:55:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 03:02:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 03:02:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 03:02:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:02:13 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 04:02:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 04:02:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 04:02:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 04:02:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 04:02:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 04:02:40 GMT
USER fluent
# Thu, 11 Jun 2026 04:02:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 04:02:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04b17d55015cef06ef07e9fb2fe3d7c817f54396d865c92c6a4fa5c4c9e9d0`  
		Last Modified: Thu, 11 Jun 2026 02:58:58 GMT  
		Size: 1.3 MB (1294918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9c84bf624656635c57e41b1246f77049d77c0dd6fefa9dcd6322009a2d6c0`  
		Last Modified: Thu, 11 Jun 2026 02:58:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67491b3c08aa81e3ffc7d706f180fa9361772999367dd9bf8d40309d1f7befe`  
		Last Modified: Thu, 11 Jun 2026 03:02:29 GMT  
		Size: 39.2 MB (39217690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d230f4d88a954662423ef62595d6fcad5668b6cb3dfb9c100a31231da54857`  
		Last Modified: Thu, 11 Jun 2026 03:02:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223343b9f7a5ff99779445b1b4a073ce3175f42fe34198eef4148f105a7fd228`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 6.4 MB (6448164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b08ea2373cabdf05df4da7786a810af865963f98eed9f473ba4ee0c0aa631ba`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cf132b1b39c3e52d83989a6b52be0f7fc8726a1cc26fe78dfdc3e50eeb63ce`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce5b372c35d91a79642056162a37cfd0ee518457b74b9cd492cfb5220699ac2`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a47ddc3a3027055e40c8cfae8b782e0136290e14223aa8cd0359abf38ffa435f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1201b05cd4d2fa066dc6b4bf0c4f46f39f642509c778165f0dad04b2b975de`

```dockerfile
```

-	Layers:
	-	`sha256:d31301b16bbb97954f1849c6c10530d930e0669591ae97392a1287684e98acf8`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 2.3 MB (2283298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7265756a9f8219dfe82b262db584f0070f6617559d11880276c6a5e201b121fb`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:1e238cce77fbe4c957e7efda342faba1c19441db6bee4cba89e3610c6eb2bdd5
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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; arm variant v5

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; arm variant v7

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:6475829b7644defa046da01f90644ec117e006c368e7ac87ada0befab5a5248b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76294002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7858c18ede6e8ab322771d1f42d6d8d3966f70b311c95e149a063fdef7df770`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:10:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 01:13:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:13:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 02:41:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 02:41:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 02:41:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 02:41:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 02:41:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 02:41:06 GMT
USER fluent
# Thu, 11 Jun 2026 02:41:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 02:41:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559b3beccacfe2507c7675689b3dcf322080300e5521890dbe4f42f508741680`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 1.3 MB (1287796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509d10f08039e48d3ade7bbe7dff9f8ee7ee76ef13f936e404824c8068446c1`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfedbe7d55d7141e3d1a588485f0412ed89261ab791f2535218e85ec39cca8d`  
		Last Modified: Thu, 11 Jun 2026 01:13:36 GMT  
		Size: 37.7 MB (37661759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ec848032e463e5e2f43d2446bedda0d5fa4791a14a5bb0c774cbb9859ee684`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bcced4715bf20e33ddc912bddb71c911c1a2277865c382c6ff541e989c6b1e`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 6.0 MB (6040858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a514740bdb40ab9a6879bc860fdf279b03d5545529f34304f363dd8a014d2ce2`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96470ce34b035b1163c61af6fb9f6569c31cdd64812278ea7e18fd3b9b3cc4fc`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dc96bea851f897f04bb4e7ccaabce918dad8900d0e7fcdf05dc7ba0b94a6c1`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:24b786d935282875dc6b7162dabf3073788072a892a0093df4c2fcba89ee83af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2537f501fef0d86e5db0aa6af2c284368f3945c25cc54095ecdfab7135a73f`

```dockerfile
```

-	Layers:
	-	`sha256:25a31722ecad71526d5b03e0cf5da4798100a7f8758b7d3a583e378d2aa2442a`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 2.3 MB (2279041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bc518b644a1a3387e522fc15e481921ad250dfa9a2e186f0310b82ecddd10d`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:20559f80aca1d03f9616c249daa8564ad7826db94e79a781b5383a8d9e2cffd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76814516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7fcf8c858da3b2c3a2fd1abddb0c7f6a696c6c6ff5a57e3aa061f203dd285d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:55:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:55:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 03:02:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 03:02:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 03:02:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:02:13 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 04:02:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 04:02:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 04:02:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 04:02:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 04:02:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 04:02:40 GMT
USER fluent
# Thu, 11 Jun 2026 04:02:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 04:02:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04b17d55015cef06ef07e9fb2fe3d7c817f54396d865c92c6a4fa5c4c9e9d0`  
		Last Modified: Thu, 11 Jun 2026 02:58:58 GMT  
		Size: 1.3 MB (1294918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9c84bf624656635c57e41b1246f77049d77c0dd6fefa9dcd6322009a2d6c0`  
		Last Modified: Thu, 11 Jun 2026 02:58:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67491b3c08aa81e3ffc7d706f180fa9361772999367dd9bf8d40309d1f7befe`  
		Last Modified: Thu, 11 Jun 2026 03:02:29 GMT  
		Size: 39.2 MB (39217690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d230f4d88a954662423ef62595d6fcad5668b6cb3dfb9c100a31231da54857`  
		Last Modified: Thu, 11 Jun 2026 03:02:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223343b9f7a5ff99779445b1b4a073ce3175f42fe34198eef4148f105a7fd228`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 6.4 MB (6448164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b08ea2373cabdf05df4da7786a810af865963f98eed9f473ba4ee0c0aa631ba`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cf132b1b39c3e52d83989a6b52be0f7fc8726a1cc26fe78dfdc3e50eeb63ce`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce5b372c35d91a79642056162a37cfd0ee518457b74b9cd492cfb5220699ac2`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a47ddc3a3027055e40c8cfae8b782e0136290e14223aa8cd0359abf38ffa435f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1201b05cd4d2fa066dc6b4bf0c4f46f39f642509c778165f0dad04b2b975de`

```dockerfile
```

-	Layers:
	-	`sha256:d31301b16bbb97954f1849c6c10530d930e0669591ae97392a1287684e98acf8`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 2.3 MB (2283298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7265756a9f8219dfe82b262db584f0070f6617559d11880276c6a5e201b121fb`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-1.0`

```console
$ docker pull fluentd@sha256:1e238cce77fbe4c957e7efda342faba1c19441db6bee4cba89e3610c6eb2bdd5
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

### `fluentd:v1.19.2-1.0` - unknown; unknown

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

### `fluentd:v1.19.2-1.0` - linux; arm variant v5

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

### `fluentd:v1.19.2-1.0` - unknown; unknown

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

### `fluentd:v1.19.2-1.0` - linux; arm variant v7

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

### `fluentd:v1.19.2-1.0` - unknown; unknown

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

### `fluentd:v1.19.2-1.0` - linux; arm64 variant v8

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

### `fluentd:v1.19.2-1.0` - unknown; unknown

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

### `fluentd:v1.19.2-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:6475829b7644defa046da01f90644ec117e006c368e7ac87ada0befab5a5248b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76294002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7858c18ede6e8ab322771d1f42d6d8d3966f70b311c95e149a063fdef7df770`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:10:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 01:13:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:13:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 02:41:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 02:41:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 02:41:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 02:41:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 02:41:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 02:41:06 GMT
USER fluent
# Thu, 11 Jun 2026 02:41:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 02:41:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559b3beccacfe2507c7675689b3dcf322080300e5521890dbe4f42f508741680`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 1.3 MB (1287796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509d10f08039e48d3ade7bbe7dff9f8ee7ee76ef13f936e404824c8068446c1`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfedbe7d55d7141e3d1a588485f0412ed89261ab791f2535218e85ec39cca8d`  
		Last Modified: Thu, 11 Jun 2026 01:13:36 GMT  
		Size: 37.7 MB (37661759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ec848032e463e5e2f43d2446bedda0d5fa4791a14a5bb0c774cbb9859ee684`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bcced4715bf20e33ddc912bddb71c911c1a2277865c382c6ff541e989c6b1e`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 6.0 MB (6040858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a514740bdb40ab9a6879bc860fdf279b03d5545529f34304f363dd8a014d2ce2`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96470ce34b035b1163c61af6fb9f6569c31cdd64812278ea7e18fd3b9b3cc4fc`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dc96bea851f897f04bb4e7ccaabce918dad8900d0e7fcdf05dc7ba0b94a6c1`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:24b786d935282875dc6b7162dabf3073788072a892a0093df4c2fcba89ee83af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2537f501fef0d86e5db0aa6af2c284368f3945c25cc54095ecdfab7135a73f`

```dockerfile
```

-	Layers:
	-	`sha256:25a31722ecad71526d5b03e0cf5da4798100a7f8758b7d3a583e378d2aa2442a`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 2.3 MB (2279041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bc518b644a1a3387e522fc15e481921ad250dfa9a2e186f0310b82ecddd10d`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; ppc64le

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

### `fluentd:v1.19.2-1.0` - unknown; unknown

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

### `fluentd:v1.19.2-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:20559f80aca1d03f9616c249daa8564ad7826db94e79a781b5383a8d9e2cffd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76814516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7fcf8c858da3b2c3a2fd1abddb0c7f6a696c6c6ff5a57e3aa061f203dd285d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:55:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:55:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 03:02:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 03:02:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 03:02:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:02:13 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 04:02:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 04:02:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 04:02:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 04:02:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 04:02:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 04:02:40 GMT
USER fluent
# Thu, 11 Jun 2026 04:02:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 04:02:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04b17d55015cef06ef07e9fb2fe3d7c817f54396d865c92c6a4fa5c4c9e9d0`  
		Last Modified: Thu, 11 Jun 2026 02:58:58 GMT  
		Size: 1.3 MB (1294918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9c84bf624656635c57e41b1246f77049d77c0dd6fefa9dcd6322009a2d6c0`  
		Last Modified: Thu, 11 Jun 2026 02:58:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67491b3c08aa81e3ffc7d706f180fa9361772999367dd9bf8d40309d1f7befe`  
		Last Modified: Thu, 11 Jun 2026 03:02:29 GMT  
		Size: 39.2 MB (39217690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d230f4d88a954662423ef62595d6fcad5668b6cb3dfb9c100a31231da54857`  
		Last Modified: Thu, 11 Jun 2026 03:02:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223343b9f7a5ff99779445b1b4a073ce3175f42fe34198eef4148f105a7fd228`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 6.4 MB (6448164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b08ea2373cabdf05df4da7786a810af865963f98eed9f473ba4ee0c0aa631ba`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cf132b1b39c3e52d83989a6b52be0f7fc8726a1cc26fe78dfdc3e50eeb63ce`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce5b372c35d91a79642056162a37cfd0ee518457b74b9cd492cfb5220699ac2`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a47ddc3a3027055e40c8cfae8b782e0136290e14223aa8cd0359abf38ffa435f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1201b05cd4d2fa066dc6b4bf0c4f46f39f642509c778165f0dad04b2b975de`

```dockerfile
```

-	Layers:
	-	`sha256:d31301b16bbb97954f1849c6c10530d930e0669591ae97392a1287684e98acf8`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 2.3 MB (2283298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7265756a9f8219dfe82b262db584f0070f6617559d11880276c6a5e201b121fb`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-debian-1.0`

```console
$ docker pull fluentd@sha256:1e238cce77fbe4c957e7efda342faba1c19441db6bee4cba89e3610c6eb2bdd5
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

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v5

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

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v7

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

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.2-debian-1.0` - linux; arm64 variant v8

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

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.2-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:6475829b7644defa046da01f90644ec117e006c368e7ac87ada0befab5a5248b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76294002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7858c18ede6e8ab322771d1f42d6d8d3966f70b311c95e149a063fdef7df770`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:10:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 01:13:26 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 01:13:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:26 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:26 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:13:26 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:13:26 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 02:41:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 02:41:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 02:41:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 02:41:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 02:41:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 02:41:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 02:41:06 GMT
USER fluent
# Thu, 11 Jun 2026 02:41:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 02:41:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559b3beccacfe2507c7675689b3dcf322080300e5521890dbe4f42f508741680`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 1.3 MB (1287796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509d10f08039e48d3ade7bbe7dff9f8ee7ee76ef13f936e404824c8068446c1`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfedbe7d55d7141e3d1a588485f0412ed89261ab791f2535218e85ec39cca8d`  
		Last Modified: Thu, 11 Jun 2026 01:13:36 GMT  
		Size: 37.7 MB (37661759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ec848032e463e5e2f43d2446bedda0d5fa4791a14a5bb0c774cbb9859ee684`  
		Last Modified: Thu, 11 Jun 2026 01:13:35 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bcced4715bf20e33ddc912bddb71c911c1a2277865c382c6ff541e989c6b1e`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 6.0 MB (6040858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a514740bdb40ab9a6879bc860fdf279b03d5545529f34304f363dd8a014d2ce2`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96470ce34b035b1163c61af6fb9f6569c31cdd64812278ea7e18fd3b9b3cc4fc`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0dc96bea851f897f04bb4e7ccaabce918dad8900d0e7fcdf05dc7ba0b94a6c1`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:24b786d935282875dc6b7162dabf3073788072a892a0093df4c2fcba89ee83af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee2537f501fef0d86e5db0aa6af2c284368f3945c25cc54095ecdfab7135a73f`

```dockerfile
```

-	Layers:
	-	`sha256:25a31722ecad71526d5b03e0cf5da4798100a7f8758b7d3a583e378d2aa2442a`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 2.3 MB (2279041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bc518b644a1a3387e522fc15e481921ad250dfa9a2e186f0310b82ecddd10d`  
		Last Modified: Thu, 11 Jun 2026 02:41:13 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; ppc64le

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

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.2-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:20559f80aca1d03f9616c249daa8564ad7826db94e79a781b5383a8d9e2cffd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76814516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7fcf8c858da3b2c3a2fd1abddb0c7f6a696c6c6ff5a57e3aa061f203dd285d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:55:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:55:39 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 03:02:13 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 03:02:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 03:02:13 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 03:02:13 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:02:13 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 03:02:13 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 04:02:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 04:02:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 04:02:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 04:02:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 04:02:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 04:02:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 04:02:40 GMT
USER fluent
# Thu, 11 Jun 2026 04:02:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 04:02:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04b17d55015cef06ef07e9fb2fe3d7c817f54396d865c92c6a4fa5c4c9e9d0`  
		Last Modified: Thu, 11 Jun 2026 02:58:58 GMT  
		Size: 1.3 MB (1294918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d9c84bf624656635c57e41b1246f77049d77c0dd6fefa9dcd6322009a2d6c0`  
		Last Modified: Thu, 11 Jun 2026 02:58:58 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67491b3c08aa81e3ffc7d706f180fa9361772999367dd9bf8d40309d1f7befe`  
		Last Modified: Thu, 11 Jun 2026 03:02:29 GMT  
		Size: 39.2 MB (39217690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d230f4d88a954662423ef62595d6fcad5668b6cb3dfb9c100a31231da54857`  
		Last Modified: Thu, 11 Jun 2026 03:02:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223343b9f7a5ff99779445b1b4a073ce3175f42fe34198eef4148f105a7fd228`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 6.4 MB (6448164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b08ea2373cabdf05df4da7786a810af865963f98eed9f473ba4ee0c0aa631ba`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cf132b1b39c3e52d83989a6b52be0f7fc8726a1cc26fe78dfdc3e50eeb63ce`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce5b372c35d91a79642056162a37cfd0ee518457b74b9cd492cfb5220699ac2`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a47ddc3a3027055e40c8cfae8b782e0136290e14223aa8cd0359abf38ffa435f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1201b05cd4d2fa066dc6b4bf0c4f46f39f642509c778165f0dad04b2b975de`

```dockerfile
```

-	Layers:
	-	`sha256:d31301b16bbb97954f1849c6c10530d930e0669591ae97392a1287684e98acf8`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 2.3 MB (2283298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7265756a9f8219dfe82b262db584f0070f6617559d11880276c6a5e201b121fb`  
		Last Modified: Thu, 11 Jun 2026 04:02:53 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
