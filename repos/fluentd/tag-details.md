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
$ docker pull fluentd@sha256:258d58f1f0b1526c0a1a8717f0dfdc0ff0d6668f218fc534662d533a15817732
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
$ docker pull fluentd@sha256:8495296ad74c2ea22ba1725a364763711bca09d471bc815b6a08dcc8ad67a12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79168859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f939273aef8e879ecf96099370ccaed95b4c84e8e71a3c1b2cc60e833673fe`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:01:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:04:11 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:04:11 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:04:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:04:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:04:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:04:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:04:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:04:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:04:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:04:11 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:12:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:12:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:12:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:12:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:12:36 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:12:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:12:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:12:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:12:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:12:36 GMT
USER fluent
# Wed, 17 Dec 2025 20:12:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:12:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f28e2a679f348ab0f9c468a1aef4aded49ba5beb0cc9a090f8868f75027d01`  
		Last Modified: Wed, 17 Dec 2025 20:04:26 GMT  
		Size: 1.3 MB (1279406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cdb0c2a4fb8ab830daa5f6ac09f5e61745fcc39f1f45d1a1a8f421c2f75632`  
		Last Modified: Wed, 17 Dec 2025 20:04:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1def3d1b5dc0edc17c179a71ee5d84640d6969553fdefe09a4318a40d751f7e2`  
		Last Modified: Wed, 17 Dec 2025 20:04:33 GMT  
		Size: 42.1 MB (42111636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8afd0b495587d95b629c66296d5928f61cc4293a6f4f6511bd1e4c55682c29`  
		Last Modified: Wed, 17 Dec 2025 20:04:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be59c8a5638e2d1c6848f2231afd62a1e5cd64ccc8dde5bb59aaef4fd48c68a9`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 6.0 MB (5998926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20372393ff0183f26172e92d2b41f52c14aac3ce8f2eedf562cd3615d4400642`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4119d3f0a065f224b2ceebe85ad76ffa1608bca659930d9bf77d1a1c79c9390`  
		Last Modified: Wed, 17 Dec 2025 20:13:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f94cb0efadcd84fc1ffc51768559b6fe62f2479330aafe63e22b96225fb960`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:45b8d5df1941df9fc0a2a66beeb01c205b80026c0bec7f0d643d2dc8a5461ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea2d6717c91fe63b8b1fd99f3b2abe1bd0da4d2bf6a0a5fa74eb890522bafb2`

```dockerfile
```

-	Layers:
	-	`sha256:a7272e56985056523f2e53b70ea2e745aeb5b1b459a6112166b14b313dc20c02`  
		Last Modified: Wed, 17 Dec 2025 21:28:34 GMT  
		Size: 2.3 MB (2280105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9144a724cf0d217124e7a59312ea71e9f06931d86992e92d176078b7502e689`  
		Last Modified: Wed, 17 Dec 2025 21:28:35 GMT  
		Size: 21.3 KB (21326 bytes)  
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
$ docker pull fluentd@sha256:739dbcbfa05f96aadcd60cfadfa314b14d564a0f2533945164f58184b6577af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79464106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773ae6f56610778830eba984a23ef22017f727a2fb99109a16a4e1017ff09dbd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:01:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:04:18 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:04:18 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:04:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:04:18 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:04:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:04:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:04:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:04:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:04:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:04:19 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:13:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:13:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:13:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:13:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:13:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:13:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:13:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:13:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:13:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:13:00 GMT
USER fluent
# Wed, 17 Dec 2025 20:13:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:13:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a274e3264dd94560e27c435a9b374f6f3790f2d03d1153d7f889fb14e1e41e3`  
		Last Modified: Wed, 17 Dec 2025 20:04:37 GMT  
		Size: 1.3 MB (1261688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01dd05f50f9e9480f0cad1fcc9af1b79e690b6431dd980c621c4bf3942da408`  
		Last Modified: Wed, 17 Dec 2025 20:04:37 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11c0c27be43ccc82382e819239e7a5b431539347de9a5e3a1073416f1a6fcc6`  
		Last Modified: Wed, 17 Dec 2025 20:04:40 GMT  
		Size: 42.1 MB (42073138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656d61c6fc78b07e0e4f7a4e29dd5be1a7c40b0a498475de83dc93f755dd2acf`  
		Last Modified: Wed, 17 Dec 2025 20:04:36 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fda29affc29043134a687aee78c6227c034ca38effc72e19453d862b4de2e0d`  
		Last Modified: Wed, 17 Dec 2025 20:13:15 GMT  
		Size: 6.0 MB (5988256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9645739104fc10b773f6ffd98c58e46837ce5f8f2c3359291915200ddacb9a15`  
		Last Modified: Wed, 17 Dec 2025 20:13:15 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3e65def3e23e94aed93ec36f494846a73999cfaeb24cc105511de665c02a65`  
		Last Modified: Wed, 17 Dec 2025 20:13:15 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68d64b052e89a3e83e45414ab07458aa6b724dee6b1c8c20682faa6d050e4c8`  
		Last Modified: Wed, 17 Dec 2025 20:13:15 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:c87f3275b37c6e15f53456185a6d371e75710e38e3cd6773aaee84c6db9388f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d889ee092e4455603e394e0f39332db70a14bcb34e388e04395b45e03a9613c`

```dockerfile
```

-	Layers:
	-	`sha256:35d8a8f4b38dd8995d5a16bbf3418a6057844136f9e453f8f51eea272acb5389`  
		Last Modified: Wed, 17 Dec 2025 21:28:47 GMT  
		Size: 2.3 MB (2280377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07cb48bb94aa367e032bd8737da148daa4cbeb770c0b4baee3c6a06824f8658`  
		Last Modified: Wed, 17 Dec 2025 21:28:48 GMT  
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

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:e8fd955f960e48a709f48e51f047a6e72096cbaf4ef355e2f3a7b14793827f26
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
$ docker pull fluentd@sha256:dfed314058894234f76f3f87abd32b3cc486162c88cb4584f53c41ee65619084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82040178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502192d8aaeb86fbc9e5fde3da82f1b813eecad24d94a0da1b74af21ba0e3afb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:47:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:49:22 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:49:22 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 00:49:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 00:49:22 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 00:49:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:49:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:49:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:49:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:49:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:49:22 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 01:50:32 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 01:50:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 01:50:32 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 01:50:32 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 01:50:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 01:50:32 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 01:50:32 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 01:50:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 01:50:32 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 01:50:32 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 01:50:32 GMT
USER fluent
# Tue, 30 Dec 2025 01:50:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 01:50:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdc57904889217c8f0331318b3d24c3dbf235fe535edf8e2e73836b99679969`  
		Last Modified: Tue, 30 Dec 2025 00:49:39 GMT  
		Size: 3.5 MB (3509707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfab611350d463ece772d5f8dd961f0874536785bd07206733fe163ee785bfd`  
		Last Modified: Tue, 30 Dec 2025 00:49:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853a1cb5318ad089abb0784ad830f80a620dd9cf88b747c91db4b20b7a949c5f`  
		Last Modified: Tue, 30 Dec 2025 00:49:43 GMT  
		Size: 36.0 MB (36008166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f971dc91a875a9ea356df935b7d977e46b610c2e84794e7b5fc1179cd4d2279`  
		Last Modified: Tue, 30 Dec 2025 00:49:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c553e6052f348a874e07fca3f35ef33bda8e28017d4de7dc62f70579fd72c37b`  
		Last Modified: Tue, 30 Dec 2025 01:50:47 GMT  
		Size: 14.3 MB (14291490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57adf88d76ef4148bb342b470fdcfcbcc4794f016a79088618cbcb272f225a5`  
		Last Modified: Tue, 30 Dec 2025 01:50:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed7faf7efa7fa2bbe54ba0e6a97d3f96ad43a5ff448b4a6c5ed840570403698`  
		Last Modified: Tue, 30 Dec 2025 01:50:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3c0df5e72ee8aa3c1cf8f61a7e0f85d006bfb9dda93ecdee2be1162f85e362`  
		Last Modified: Tue, 30 Dec 2025 01:50:46 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:af976889483f50db5e7f67319229f70c55f7b32546676829029e7f1a518e7dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020bb29b746e2fa8ed2b9e23ee0c55628aeb7b07385d2910d9f0becb9982dd50`

```dockerfile
```

-	Layers:
	-	`sha256:ffabfd1721f2608e31042fc1f135466c8ba0259956450076978891944c5b4f0a`  
		Last Modified: Tue, 30 Dec 2025 03:29:58 GMT  
		Size: 2.7 MB (2671022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c8f9f7f85fc78b53216bb532f4bbc8171c96905c490a2fc4c042b8aacc28af4`  
		Last Modified: Tue, 30 Dec 2025 03:29:59 GMT  
		Size: 21.1 KB (21068 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:8d1bb367941c344b55d41de9833e24ef6fb2d1f3ab759ccb5b44565fdd1096ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75437356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696aefbb18a0d241ef6c87e16ab4d0123a5d81a3725c9e58a17f53ed9c69fa15`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:16:41 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:16:41 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 01:16:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 01:16:41 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 01:16:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:16:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:16:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:16:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:16:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:16:41 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 02:34:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 02:34:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 02:34:10 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 02:34:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 02:34:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 02:34:10 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 02:34:10 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 02:34:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 02:34:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 02:34:10 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 02:34:10 GMT
USER fluent
# Tue, 30 Dec 2025 02:34:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 02:34:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa8eb03a5eb5dc316e7d14f2cc3e1ac5fb3a475bec74d4d59bbc8009986997a`  
		Last Modified: Tue, 30 Dec 2025 01:16:56 GMT  
		Size: 3.1 MB (3079815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c84cec1d2a69d1b707673854472bdb4481a2f40b9234a607f80d9a3d7a8ee7`  
		Last Modified: Tue, 30 Dec 2025 01:16:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdded823509c9fa8e84064c1dd7d9425dbd644062010544cabe1d7cfb8b6477`  
		Last Modified: Tue, 30 Dec 2025 01:16:59 GMT  
		Size: 32.3 MB (32327459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f8ae75d3527b4ff18a47a14ae5014ef580ce159702b603a52e1db6d1f77393`  
		Last Modified: Tue, 30 Dec 2025 01:16:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7153ae236949f99a5f23d024b4af9588a4752d19f0a2c028d491c515000fef54`  
		Last Modified: Tue, 30 Dec 2025 02:34:25 GMT  
		Size: 14.3 MB (14270115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58e41f2b5aa924da576bd454ff567ec016bda810e29cafb2c408a62ed1a9097`  
		Last Modified: Tue, 30 Dec 2025 02:34:24 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fc72c9ad086fbe0cf622456b99aba1c97b50e132cb0d0aa6ff7dd702289400`  
		Last Modified: Tue, 30 Dec 2025 02:34:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6059db72fe2bbd5688f4ad2f676b776ca11f28cedc6c458fe589ecfdfdfc9e60`  
		Last Modified: Tue, 30 Dec 2025 02:34:24 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:83873a53ce95fa68056b634b1c2e3a75a2b7760e1bbdb0b057a78f0c57e539f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ede50262cf9d2ffc1d54ef5df2865989268b03cf8b0d879d595284525dc77a3`

```dockerfile
```

-	Layers:
	-	`sha256:72a8f558a76e183505434a20f35f2f29faab2299c2b9f5c028f249e1270a10b1`  
		Last Modified: Tue, 30 Dec 2025 03:30:06 GMT  
		Size: 2.7 MB (2674817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880c513827087f2588a95501e20ce14b671d2666a9ab4ef5cb958b7fad76148f`  
		Last Modified: Tue, 30 Dec 2025 03:30:07 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:159a43a9f877fc4fa8eff143fc79294c793919f980a7e03a1d42785ee88bb122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73209526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db918cb58eb45cfe8e8ed742d250e25666b4fe5a394387ef1b46fa676fe432ab`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:45:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:45:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:47:17 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:47:17 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 01:47:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 01:47:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 01:47:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:47:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:47:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:47:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:47:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:47:17 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 02:42:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 02:42:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 02:42:14 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 02:42:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 02:42:15 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 02:42:15 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 02:42:15 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 02:42:15 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 02:42:15 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 02:42:15 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 02:42:15 GMT
USER fluent
# Tue, 30 Dec 2025 02:42:15 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 02:42:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7b5dece593c8cbb29a37091a49cbcd13486bd61cd33d3ab360b403b7b84de3`  
		Last Modified: Tue, 30 Dec 2025 01:47:33 GMT  
		Size: 2.9 MB (2912747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb97ce5a95c82339bebf579a8181ce972cd84f66f1b06d8c58c0c3f25f32593`  
		Last Modified: Tue, 30 Dec 2025 01:47:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2131befd86e0cb6e898d6f2e1e3b2c38aab4e8e726f3944131b4c9b670fa67b`  
		Last Modified: Tue, 30 Dec 2025 01:47:34 GMT  
		Size: 32.2 MB (32161925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fdb606e7417b70421caa2627077ce7ccf1fc46a69aab2805b8baa4930b6df5`  
		Last Modified: Tue, 30 Dec 2025 01:47:32 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b46f6d1d512dec0295cd94b10b2b5c2813c9c8cb1c27b68d586711d1f76ac46`  
		Last Modified: Tue, 30 Dec 2025 02:42:31 GMT  
		Size: 14.2 MB (14198405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5a8edcc9b8a1fb7db2037dc54d0c9be49b261d6699bdfa03f4c74124857978`  
		Last Modified: Tue, 30 Dec 2025 02:42:30 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0fefa7ff933dab246af17e651c5dff76563c510a5f30a9d65ecf1c95736bf3`  
		Last Modified: Tue, 30 Dec 2025 02:42:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f07d831a6de7af64acb7f20158a131cae10e28cc2ec1586b7c22e4b157be773`  
		Last Modified: Tue, 30 Dec 2025 02:42:30 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e3f370581a617dc1d3d690893c911098451cb17ec2d867e56cfddc8affd9a6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1f56a258d22a966ee4690012e7a247e97c47890febdd4f3acaa50ecc131e2c`

```dockerfile
```

-	Layers:
	-	`sha256:63f42e11a4c890fb63befc759e1b935e203a8c126eb7cebc35224fe73e60d6a1`  
		Last Modified: Tue, 30 Dec 2025 03:30:11 GMT  
		Size: 2.7 MB (2673248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad74119b1105a6c341545581785c54becfa56243bbe725d43fc80c2218979af0`  
		Last Modified: Tue, 30 Dec 2025 03:30:12 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:b8f642218e2ae988f2331501e2bf6151a9f0fde7aaf00ac70db9b4192b39c6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81651964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e43e2c6ab4479ae58a96091743583a2e9aa56c6092bc9ba810cf6ac686a98a8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:50:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:52:29 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:52:29 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 00:52:29 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 00:52:29 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 00:52:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:52:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:52:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:52:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:52:29 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:52:29 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 01:51:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 01:51:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 01:51:55 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 01:51:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 01:51:56 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 01:51:56 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 01:51:56 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 01:51:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 01:51:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 01:51:56 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 01:51:56 GMT
USER fluent
# Tue, 30 Dec 2025 01:51:56 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 01:51:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae7c40900658b18d348bd2774604c46eca98d08ef1d45a1f985d0cbc1f4e5c6`  
		Last Modified: Tue, 30 Dec 2025 00:52:46 GMT  
		Size: 3.3 MB (3340664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f8d350e700bb8acd50f81d0a28cf15ef5b70d1c463bb7b91bd43220a39cc54`  
		Last Modified: Tue, 30 Dec 2025 00:52:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5617bc1baec7c56f0156f71e4e51a4864979dc850b678067e8d32ba855785a6c`  
		Last Modified: Tue, 30 Dec 2025 00:52:49 GMT  
		Size: 35.9 MB (35908942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dad51bbc72b51dc192dd58ed0f2cf9fa9cfc24d438b54790831864a1a607307`  
		Last Modified: Tue, 30 Dec 2025 00:52:45 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598a4c1af5657c7775ea48760514f0b26c70f0f11cd40080df1ff9b9aee02d2f`  
		Last Modified: Tue, 30 Dec 2025 01:52:13 GMT  
		Size: 14.3 MB (14297756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c671d9d2905a29e09509af1e6f96144c6039f918f431b598119b51d8273323`  
		Last Modified: Tue, 30 Dec 2025 01:52:12 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762165333180467ac9039f42ca7b5e76b4754e1d438baeffc516f04b07c75f5a`  
		Last Modified: Tue, 30 Dec 2025 01:52:12 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3710b91427c358e0f91140262554b9991aaade8e2e5c9f9840503ed6412ff96`  
		Last Modified: Tue, 30 Dec 2025 01:52:12 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a963bab7849684de366d147717eb1e1ae8b4792ac4175b408f5f96eec16d9892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457b3a5e3de0af9208a13ab26ffced4012d1f491b36e789fb49aba5a103a138d`

```dockerfile
```

-	Layers:
	-	`sha256:4bc65ce0daab08536bf9f713ad7204ffc1fcd323f7824d57c12bc124309d0fbb`  
		Last Modified: Tue, 30 Dec 2025 03:30:15 GMT  
		Size: 2.7 MB (2671262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe15d53723026abfd8f019f8626b1b11958c75415d9ef662b6cff794f4d4b01`  
		Last Modified: Tue, 30 Dec 2025 03:30:16 GMT  
		Size: 21.2 KB (21162 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:0b85c2dd76fc76d3aff8a8d96800d7ee85d83fc8bbcc23d81228992febbe9213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78964195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2ca30edc606da6621e20f23de24cb8ca9bd8d0618551495f4973dd147db3af`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:14:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:14:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:17:03 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:17:03 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 00:17:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 00:17:03 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 00:17:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:17:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:17:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:17:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:17:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:17:03 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 01:54:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 01:54:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 01:54:19 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 01:54:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 01:54:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 01:54:19 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 01:54:19 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 01:54:19 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 01:54:19 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 01:54:19 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 01:54:19 GMT
USER fluent
# Tue, 30 Dec 2025 01:54:19 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 01:54:19 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fbd368b46ddd6b63ad9ce6cee84be7b9ba182a72c7e222c298e3d8fcef7ebe`  
		Last Modified: Tue, 30 Dec 2025 00:17:20 GMT  
		Size: 3.5 MB (3510976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a03bd78cba1c0c4f9c767a5eb56c26010280a0812c10086c90f2836d0e0c21`  
		Last Modified: Tue, 30 Dec 2025 00:17:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855343f9fd97a631f9bcdb6cd5501b87a86b6ae39eb3c6ea6cbe92bdbf6d6ccc`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 32.2 MB (32160077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700247d907b673a939c55b9bc927d13dcfb318b76b7d7b3b4b546f0cc721bdfe`  
		Last Modified: Tue, 30 Dec 2025 00:17:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42b91cdc82adf815470f10a994a0a016fd5b5b7ca6d84525b91b5209e7fd33d`  
		Last Modified: Tue, 30 Dec 2025 01:54:37 GMT  
		Size: 14.1 MB (14080974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15be47c8a83256b9ed22d855d76f3771df0f9d121e8fdcfc90f0077b8d09b27`  
		Last Modified: Tue, 30 Dec 2025 01:54:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d314d22e0408c830265760c401298e032f0c9988c08b552784de7b65383b1e`  
		Last Modified: Tue, 30 Dec 2025 01:54:36 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7bb95e1360632ec238ffb528470ca2e319a47984dc3958a22997374d92f274`  
		Last Modified: Tue, 30 Dec 2025 01:54:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c97d12c1307a7039de223156faefc22fe52ee5b919f1d9b59e52bd29f0af8982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f441edef39256f0456fc64dbec53649bbdcf3eaac2efbdbbf511bf47e59fdb5`

```dockerfile
```

-	Layers:
	-	`sha256:7055aae267eaaf3bcb8e499083a5064fc147995011bbd3d1159eb14ca9fc30a6`  
		Last Modified: Tue, 30 Dec 2025 03:30:20 GMT  
		Size: 2.7 MB (2668201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d200137d696f79fd27d1504a159e12c7c85751d50dee14aa09933f2f9f6dfe60`  
		Last Modified: Tue, 30 Dec 2025 03:30:31 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8a048769e677e82292b628db670ab7901d10590f53376259849f230dec026398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84298646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430f3a82cce4612c1dfdc02ba440564ad0aac06b9a745cc0aa97cc7be3e3249e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:00:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 16:00:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:44:14 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:44:14 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:44:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:44:14 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:44:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:44:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:44:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:44:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:44:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:44:14 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:48:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:48:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:48:50 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:48:50 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:48:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:48:52 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:48:52 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:48:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:48:52 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:48:52 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:48:52 GMT
USER fluent
# Sun, 28 Dec 2025 05:48:52 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:48:52 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb227c51ebfc2a3295a101a484e244003b657ea6711f9e49c089462c924bd00`  
		Last Modified: Tue, 09 Dec 2025 16:05:23 GMT  
		Size: 3.7 MB (3709091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75eef6844398710a726e0ebacac5f7d288c26659a6e0c3cc9118a56c7353d82`  
		Last Modified: Tue, 09 Dec 2025 16:05:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3837c75f369fa8e6655ad22ce6f042f8b0d564e4a726971d216f9abc03153fcc`  
		Last Modified: Tue, 09 Dec 2025 20:44:46 GMT  
		Size: 33.8 MB (33832997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eced5f67d8b3a29b7adf1863b1050a2a249f5c72fc476e02b1f275b295ac95`  
		Last Modified: Tue, 09 Dec 2025 20:44:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb29e7df425870cf27a5187e07601132650c4b6882cc885edc7cdc212dd701a5`  
		Last Modified: Sun, 28 Dec 2025 05:49:15 GMT  
		Size: 14.7 MB (14685314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca335ae6d1f8e749af908fc6a024b654f96a4eb8d84ec280b525dd767361f26`  
		Last Modified: Sun, 28 Dec 2025 05:49:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d277bd583dee330be9d49a29602f370c36fd1f9e8661042aa9cea746b7e7ca`  
		Last Modified: Sun, 28 Dec 2025 05:49:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac344f93ff93514bcbdfe7c1fb92554c5a11fa1661cfaec2421cee3f77dc6e`  
		Last Modified: Sun, 28 Dec 2025 05:49:14 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5fbfba12a0a3bccc0f9ff040c3897e3f5d50d9cc80ce81bfe9c1d457c7ec663b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4acfc2b6da7ba1a66917f93bbf89245f39e8de021bacbc5ae0ee186d39f1bad`

```dockerfile
```

-	Layers:
	-	`sha256:29947c754de214f427787a9cc15d469ae7bcf7bde485dda903db8e97362f1632`  
		Last Modified: Sun, 28 Dec 2025 06:29:06 GMT  
		Size: 2.7 MB (2675439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756f2ddd8a0a073665ca119876ad7a9482e291713cde052bd3c12baa57127954`  
		Last Modified: Sun, 28 Dec 2025 06:29:07 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:7924a78c5b97f7c9a10d2bb3f75435853b4bafdb5c9072e67ae902b622260c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d50cf2f06ee540d4f2d48cc9707364cda815c3a236fa048754509c83a1a7f29`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:51:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:51:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:59:46 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:59:46 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 01:59:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 01:59:46 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 01:59:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:59:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:59:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:59:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:59:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:59:46 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 03:05:24 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 03:05:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 03:05:24 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 03:05:24 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 03:05:25 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 03:05:25 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 03:05:25 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 03:05:25 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 03:05:25 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 03:05:25 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 03:05:25 GMT
USER fluent
# Tue, 30 Dec 2025 03:05:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 03:05:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45ef165ffd3b0ee2e8c1c8b218540a111a56932a3cdb4b2dca3805537d5a23`  
		Last Modified: Tue, 30 Dec 2025 01:54:27 GMT  
		Size: 3.2 MB (3170327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fca4f8dd7e8bc459f3b31931b814f3dd67d3eba0ead6c52c08d03fe5885f6d4`  
		Last Modified: Tue, 30 Dec 2025 01:54:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83956e37af31ed691735a824abf11a19eb1e8ef47d3b3916bf546561e9d4459e`  
		Last Modified: Tue, 30 Dec 2025 02:00:16 GMT  
		Size: 33.1 MB (33099235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce817a6f503be53c3e17d4eeab19b64e281ed6c1057ae0919ee946de2bd7d4`  
		Last Modified: Tue, 30 Dec 2025 02:00:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b4847d27c018ddd9117a4ef5773270fbc07ccc299a793c6b54f2f927adf975`  
		Last Modified: Tue, 30 Dec 2025 03:05:43 GMT  
		Size: 14.4 MB (14426727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d772efecf7bb978daf7e77bf01d4f37cb4a05f20239afa4c1d5d85ea15f75f`  
		Last Modified: Tue, 30 Dec 2025 03:05:42 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227e7c2e88365abd3e1137b0c1ea901afd716817f0870271855c31dbe8e8d2b2`  
		Last Modified: Tue, 30 Dec 2025 03:05:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6000ded41b3e5b6d2ad83e28f72b5492aa74472d17621cd1e8ee338663e6f1fa`  
		Last Modified: Tue, 30 Dec 2025 03:05:42 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6faf5775edf15801dac9356e16f326d4dd0857c360455291b3a0d07b24f44b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b593630d043398f9ccbb8176bf1cebfb4be679ce043d3e69b42ec4b050bc1e`

```dockerfile
```

-	Layers:
	-	`sha256:a6a1bec6b413ad767f293cca343beddab4340497ce0d2c81ae10160aa923c9d9`  
		Last Modified: Tue, 30 Dec 2025 03:30:39 GMT  
		Size: 2.7 MB (2667847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a219b5dc19cc804f9a78ab3f4d08cf886d21d974c2172fc0a08e32982f4f757`  
		Last Modified: Tue, 30 Dec 2025 03:30:39 GMT  
		Size: 21.1 KB (21068 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.11-debian-1.0`

```console
$ docker pull fluentd@sha256:e8fd955f960e48a709f48e51f047a6e72096cbaf4ef355e2f3a7b14793827f26
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
$ docker pull fluentd@sha256:dfed314058894234f76f3f87abd32b3cc486162c88cb4584f53c41ee65619084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82040178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502192d8aaeb86fbc9e5fde3da82f1b813eecad24d94a0da1b74af21ba0e3afb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:47:02 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:49:22 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:49:22 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 00:49:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 00:49:22 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 00:49:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:49:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:49:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:49:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:49:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:49:22 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 01:50:32 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 01:50:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 01:50:32 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 01:50:32 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 01:50:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 01:50:32 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 01:50:32 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 01:50:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 01:50:32 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 01:50:32 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 01:50:32 GMT
USER fluent
# Tue, 30 Dec 2025 01:50:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 01:50:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdc57904889217c8f0331318b3d24c3dbf235fe535edf8e2e73836b99679969`  
		Last Modified: Tue, 30 Dec 2025 00:49:39 GMT  
		Size: 3.5 MB (3509707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdfab611350d463ece772d5f8dd961f0874536785bd07206733fe163ee785bfd`  
		Last Modified: Tue, 30 Dec 2025 00:49:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853a1cb5318ad089abb0784ad830f80a620dd9cf88b747c91db4b20b7a949c5f`  
		Last Modified: Tue, 30 Dec 2025 00:49:43 GMT  
		Size: 36.0 MB (36008166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f971dc91a875a9ea356df935b7d977e46b610c2e84794e7b5fc1179cd4d2279`  
		Last Modified: Tue, 30 Dec 2025 00:49:48 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c553e6052f348a874e07fca3f35ef33bda8e28017d4de7dc62f70579fd72c37b`  
		Last Modified: Tue, 30 Dec 2025 01:50:47 GMT  
		Size: 14.3 MB (14291490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57adf88d76ef4148bb342b470fdcfcbcc4794f016a79088618cbcb272f225a5`  
		Last Modified: Tue, 30 Dec 2025 01:50:46 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed7faf7efa7fa2bbe54ba0e6a97d3f96ad43a5ff448b4a6c5ed840570403698`  
		Last Modified: Tue, 30 Dec 2025 01:50:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3c0df5e72ee8aa3c1cf8f61a7e0f85d006bfb9dda93ecdee2be1162f85e362`  
		Last Modified: Tue, 30 Dec 2025 01:50:46 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:af976889483f50db5e7f67319229f70c55f7b32546676829029e7f1a518e7dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020bb29b746e2fa8ed2b9e23ee0c55628aeb7b07385d2910d9f0becb9982dd50`

```dockerfile
```

-	Layers:
	-	`sha256:ffabfd1721f2608e31042fc1f135466c8ba0259956450076978891944c5b4f0a`  
		Last Modified: Tue, 30 Dec 2025 03:29:58 GMT  
		Size: 2.7 MB (2671022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c8f9f7f85fc78b53216bb532f4bbc8171c96905c490a2fc4c042b8aacc28af4`  
		Last Modified: Tue, 30 Dec 2025 03:29:59 GMT  
		Size: 21.1 KB (21068 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:8d1bb367941c344b55d41de9833e24ef6fb2d1f3ab759ccb5b44565fdd1096ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75437356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696aefbb18a0d241ef6c87e16ab4d0123a5d81a3725c9e58a17f53ed9c69fa15`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:14:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:14:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:16:41 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:16:41 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 01:16:41 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 01:16:41 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 01:16:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:16:41 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:16:41 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:16:41 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:16:41 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:16:41 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 02:34:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 02:34:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 02:34:10 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 02:34:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 02:34:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 02:34:10 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 02:34:10 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 02:34:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 02:34:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 02:34:10 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 02:34:10 GMT
USER fluent
# Tue, 30 Dec 2025 02:34:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 02:34:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa8eb03a5eb5dc316e7d14f2cc3e1ac5fb3a475bec74d4d59bbc8009986997a`  
		Last Modified: Tue, 30 Dec 2025 01:16:56 GMT  
		Size: 3.1 MB (3079815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c84cec1d2a69d1b707673854472bdb4481a2f40b9234a607f80d9a3d7a8ee7`  
		Last Modified: Tue, 30 Dec 2025 01:16:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdded823509c9fa8e84064c1dd7d9425dbd644062010544cabe1d7cfb8b6477`  
		Last Modified: Tue, 30 Dec 2025 01:16:59 GMT  
		Size: 32.3 MB (32327459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f8ae75d3527b4ff18a47a14ae5014ef580ce159702b603a52e1db6d1f77393`  
		Last Modified: Tue, 30 Dec 2025 01:16:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7153ae236949f99a5f23d024b4af9588a4752d19f0a2c028d491c515000fef54`  
		Last Modified: Tue, 30 Dec 2025 02:34:25 GMT  
		Size: 14.3 MB (14270115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58e41f2b5aa924da576bd454ff567ec016bda810e29cafb2c408a62ed1a9097`  
		Last Modified: Tue, 30 Dec 2025 02:34:24 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fc72c9ad086fbe0cf622456b99aba1c97b50e132cb0d0aa6ff7dd702289400`  
		Last Modified: Tue, 30 Dec 2025 02:34:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6059db72fe2bbd5688f4ad2f676b776ca11f28cedc6c458fe589ecfdfdfc9e60`  
		Last Modified: Tue, 30 Dec 2025 02:34:24 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:83873a53ce95fa68056b634b1c2e3a75a2b7760e1bbdb0b057a78f0c57e539f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ede50262cf9d2ffc1d54ef5df2865989268b03cf8b0d879d595284525dc77a3`

```dockerfile
```

-	Layers:
	-	`sha256:72a8f558a76e183505434a20f35f2f29faab2299c2b9f5c028f249e1270a10b1`  
		Last Modified: Tue, 30 Dec 2025 03:30:06 GMT  
		Size: 2.7 MB (2674817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880c513827087f2588a95501e20ce14b671d2666a9ab4ef5cb958b7fad76148f`  
		Last Modified: Tue, 30 Dec 2025 03:30:07 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:159a43a9f877fc4fa8eff143fc79294c793919f980a7e03a1d42785ee88bb122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73209526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db918cb58eb45cfe8e8ed742d250e25666b4fe5a394387ef1b46fa676fe432ab`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:45:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:45:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:47:17 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:47:17 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 01:47:17 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 01:47:17 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 01:47:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:47:17 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:47:17 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:47:17 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:47:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:47:17 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 02:42:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 02:42:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 02:42:14 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 02:42:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 02:42:15 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 02:42:15 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 02:42:15 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 02:42:15 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 02:42:15 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 02:42:15 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 02:42:15 GMT
USER fluent
# Tue, 30 Dec 2025 02:42:15 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 02:42:15 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7b5dece593c8cbb29a37091a49cbcd13486bd61cd33d3ab360b403b7b84de3`  
		Last Modified: Tue, 30 Dec 2025 01:47:33 GMT  
		Size: 2.9 MB (2912747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb97ce5a95c82339bebf579a8181ce972cd84f66f1b06d8c58c0c3f25f32593`  
		Last Modified: Tue, 30 Dec 2025 01:47:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2131befd86e0cb6e898d6f2e1e3b2c38aab4e8e726f3944131b4c9b670fa67b`  
		Last Modified: Tue, 30 Dec 2025 01:47:34 GMT  
		Size: 32.2 MB (32161925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fdb606e7417b70421caa2627077ce7ccf1fc46a69aab2805b8baa4930b6df5`  
		Last Modified: Tue, 30 Dec 2025 01:47:32 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b46f6d1d512dec0295cd94b10b2b5c2813c9c8cb1c27b68d586711d1f76ac46`  
		Last Modified: Tue, 30 Dec 2025 02:42:31 GMT  
		Size: 14.2 MB (14198405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5a8edcc9b8a1fb7db2037dc54d0c9be49b261d6699bdfa03f4c74124857978`  
		Last Modified: Tue, 30 Dec 2025 02:42:30 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0fefa7ff933dab246af17e651c5dff76563c510a5f30a9d65ecf1c95736bf3`  
		Last Modified: Tue, 30 Dec 2025 02:42:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f07d831a6de7af64acb7f20158a131cae10e28cc2ec1586b7c22e4b157be773`  
		Last Modified: Tue, 30 Dec 2025 02:42:30 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e3f370581a617dc1d3d690893c911098451cb17ec2d867e56cfddc8affd9a6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1f56a258d22a966ee4690012e7a247e97c47890febdd4f3acaa50ecc131e2c`

```dockerfile
```

-	Layers:
	-	`sha256:63f42e11a4c890fb63befc759e1b935e203a8c126eb7cebc35224fe73e60d6a1`  
		Last Modified: Tue, 30 Dec 2025 03:30:11 GMT  
		Size: 2.7 MB (2673248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad74119b1105a6c341545581785c54becfa56243bbe725d43fc80c2218979af0`  
		Last Modified: Tue, 30 Dec 2025 03:30:12 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:b8f642218e2ae988f2331501e2bf6151a9f0fde7aaf00ac70db9b4192b39c6a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81651964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e43e2c6ab4479ae58a96091743583a2e9aa56c6092bc9ba810cf6ac686a98a8`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:50:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:50:24 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:52:29 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:52:29 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 00:52:29 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 00:52:29 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 00:52:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:52:29 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:52:29 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:52:29 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:52:29 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:52:29 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 01:51:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 01:51:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 01:51:55 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 01:51:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 01:51:56 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 01:51:56 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 01:51:56 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 01:51:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 01:51:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 01:51:56 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 01:51:56 GMT
USER fluent
# Tue, 30 Dec 2025 01:51:56 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 01:51:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae7c40900658b18d348bd2774604c46eca98d08ef1d45a1f985d0cbc1f4e5c6`  
		Last Modified: Tue, 30 Dec 2025 00:52:46 GMT  
		Size: 3.3 MB (3340664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f8d350e700bb8acd50f81d0a28cf15ef5b70d1c463bb7b91bd43220a39cc54`  
		Last Modified: Tue, 30 Dec 2025 00:52:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5617bc1baec7c56f0156f71e4e51a4864979dc850b678067e8d32ba855785a6c`  
		Last Modified: Tue, 30 Dec 2025 00:52:49 GMT  
		Size: 35.9 MB (35908942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dad51bbc72b51dc192dd58ed0f2cf9fa9cfc24d438b54790831864a1a607307`  
		Last Modified: Tue, 30 Dec 2025 00:52:45 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:598a4c1af5657c7775ea48760514f0b26c70f0f11cd40080df1ff9b9aee02d2f`  
		Last Modified: Tue, 30 Dec 2025 01:52:13 GMT  
		Size: 14.3 MB (14297756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c671d9d2905a29e09509af1e6f96144c6039f918f431b598119b51d8273323`  
		Last Modified: Tue, 30 Dec 2025 01:52:12 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762165333180467ac9039f42ca7b5e76b4754e1d438baeffc516f04b07c75f5a`  
		Last Modified: Tue, 30 Dec 2025 01:52:12 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3710b91427c358e0f91140262554b9991aaade8e2e5c9f9840503ed6412ff96`  
		Last Modified: Tue, 30 Dec 2025 01:52:12 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a963bab7849684de366d147717eb1e1ae8b4792ac4175b408f5f96eec16d9892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457b3a5e3de0af9208a13ab26ffced4012d1f491b36e789fb49aba5a103a138d`

```dockerfile
```

-	Layers:
	-	`sha256:4bc65ce0daab08536bf9f713ad7204ffc1fcd323f7824d57c12bc124309d0fbb`  
		Last Modified: Tue, 30 Dec 2025 03:30:15 GMT  
		Size: 2.7 MB (2671262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fe15d53723026abfd8f019f8626b1b11958c75415d9ef662b6cff794f4d4b01`  
		Last Modified: Tue, 30 Dec 2025 03:30:16 GMT  
		Size: 21.2 KB (21162 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:0b85c2dd76fc76d3aff8a8d96800d7ee85d83fc8bbcc23d81228992febbe9213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78964195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2ca30edc606da6621e20f23de24cb8ca9bd8d0618551495f4973dd147db3af`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:14:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:14:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 00:17:03 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 00:17:03 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 00:17:03 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 00:17:03 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 00:17:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 00:17:03 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 00:17:03 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 00:17:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:17:03 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 00:17:03 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 01:54:19 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 01:54:19 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 01:54:19 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 01:54:19 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 01:54:19 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 01:54:19 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 01:54:19 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 01:54:19 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 01:54:19 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 01:54:19 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 01:54:19 GMT
USER fluent
# Tue, 30 Dec 2025 01:54:19 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 01:54:19 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fbd368b46ddd6b63ad9ce6cee84be7b9ba182a72c7e222c298e3d8fcef7ebe`  
		Last Modified: Tue, 30 Dec 2025 00:17:20 GMT  
		Size: 3.5 MB (3510976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a03bd78cba1c0c4f9c767a5eb56c26010280a0812c10086c90f2836d0e0c21`  
		Last Modified: Tue, 30 Dec 2025 00:17:20 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855343f9fd97a631f9bcdb6cd5501b87a86b6ae39eb3c6ea6cbe92bdbf6d6ccc`  
		Last Modified: Tue, 30 Dec 2025 00:17:22 GMT  
		Size: 32.2 MB (32160077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700247d907b673a939c55b9bc927d13dcfb318b76b7d7b3b4b546f0cc721bdfe`  
		Last Modified: Tue, 30 Dec 2025 00:17:18 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42b91cdc82adf815470f10a994a0a016fd5b5b7ca6d84525b91b5209e7fd33d`  
		Last Modified: Tue, 30 Dec 2025 01:54:37 GMT  
		Size: 14.1 MB (14080974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15be47c8a83256b9ed22d855d76f3771df0f9d121e8fdcfc90f0077b8d09b27`  
		Last Modified: Tue, 30 Dec 2025 01:54:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d314d22e0408c830265760c401298e032f0c9988c08b552784de7b65383b1e`  
		Last Modified: Tue, 30 Dec 2025 01:54:36 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7bb95e1360632ec238ffb528470ca2e319a47984dc3958a22997374d92f274`  
		Last Modified: Tue, 30 Dec 2025 01:54:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c97d12c1307a7039de223156faefc22fe52ee5b919f1d9b59e52bd29f0af8982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f441edef39256f0456fc64dbec53649bbdcf3eaac2efbdbbf511bf47e59fdb5`

```dockerfile
```

-	Layers:
	-	`sha256:7055aae267eaaf3bcb8e499083a5064fc147995011bbd3d1159eb14ca9fc30a6`  
		Last Modified: Tue, 30 Dec 2025 03:30:20 GMT  
		Size: 2.7 MB (2668201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d200137d696f79fd27d1504a159e12c7c85751d50dee14aa09933f2f9f6dfe60`  
		Last Modified: Tue, 30 Dec 2025 03:30:31 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8a048769e677e82292b628db670ab7901d10590f53376259849f230dec026398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84298646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430f3a82cce4612c1dfdc02ba440564ad0aac06b9a745cc0aa97cc7be3e3249e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:00:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 16:00:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:44:14 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:44:14 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:44:14 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:44:14 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:44:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:44:14 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:44:14 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:44:14 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:44:14 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:44:14 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:48:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:48:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:48:50 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:48:50 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:48:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:48:52 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:48:52 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:48:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:48:52 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:48:52 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:48:52 GMT
USER fluent
# Sun, 28 Dec 2025 05:48:52 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:48:52 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb227c51ebfc2a3295a101a484e244003b657ea6711f9e49c089462c924bd00`  
		Last Modified: Tue, 09 Dec 2025 16:05:23 GMT  
		Size: 3.7 MB (3709091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75eef6844398710a726e0ebacac5f7d288c26659a6e0c3cc9118a56c7353d82`  
		Last Modified: Tue, 09 Dec 2025 16:05:22 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3837c75f369fa8e6655ad22ce6f042f8b0d564e4a726971d216f9abc03153fcc`  
		Last Modified: Tue, 09 Dec 2025 20:44:46 GMT  
		Size: 33.8 MB (33832997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4eced5f67d8b3a29b7adf1863b1050a2a249f5c72fc476e02b1f275b295ac95`  
		Last Modified: Tue, 09 Dec 2025 20:44:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb29e7df425870cf27a5187e07601132650c4b6882cc885edc7cdc212dd701a5`  
		Last Modified: Sun, 28 Dec 2025 05:49:15 GMT  
		Size: 14.7 MB (14685314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca335ae6d1f8e749af908fc6a024b654f96a4eb8d84ec280b525dd767361f26`  
		Last Modified: Sun, 28 Dec 2025 05:49:14 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d277bd583dee330be9d49a29602f370c36fd1f9e8661042aa9cea746b7e7ca`  
		Last Modified: Sun, 28 Dec 2025 05:49:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac344f93ff93514bcbdfe7c1fb92554c5a11fa1661cfaec2421cee3f77dc6e`  
		Last Modified: Sun, 28 Dec 2025 05:49:14 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5fbfba12a0a3bccc0f9ff040c3897e3f5d50d9cc80ce81bfe9c1d457c7ec663b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4acfc2b6da7ba1a66917f93bbf89245f39e8de021bacbc5ae0ee186d39f1bad`

```dockerfile
```

-	Layers:
	-	`sha256:29947c754de214f427787a9cc15d469ae7bcf7bde485dda903db8e97362f1632`  
		Last Modified: Sun, 28 Dec 2025 06:29:06 GMT  
		Size: 2.7 MB (2675439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756f2ddd8a0a073665ca119876ad7a9482e291713cde052bd3c12baa57127954`  
		Last Modified: Sun, 28 Dec 2025 06:29:07 GMT  
		Size: 21.1 KB (21102 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:7924a78c5b97f7c9a10d2bb3f75435853b4bafdb5c9072e67ae902b622260c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d50cf2f06ee540d4f2d48cc9707364cda815c3a236fa048754509c83a1a7f29`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:51:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 01:51:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 30 Dec 2025 01:59:46 GMT
ENV LANG=C.UTF-8
# Tue, 30 Dec 2025 01:59:46 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 30 Dec 2025 01:59:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 30 Dec 2025 01:59:46 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 30 Dec 2025 01:59:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 30 Dec 2025 01:59:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 30 Dec 2025 01:59:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 30 Dec 2025 01:59:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:59:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 30 Dec 2025 01:59:46 GMT
CMD ["irb"]
# Tue, 30 Dec 2025 03:05:24 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 30 Dec 2025 03:05:24 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 30 Dec 2025 03:05:24 GMT
ENV TINI_VERSION=0.18.0
# Tue, 30 Dec 2025 03:05:24 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 30 Dec 2025 03:05:25 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 30 Dec 2025 03:05:25 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 30 Dec 2025 03:05:25 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 30 Dec 2025 03:05:25 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 30 Dec 2025 03:05:25 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 30 Dec 2025 03:05:25 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 30 Dec 2025 03:05:25 GMT
USER fluent
# Tue, 30 Dec 2025 03:05:25 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 30 Dec 2025 03:05:25 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45ef165ffd3b0ee2e8c1c8b218540a111a56932a3cdb4b2dca3805537d5a23`  
		Last Modified: Tue, 30 Dec 2025 01:54:27 GMT  
		Size: 3.2 MB (3170327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fca4f8dd7e8bc459f3b31931b814f3dd67d3eba0ead6c52c08d03fe5885f6d4`  
		Last Modified: Tue, 30 Dec 2025 01:54:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83956e37af31ed691735a824abf11a19eb1e8ef47d3b3916bf546561e9d4459e`  
		Last Modified: Tue, 30 Dec 2025 02:00:16 GMT  
		Size: 33.1 MB (33099235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce817a6f503be53c3e17d4eeab19b64e281ed6c1057ae0919ee946de2bd7d4`  
		Last Modified: Tue, 30 Dec 2025 02:00:13 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b4847d27c018ddd9117a4ef5773270fbc07ccc299a793c6b54f2f927adf975`  
		Last Modified: Tue, 30 Dec 2025 03:05:43 GMT  
		Size: 14.4 MB (14426727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d772efecf7bb978daf7e77bf01d4f37cb4a05f20239afa4c1d5d85ea15f75f`  
		Last Modified: Tue, 30 Dec 2025 03:05:42 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227e7c2e88365abd3e1137b0c1ea901afd716817f0870271855c31dbe8e8d2b2`  
		Last Modified: Tue, 30 Dec 2025 03:05:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6000ded41b3e5b6d2ad83e28f72b5492aa74472d17621cd1e8ee338663e6f1fa`  
		Last Modified: Tue, 30 Dec 2025 03:05:42 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6faf5775edf15801dac9356e16f326d4dd0857c360455291b3a0d07b24f44b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b593630d043398f9ccbb8176bf1cebfb4be679ce043d3e69b42ec4b050bc1e`

```dockerfile
```

-	Layers:
	-	`sha256:a6a1bec6b413ad767f293cca343beddab4340497ce0d2c81ae10160aa923c9d9`  
		Last Modified: Tue, 30 Dec 2025 03:30:39 GMT  
		Size: 2.7 MB (2667847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a219b5dc19cc804f9a78ab3f4d08cf886d21d974c2172fc0a08e32982f4f757`  
		Last Modified: Tue, 30 Dec 2025 03:30:39 GMT  
		Size: 21.1 KB (21068 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:258d58f1f0b1526c0a1a8717f0dfdc0ff0d6668f218fc534662d533a15817732
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
$ docker pull fluentd@sha256:8495296ad74c2ea22ba1725a364763711bca09d471bc815b6a08dcc8ad67a12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79168859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3f939273aef8e879ecf96099370ccaed95b4c84e8e71a3c1b2cc60e833673fe`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:01:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:04:11 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:04:11 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:04:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:04:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:04:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:04:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:04:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:04:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:04:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:04:11 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:12:36 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:12:36 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:12:36 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:12:36 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:12:36 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:12:36 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:12:36 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:12:36 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:12:36 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:12:36 GMT
USER fluent
# Wed, 17 Dec 2025 20:12:36 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:12:36 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f28e2a679f348ab0f9c468a1aef4aded49ba5beb0cc9a090f8868f75027d01`  
		Last Modified: Wed, 17 Dec 2025 20:04:26 GMT  
		Size: 1.3 MB (1279406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cdb0c2a4fb8ab830daa5f6ac09f5e61745fcc39f1f45d1a1a8f421c2f75632`  
		Last Modified: Wed, 17 Dec 2025 20:04:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1def3d1b5dc0edc17c179a71ee5d84640d6969553fdefe09a4318a40d751f7e2`  
		Last Modified: Wed, 17 Dec 2025 20:04:33 GMT  
		Size: 42.1 MB (42111636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8afd0b495587d95b629c66296d5928f61cc4293a6f4f6511bd1e4c55682c29`  
		Last Modified: Wed, 17 Dec 2025 20:04:26 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be59c8a5638e2d1c6848f2231afd62a1e5cd64ccc8dde5bb59aaef4fd48c68a9`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 6.0 MB (5998926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20372393ff0183f26172e92d2b41f52c14aac3ce8f2eedf562cd3615d4400642`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4119d3f0a065f224b2ceebe85ad76ffa1608bca659930d9bf77d1a1c79c9390`  
		Last Modified: Wed, 17 Dec 2025 20:13:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f94cb0efadcd84fc1ffc51768559b6fe62f2479330aafe63e22b96225fb960`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:45b8d5df1941df9fc0a2a66beeb01c205b80026c0bec7f0d643d2dc8a5461ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea2d6717c91fe63b8b1fd99f3b2abe1bd0da4d2bf6a0a5fa74eb890522bafb2`

```dockerfile
```

-	Layers:
	-	`sha256:a7272e56985056523f2e53b70ea2e745aeb5b1b459a6112166b14b313dc20c02`  
		Last Modified: Wed, 17 Dec 2025 21:28:34 GMT  
		Size: 2.3 MB (2280105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9144a724cf0d217124e7a59312ea71e9f06931d86992e92d176078b7502e689`  
		Last Modified: Wed, 17 Dec 2025 21:28:35 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

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

### `fluentd:v1.19-1` - unknown; unknown

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

### `fluentd:v1.19-1` - linux; arm variant v7

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

### `fluentd:v1.19-1` - unknown; unknown

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

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:739dbcbfa05f96aadcd60cfadfa314b14d564a0f2533945164f58184b6577af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79464106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773ae6f56610778830eba984a23ef22017f727a2fb99109a16a4e1017ff09dbd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:01:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:01:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:04:18 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:04:18 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:04:18 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:04:18 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:04:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:04:18 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:04:18 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:04:18 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:04:19 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:04:19 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:13:00 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:13:00 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:13:00 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:13:00 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:13:00 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:13:00 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:13:00 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:13:00 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:13:00 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:13:00 GMT
USER fluent
# Wed, 17 Dec 2025 20:13:00 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:13:00 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a274e3264dd94560e27c435a9b374f6f3790f2d03d1153d7f889fb14e1e41e3`  
		Last Modified: Wed, 17 Dec 2025 20:04:37 GMT  
		Size: 1.3 MB (1261688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01dd05f50f9e9480f0cad1fcc9af1b79e690b6431dd980c621c4bf3942da408`  
		Last Modified: Wed, 17 Dec 2025 20:04:37 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11c0c27be43ccc82382e819239e7a5b431539347de9a5e3a1073416f1a6fcc6`  
		Last Modified: Wed, 17 Dec 2025 20:04:40 GMT  
		Size: 42.1 MB (42073138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656d61c6fc78b07e0e4f7a4e29dd5be1a7c40b0a498475de83dc93f755dd2acf`  
		Last Modified: Wed, 17 Dec 2025 20:04:36 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fda29affc29043134a687aee78c6227c034ca38effc72e19453d862b4de2e0d`  
		Last Modified: Wed, 17 Dec 2025 20:13:15 GMT  
		Size: 6.0 MB (5988256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9645739104fc10b773f6ffd98c58e46837ce5f8f2c3359291915200ddacb9a15`  
		Last Modified: Wed, 17 Dec 2025 20:13:15 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3e65def3e23e94aed93ec36f494846a73999cfaeb24cc105511de665c02a65`  
		Last Modified: Wed, 17 Dec 2025 20:13:15 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68d64b052e89a3e83e45414ab07458aa6b724dee6b1c8c20682faa6d050e4c8`  
		Last Modified: Wed, 17 Dec 2025 20:13:15 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c87f3275b37c6e15f53456185a6d371e75710e38e3cd6773aaee84c6db9388f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d889ee092e4455603e394e0f39332db70a14bcb34e388e04395b45e03a9613c`

```dockerfile
```

-	Layers:
	-	`sha256:35d8a8f4b38dd8995d5a16bbf3418a6057844136f9e453f8f51eea272acb5389`  
		Last Modified: Wed, 17 Dec 2025 21:28:47 GMT  
		Size: 2.3 MB (2280377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07cb48bb94aa367e032bd8737da148daa4cbeb770c0b4baee3c6a06824f8658`  
		Last Modified: Wed, 17 Dec 2025 21:28:48 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

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

### `fluentd:v1.19-1` - unknown; unknown

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

### `fluentd:v1.19-1` - linux; ppc64le

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

### `fluentd:v1.19-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; amd64

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; arm variant v5

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; arm variant v7

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; 386

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; ppc64le

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19.0-1.0` - linux; amd64

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

### `fluentd:v1.19.0-1.0` - unknown; unknown

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

### `fluentd:v1.19.0-1.0` - linux; arm variant v5

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

### `fluentd:v1.19.0-1.0` - unknown; unknown

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

### `fluentd:v1.19.0-1.0` - linux; arm variant v7

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

### `fluentd:v1.19.0-1.0` - unknown; unknown

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

### `fluentd:v1.19.0-1.0` - linux; arm64 variant v8

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

### `fluentd:v1.19.0-1.0` - unknown; unknown

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

### `fluentd:v1.19.0-1.0` - linux; 386

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

### `fluentd:v1.19.0-1.0` - unknown; unknown

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

### `fluentd:v1.19.0-1.0` - linux; ppc64le

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

### `fluentd:v1.19.0-1.0` - unknown; unknown

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

### `fluentd:v1.19.1-debian-1.0` - linux; amd64

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

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.1-debian-1.0` - linux; arm variant v5

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

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.1-debian-1.0` - linux; arm variant v7

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

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.1-debian-1.0` - linux; arm64 variant v8

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

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.1-debian-1.0` - linux; 386

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

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.1-debian-1.0` - linux; ppc64le

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

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

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
