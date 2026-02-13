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
$ docker pull fluentd@sha256:271bf34fe9ded0e997f03d0e68913ff78aeb89568060083887a6650cdb4537ad
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
$ docker pull fluentd@sha256:45c609aa35a6efbbf7ba404bb177c4a99beafcf726b35af540630df793f0229c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79177985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3742aea87a869860fd82d04ba4e0f2679c87240dbd6cb0ae997cf0bf5660a797`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:13:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:13:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:15:56 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:15:56 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:15:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:15:56 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:15:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:15:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:15:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:15:56 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:26:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:26:07 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:26:07 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:26:08 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:26:08 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:26:08 GMT
USER fluent
# Tue, 03 Feb 2026 04:26:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:26:08 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd62801a76356b1b2a4bd7d0e0af507d64d67295bb586f272377f03f69211cb`  
		Last Modified: Tue, 03 Feb 2026 03:16:06 GMT  
		Size: 1.3 MB (1279351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559eac235c75feecce250b6f5bf2035a78c5d732256b9803c22f73f5fab57c4`  
		Last Modified: Tue, 03 Feb 2026 03:16:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80098ee487838645ca286b994643ee6cd611bfde9dd33e14009a0cb6111d368f`  
		Last Modified: Tue, 03 Feb 2026 03:16:07 GMT  
		Size: 42.1 MB (42112727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f5098c7eff479e8cf2942ce700947554a5460f03a9c982c9a0c7971ed8e830`  
		Last Modified: Tue, 03 Feb 2026 03:16:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64f9e55a08318c5b342595d089796c90c4ea9709834ccdb0c62a668dd6ded4`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 6.0 MB (6004917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ba26a50d4e36f5948e8e96b92fe65b04b6453629121b5c4884c9628c0b85ae`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073b4135eb33889189bc6c314c38ac61829dae1bf884092fbd5f27cfd2c8db1d`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2b7869fc658a75615a950a30320230d90acba798b6e51f0a93cecf18077a81`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:ebef43c47a752172b97918a1a5f174058a98c9377883163bed7c8c5e953780e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42803b2651c6d9f54ecec768e7b60ef379c0af1f3d20bf483d6b980e2b856353`

```dockerfile
```

-	Layers:
	-	`sha256:c37f44765165c6e318ddd053d9fbcba71f602ba78c7418b30ccea04294084872`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 2.3 MB (2280193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa5c2b07161651b899a277dc1fd27269aaad60f8cea33acd8f5cfbf9acfa8d6`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
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
$ docker pull fluentd@sha256:ed1f60c202bd2fd7d98b1cbafc3ce6b37b52247d52a8a9e99ae4fc5e292b82e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70894341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bbd347cae3af93c81731a0e5fa643bc53a41f5db36f63c5da866f110fa8c69`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:37:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:39:47 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:39:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:39:47 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:39:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:39:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:39:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:39:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:39:47 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:25:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:25:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 05:25:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:25:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:25:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:25:42 GMT
USER fluent
# Tue, 03 Feb 2026 05:25:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:25:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b80b6adb1ac78286c039e72a54aa2f5853d41b835f2b869690c3949c3d00d1d`  
		Last Modified: Tue, 03 Feb 2026 04:39:56 GMT  
		Size: 1.2 MB (1236625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f91969b4a8b878ca7237b13f3af6a5a1eca4dfb8f3119c7e9108f5f6b1f1dc7`  
		Last Modified: Tue, 03 Feb 2026 04:39:56 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36aaa96e15b5b0d514b77b2d44142ad2ab78e7fa7af8c06826351eeb6c6150f5`  
		Last Modified: Tue, 03 Feb 2026 04:39:57 GMT  
		Size: 37.8 MB (37767555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7547a185449487deefabd7025cd804d78a0399cfc8c6831d9d5bff6f759b04`  
		Last Modified: Tue, 03 Feb 2026 04:39:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431a47248ff3557223eef91a10b044459456f051f2ab32938fce8648356d0c3`  
		Last Modified: Tue, 03 Feb 2026 05:25:50 GMT  
		Size: 5.7 MB (5674015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8aa139ec92adbfa6f1b5db0c8f0e7ccae4310e417abaf2d1a8349c0526705d`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adeb0eecdc2d96ed8a202e0baf9cd32b9dd955f9e7d737f58ec1f8bcf2e9e33`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445d4a93ae7daf648fc2f59b06be5556058ade490bfb67b3e6225032f18d9b2c`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:7e6b00425c55f72458df62fc405d2f703fa5e29c1ee8673415e9b2a68d068659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c60e27b0b62b91d2aa8a8c9a759a344fb0255aa6c09bddd3a3fb757aedf38f1`

```dockerfile
```

-	Layers:
	-	`sha256:611381c7004cc77d13fe926de8025d98cfd0a4e2c6f5c8698525f9d4698b7060`  
		Last Modified: Tue, 03 Feb 2026 05:25:50 GMT  
		Size: 2.3 MB (2281605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deebcfb069bffc65bd689fe1c3be97c5dca1f73a1c4780dee0176631976f2a28`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
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
$ docker pull fluentd@sha256:3b853bd23906c1816408ee609316cf8a7689aaaed1a014b6b49c24c283253917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76219400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe7763fe67625f4e48d6335a64e16721a223a5e4ac2c941f400c1f60eb6cffc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:12:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:15:22 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:15:22 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:15:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:15:22 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:15:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:15:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:15:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:15:22 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:20:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:20:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:20:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:20:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:20:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:20:38 GMT
USER fluent
# Tue, 03 Feb 2026 04:20:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:20:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05a0d4e4c16ffceb79d0ceb06d11084a791121ea4ec19243e3c00fc55e1c3a9`  
		Last Modified: Tue, 03 Feb 2026 03:15:31 GMT  
		Size: 1.3 MB (1287315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1fac4a7d33f7c6e4838767d92d0c06220d4b9591f1d776ae44ca7d1ea57199`  
		Last Modified: Tue, 03 Feb 2026 03:15:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bcb1ba844e9351be780393e4bc60c9be1ac35bf50222c960c76e6868b82db9`  
		Last Modified: Tue, 03 Feb 2026 03:15:32 GMT  
		Size: 37.7 MB (37661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb85ea55567993abd8de7ddf9b6df00275cfbb8f3f67e4bcb5f6b1b534b758`  
		Last Modified: Tue, 03 Feb 2026 03:15:31 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826baa5ad40ce02adbb9a52eb6e9eecc051c53bbf52c491873c96c76f5efeadd`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 6.0 MB (5974359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a6b69ff9695911dd096813746068afe6c322e38821ec149cc20f915ec1fe19`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937fed61a281bb4c0ffffe86c2f800a7c9d155304169105d6f0501aeaf1d8ef6`  
		Last Modified: Tue, 03 Feb 2026 04:20:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c28cbdcfa4bd3ad55967f7507ac1cfb9b32ee3531fca9300c778368b679dd`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:74fe03478a8f0fc59dadcb3a07950709dbb46f791269948488612d45543c3a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab65a08a3539869a2ac4ee95a9a76f3a98cb8ee8d5d96f3e737e0321116b608a`

```dockerfile
```

-	Layers:
	-	`sha256:a088033117d481385bbd97fe239532f4e569c29f56a2d55db2e0d716b5f0a77b`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 2.3 MB (2277381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d54feef28c7ae499a398916390dc5d61e81f890249114e4b8cbf2cf1c03954`  
		Last Modified: Tue, 03 Feb 2026 04:20:46 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:993d8f0aaa967ddc0f698b8365afed5414ad4367a5c8a99c4f3cb59a472b6fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80956432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cbc0b218744753b427be375028e1f6daf0d9b6e355098614bfb02be378032a`
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
# Tue, 03 Feb 2026 12:55:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 12:55:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 12:55:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 12:55:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 12:55:43 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 12:55:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 12:55:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 12:55:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 12:55:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 12:55:44 GMT
USER fluent
# Tue, 03 Feb 2026 12:55:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 12:55:44 GMT
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
	-	`sha256:3e35a71ba93612b0ce930f63c0e5018382079e39ba594dce5e721ce5ba2f00ee`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 6.5 MB (6524989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b64524936aa6d70341004113eba904d7e77974ebee5acfe68770b70cb11e3c`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9240d8876f06d9424ba6b4cabd8d5a5c4c219f06d2978fc0af9da543a15a3`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00f0253dc79d24e9ad9476f1c0e799f94b4ae208a14706fe887e170e6bbd3ba`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:da3d5fa8b3bbf8f6d6ed0a2f0db9289b76fff2560178f2e562ca017d75fb9107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937c9fa20a00a14724d04ee95168366ce66d8e0ab48d5513c53a1c04811984cd`

```dockerfile
```

-	Layers:
	-	`sha256:d61b558bcd3bcad47197215cfa1938a506fa6a38cae7bd624f1307f5e6065239`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 2.3 MB (2283728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e26ea783bb474be04dbb088c5fce469219107fd192f4f8fe6067c6d3d67040`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
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
$ docker pull fluentd@sha256:0d59a62499aaf3f08f0c3e45633279e9dc2580037825685fc3bc87f60ecf4b7b
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
$ docker pull fluentd@sha256:03a0a63c893db49c61fcdb1d0a3b3d33d0f4d71ca908fe9d245af51698831003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82043810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71469e6535f886dcb7358297d4ad87dc6a05ddfac1bac251994814a8b135d056`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:14:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:16:47 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:16:47 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 03:16:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 03:16:47 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 03:16:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:16:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:16:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:16:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:16:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:16:47 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:25:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:25:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 04:25:55 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 04:25:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 04:25:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:25:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:25:55 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:25:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:25:55 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:25:55 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:25:55 GMT
USER fluent
# Tue, 03 Feb 2026 04:25:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:25:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48372e33ccf8083312bf2c623ceab9d6c6a6ba9f95c29a34a6006f685512daf`  
		Last Modified: Tue, 03 Feb 2026 03:16:56 GMT  
		Size: 3.5 MB (3510204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa413459866fbddb21248dc9cb8ed0f7e69e6fb6d22da3c80c6bec2b7504068f`  
		Last Modified: Tue, 03 Feb 2026 03:16:56 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c2926c16aeb239352ed09a492ad32bc88b620fdde970c2e8d91d28459c9d10`  
		Last Modified: Tue, 03 Feb 2026 03:16:57 GMT  
		Size: 36.0 MB (36010880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001d02c9922d8c826ce71142da7e859fd1e52096f6b041f3d89b3552a5e1e6b1`  
		Last Modified: Tue, 03 Feb 2026 03:16:56 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a97ebabc65d3cd9efec254282927949a5bc63b98224f0b877e42c63ec50dad`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
		Size: 14.3 MB (14291838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dc99b00604834ef4e653f65d28ccbfd888ddd64506999d425e531892e2b458`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f6bdd89a42a62bc055fcd214488ecf62c2c9b33059c09ec28e622269c3d7da`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2d7550603de4ad83a38035bbb2fe1eb5834e686092ee09dfb3c14b5674b88`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5c28f77ddb3f40db7e82cb1b7bc2692f629b044c00b4c2ec3cb86ceea3a5593a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead4b871a1e5e295fb54e404f9082ab621ac124f233f1111c36e6affafd036b8`

```dockerfile
```

-	Layers:
	-	`sha256:8cda2240232d10ba751e40be862a8ed01d23212ae840c9723da7e8d8d284299d`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:639f3c466e62e996161f505d4c618af7bdf476054845a4bb25d59a2fcf8f02a1`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
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
$ docker pull fluentd@sha256:48f00bd7c389fc5d9b8a024eb234d0961259a706c33a5aee6e7adda915ec73c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73217424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3014905ba601389796d09fab666a9b35eafefe3610d208fd39ed09c8cf11b6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:38:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:38:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:40:37 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:40:37 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 04:40:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 04:40:37 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 04:40:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:40:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:40:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:40:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:40:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:40:37 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:25:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:25:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 05:25:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 05:25:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 05:25:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:25:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:25:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:25:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:25:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:25:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:25:49 GMT
USER fluent
# Tue, 03 Feb 2026 05:25:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:25:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1fbf192646fe352a9b4aedb0c817877e1fcaeea74e9f5e35b67ed9e4c8ebcb`  
		Last Modified: Tue, 03 Feb 2026 04:40:45 GMT  
		Size: 2.9 MB (2913784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e7714383eaa93253e7b9bf9f09745dfa98a9c78e40afa1339ed9d09353a4de`  
		Last Modified: Tue, 03 Feb 2026 04:40:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a24dcc13cafc866f1df4d3392613bf51c4a8d14f2df5c11e6f587ab9c46ddb`  
		Last Modified: Tue, 03 Feb 2026 04:40:46 GMT  
		Size: 32.2 MB (32167967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c70dd7c8f9341109e2fced49b70912c8ff6bec90f57e39d5ac9f64fb4a4e334`  
		Last Modified: Tue, 03 Feb 2026 04:40:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cd569a6b55d0f35b5aabb7a8142e2402db58477a603957cbf8d2e65e91ede0`  
		Last Modified: Tue, 03 Feb 2026 05:25:58 GMT  
		Size: 14.2 MB (14199184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd79306acfc5ad7fb1835d68872b8fad6a79e19a2c6a7a4bd00b6c85478184a`  
		Last Modified: Tue, 03 Feb 2026 05:25:57 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea5faec1a13d77eca6aacb36f64f755b50201eee629a2fbc90d33bdff72c0d2`  
		Last Modified: Tue, 03 Feb 2026 05:25:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6359ebe92670b929138d5bee481da4f42fdb52d00b31a1820a358e80ce75d3`  
		Last Modified: Tue, 03 Feb 2026 05:25:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d0427a2026c2425696900a64fd2fa2b4211e447a04b0447bdc7da9f45ee2b870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82717fdd207d77f745c854aef52a4d8e0718ebd776cd748638de63c4819e2cb7`

```dockerfile
```

-	Layers:
	-	`sha256:233349fec587372d62a758988be834c2d68ebef153a43cb599c26a8376ab5cd1`  
		Last Modified: Tue, 03 Feb 2026 05:25:58 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e9823f117f4b325ba0fc786b2186c28c89865ffd2c5fcf6e628b5717da258e`  
		Last Modified: Tue, 03 Feb 2026 05:25:57 GMT  
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
$ docker pull fluentd@sha256:50a2bd14a9d0a2f890fefdc8161360de0e438e922f8449dfa8d224440342d243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78969561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbce4a2ab1b1bed6a9a84f13387b93baa813bf2808be3c2d5b701e28eb0f5bc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:13:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:13:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:15:49 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:15:49 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 03:15:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 03:15:49 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 03:15:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:15:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:15:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:15:50 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:20:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:20:30 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 04:20:30 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 04:20:30 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 04:20:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:20:30 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:20:30 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:20:30 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:20:30 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:20:30 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:20:30 GMT
USER fluent
# Tue, 03 Feb 2026 04:20:30 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:20:30 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5f93d228262ac8f12d9af5f87a89d9722b3f4d559df30edfa91327db9f457723`  
		Last Modified: Tue, 03 Feb 2026 01:13:52 GMT  
		Size: 29.2 MB (29210015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24abb20a59c9f8d1ac83d369a03c98239393420480e2f8a2434805a843a6ceda`  
		Last Modified: Tue, 03 Feb 2026 03:15:58 GMT  
		Size: 3.5 MB (3512932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c502f7acf59b98d4598573c8b213f479f5ae653ec910d8e29648933447983a`  
		Last Modified: Tue, 03 Feb 2026 03:15:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da7a48fe5edbd2304cd4a408651078235403c424d484261afcc9e0d2a3d0b81`  
		Last Modified: Tue, 03 Feb 2026 03:15:58 GMT  
		Size: 32.2 MB (32163330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c1df4ea9a1ab068bdd0ce2b1ca9ae87a72cdc24beefecac227d1ca8f5758b0`  
		Last Modified: Tue, 03 Feb 2026 03:15:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9f4a78064febb5bcf29691fa4ca6ac56738330602404f3cf60c671665e4352`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 14.1 MB (14080888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b823f2df43bc10b0afe5affee5ccf61d306dd7e90cedafab15aa3a1961e6690`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0f8f662145c0de1cd673c4e0ff13dd8261111047fc01a4d3e6afaa85e59064`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31076b8966382ff20ee5a8efe4cf5d045f49622b7199404d3238ef398c5312ea`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e98af611a86af65641ff52f8ddaeb62a115e34dc2847f278ff249f6dda98dead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3a6ab66cfd435ef59a02238c808463d93f5542fc3c9e961b3ff99eacbee83`

```dockerfile
```

-	Layers:
	-	`sha256:d740811031601ef4b6a8dbd5672641746ea1211424472229ce8e0f41220d0938`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980624a6a1db46c4aad08e751cc7c41bc261cc84b5d5952a8ff26879cda71b64`  
		Last Modified: Tue, 03 Feb 2026 04:20:38 GMT  
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
$ docker pull fluentd@sha256:0d59a62499aaf3f08f0c3e45633279e9dc2580037825685fc3bc87f60ecf4b7b
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
$ docker pull fluentd@sha256:03a0a63c893db49c61fcdb1d0a3b3d33d0f4d71ca908fe9d245af51698831003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82043810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71469e6535f886dcb7358297d4ad87dc6a05ddfac1bac251994814a8b135d056`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:14:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:16:47 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:16:47 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 03:16:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 03:16:47 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 03:16:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:16:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:16:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:16:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:16:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:16:47 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:25:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:25:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 04:25:55 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 04:25:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 04:25:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:25:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:25:55 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:25:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:25:55 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:25:55 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:25:55 GMT
USER fluent
# Tue, 03 Feb 2026 04:25:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:25:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48372e33ccf8083312bf2c623ceab9d6c6a6ba9f95c29a34a6006f685512daf`  
		Last Modified: Tue, 03 Feb 2026 03:16:56 GMT  
		Size: 3.5 MB (3510204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa413459866fbddb21248dc9cb8ed0f7e69e6fb6d22da3c80c6bec2b7504068f`  
		Last Modified: Tue, 03 Feb 2026 03:16:56 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c2926c16aeb239352ed09a492ad32bc88b620fdde970c2e8d91d28459c9d10`  
		Last Modified: Tue, 03 Feb 2026 03:16:57 GMT  
		Size: 36.0 MB (36010880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001d02c9922d8c826ce71142da7e859fd1e52096f6b041f3d89b3552a5e1e6b1`  
		Last Modified: Tue, 03 Feb 2026 03:16:56 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a97ebabc65d3cd9efec254282927949a5bc63b98224f0b877e42c63ec50dad`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
		Size: 14.3 MB (14291838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08dc99b00604834ef4e653f65d28ccbfd888ddd64506999d425e531892e2b458`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f6bdd89a42a62bc055fcd214488ecf62c2c9b33059c09ec28e622269c3d7da`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2d7550603de4ad83a38035bbb2fe1eb5834e686092ee09dfb3c14b5674b88`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5c28f77ddb3f40db7e82cb1b7bc2692f629b044c00b4c2ec3cb86ceea3a5593a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead4b871a1e5e295fb54e404f9082ab621ac124f233f1111c36e6affafd036b8`

```dockerfile
```

-	Layers:
	-	`sha256:8cda2240232d10ba751e40be862a8ed01d23212ae840c9723da7e8d8d284299d`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:639f3c466e62e996161f505d4c618af7bdf476054845a4bb25d59a2fcf8f02a1`  
		Last Modified: Tue, 03 Feb 2026 04:26:03 GMT  
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
$ docker pull fluentd@sha256:48f00bd7c389fc5d9b8a024eb234d0961259a706c33a5aee6e7adda915ec73c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73217424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3014905ba601389796d09fab666a9b35eafefe3610d208fd39ed09c8cf11b6`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:38:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:38:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:40:37 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:40:37 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 04:40:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 04:40:37 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 04:40:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:40:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:40:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:40:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:40:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:40:37 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:25:49 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:25:49 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 05:25:49 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 05:25:49 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 05:25:49 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:25:49 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:25:49 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:25:49 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:25:49 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:25:49 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:25:49 GMT
USER fluent
# Tue, 03 Feb 2026 05:25:49 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:25:49 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1fbf192646fe352a9b4aedb0c817877e1fcaeea74e9f5e35b67ed9e4c8ebcb`  
		Last Modified: Tue, 03 Feb 2026 04:40:45 GMT  
		Size: 2.9 MB (2913784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e7714383eaa93253e7b9bf9f09745dfa98a9c78e40afa1339ed9d09353a4de`  
		Last Modified: Tue, 03 Feb 2026 04:40:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a24dcc13cafc866f1df4d3392613bf51c4a8d14f2df5c11e6f587ab9c46ddb`  
		Last Modified: Tue, 03 Feb 2026 04:40:46 GMT  
		Size: 32.2 MB (32167967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c70dd7c8f9341109e2fced49b70912c8ff6bec90f57e39d5ac9f64fb4a4e334`  
		Last Modified: Tue, 03 Feb 2026 04:40:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97cd569a6b55d0f35b5aabb7a8142e2402db58477a603957cbf8d2e65e91ede0`  
		Last Modified: Tue, 03 Feb 2026 05:25:58 GMT  
		Size: 14.2 MB (14199184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd79306acfc5ad7fb1835d68872b8fad6a79e19a2c6a7a4bd00b6c85478184a`  
		Last Modified: Tue, 03 Feb 2026 05:25:57 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea5faec1a13d77eca6aacb36f64f755b50201eee629a2fbc90d33bdff72c0d2`  
		Last Modified: Tue, 03 Feb 2026 05:25:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6359ebe92670b929138d5bee481da4f42fdb52d00b31a1820a358e80ce75d3`  
		Last Modified: Tue, 03 Feb 2026 05:25:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:d0427a2026c2425696900a64fd2fa2b4211e447a04b0447bdc7da9f45ee2b870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82717fdd207d77f745c854aef52a4d8e0718ebd776cd748638de63c4819e2cb7`

```dockerfile
```

-	Layers:
	-	`sha256:233349fec587372d62a758988be834c2d68ebef153a43cb599c26a8376ab5cd1`  
		Last Modified: Tue, 03 Feb 2026 05:25:58 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e9823f117f4b325ba0fc786b2186c28c89865ffd2c5fcf6e628b5717da258e`  
		Last Modified: Tue, 03 Feb 2026 05:25:57 GMT  
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
$ docker pull fluentd@sha256:50a2bd14a9d0a2f890fefdc8161360de0e438e922f8449dfa8d224440342d243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78969561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbce4a2ab1b1bed6a9a84f13387b93baa813bf2808be3c2d5b701e28eb0f5bc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:13:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:13:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:15:49 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:15:49 GMT
ENV RUBY_VERSION=3.2.10
# Tue, 03 Feb 2026 03:15:49 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.10.tar.xz
# Tue, 03 Feb 2026 03:15:49 GMT
ENV RUBY_DOWNLOAD_SHA256=a64a8a910ac2f28834b2170dedea688f06cbc6431fcd65eb18cc49ddbf3826ae
# Tue, 03 Feb 2026 03:15:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:15:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:49 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:15:50 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:15:50 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:20:30 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:20:30 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 03 Feb 2026 04:20:30 GMT
ENV TINI_VERSION=0.18.0
# Tue, 03 Feb 2026 04:20:30 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 03 Feb 2026 04:20:30 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:20:30 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:20:30 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:20:30 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:20:30 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:20:30 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:20:30 GMT
USER fluent
# Tue, 03 Feb 2026 04:20:30 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:20:30 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5f93d228262ac8f12d9af5f87a89d9722b3f4d559df30edfa91327db9f457723`  
		Last Modified: Tue, 03 Feb 2026 01:13:52 GMT  
		Size: 29.2 MB (29210015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24abb20a59c9f8d1ac83d369a03c98239393420480e2f8a2434805a843a6ceda`  
		Last Modified: Tue, 03 Feb 2026 03:15:58 GMT  
		Size: 3.5 MB (3512932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c502f7acf59b98d4598573c8b213f479f5ae653ec910d8e29648933447983a`  
		Last Modified: Tue, 03 Feb 2026 03:15:57 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da7a48fe5edbd2304cd4a408651078235403c424d484261afcc9e0d2a3d0b81`  
		Last Modified: Tue, 03 Feb 2026 03:15:58 GMT  
		Size: 32.2 MB (32163330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c1df4ea9a1ab068bdd0ce2b1ca9ae87a72cdc24beefecac227d1ca8f5758b0`  
		Last Modified: Tue, 03 Feb 2026 03:15:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9f4a78064febb5bcf29691fa4ca6ac56738330602404f3cf60c671665e4352`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 14.1 MB (14080888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b823f2df43bc10b0afe5affee5ccf61d306dd7e90cedafab15aa3a1961e6690`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0f8f662145c0de1cd673c4e0ff13dd8261111047fc01a4d3e6afaa85e59064`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31076b8966382ff20ee5a8efe4cf5d045f49622b7199404d3238ef398c5312ea`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e98af611a86af65641ff52f8ddaeb62a115e34dc2847f278ff249f6dda98dead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d3a6ab66cfd435ef59a02238c808463d93f5542fc3c9e961b3ff99eacbee83`

```dockerfile
```

-	Layers:
	-	`sha256:d740811031601ef4b6a8dbd5672641746ea1211424472229ce8e0f41220d0938`  
		Last Modified: Tue, 03 Feb 2026 04:20:39 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980624a6a1db46c4aad08e751cc7c41bc261cc84b5d5952a8ff26879cda71b64`  
		Last Modified: Tue, 03 Feb 2026 04:20:38 GMT  
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
$ docker pull fluentd@sha256:271bf34fe9ded0e997f03d0e68913ff78aeb89568060083887a6650cdb4537ad
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
$ docker pull fluentd@sha256:45c609aa35a6efbbf7ba404bb177c4a99beafcf726b35af540630df793f0229c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79177985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3742aea87a869860fd82d04ba4e0f2679c87240dbd6cb0ae997cf0bf5660a797`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:13:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:13:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:15:56 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:15:56 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:15:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:15:56 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:15:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:15:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:15:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:15:56 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:26:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:26:07 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:26:07 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:26:08 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:26:08 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:26:08 GMT
USER fluent
# Tue, 03 Feb 2026 04:26:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:26:08 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd62801a76356b1b2a4bd7d0e0af507d64d67295bb586f272377f03f69211cb`  
		Last Modified: Tue, 03 Feb 2026 03:16:06 GMT  
		Size: 1.3 MB (1279351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559eac235c75feecce250b6f5bf2035a78c5d732256b9803c22f73f5fab57c4`  
		Last Modified: Tue, 03 Feb 2026 03:16:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80098ee487838645ca286b994643ee6cd611bfde9dd33e14009a0cb6111d368f`  
		Last Modified: Tue, 03 Feb 2026 03:16:07 GMT  
		Size: 42.1 MB (42112727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f5098c7eff479e8cf2942ce700947554a5460f03a9c982c9a0c7971ed8e830`  
		Last Modified: Tue, 03 Feb 2026 03:16:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64f9e55a08318c5b342595d089796c90c4ea9709834ccdb0c62a668dd6ded4`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 6.0 MB (6004917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ba26a50d4e36f5948e8e96b92fe65b04b6453629121b5c4884c9628c0b85ae`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073b4135eb33889189bc6c314c38ac61829dae1bf884092fbd5f27cfd2c8db1d`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2b7869fc658a75615a950a30320230d90acba798b6e51f0a93cecf18077a81`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ebef43c47a752172b97918a1a5f174058a98c9377883163bed7c8c5e953780e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42803b2651c6d9f54ecec768e7b60ef379c0af1f3d20bf483d6b980e2b856353`

```dockerfile
```

-	Layers:
	-	`sha256:c37f44765165c6e318ddd053d9fbcba71f602ba78c7418b30ccea04294084872`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 2.3 MB (2280193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa5c2b07161651b899a277dc1fd27269aaad60f8cea33acd8f5cfbf9acfa8d6`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
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
$ docker pull fluentd@sha256:ed1f60c202bd2fd7d98b1cbafc3ce6b37b52247d52a8a9e99ae4fc5e292b82e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70894341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bbd347cae3af93c81731a0e5fa643bc53a41f5db36f63c5da866f110fa8c69`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:37:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:39:47 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:39:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:39:47 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:39:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:39:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:39:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:39:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:39:47 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:25:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:25:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 05:25:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:25:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:25:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:25:42 GMT
USER fluent
# Tue, 03 Feb 2026 05:25:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:25:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b80b6adb1ac78286c039e72a54aa2f5853d41b835f2b869690c3949c3d00d1d`  
		Last Modified: Tue, 03 Feb 2026 04:39:56 GMT  
		Size: 1.2 MB (1236625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f91969b4a8b878ca7237b13f3af6a5a1eca4dfb8f3119c7e9108f5f6b1f1dc7`  
		Last Modified: Tue, 03 Feb 2026 04:39:56 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36aaa96e15b5b0d514b77b2d44142ad2ab78e7fa7af8c06826351eeb6c6150f5`  
		Last Modified: Tue, 03 Feb 2026 04:39:57 GMT  
		Size: 37.8 MB (37767555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7547a185449487deefabd7025cd804d78a0399cfc8c6831d9d5bff6f759b04`  
		Last Modified: Tue, 03 Feb 2026 04:39:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431a47248ff3557223eef91a10b044459456f051f2ab32938fce8648356d0c3`  
		Last Modified: Tue, 03 Feb 2026 05:25:50 GMT  
		Size: 5.7 MB (5674015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8aa139ec92adbfa6f1b5db0c8f0e7ccae4310e417abaf2d1a8349c0526705d`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adeb0eecdc2d96ed8a202e0baf9cd32b9dd955f9e7d737f58ec1f8bcf2e9e33`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445d4a93ae7daf648fc2f59b06be5556058ade490bfb67b3e6225032f18d9b2c`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7e6b00425c55f72458df62fc405d2f703fa5e29c1ee8673415e9b2a68d068659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c60e27b0b62b91d2aa8a8c9a759a344fb0255aa6c09bddd3a3fb757aedf38f1`

```dockerfile
```

-	Layers:
	-	`sha256:611381c7004cc77d13fe926de8025d98cfd0a4e2c6f5c8698525f9d4698b7060`  
		Last Modified: Tue, 03 Feb 2026 05:25:50 GMT  
		Size: 2.3 MB (2281605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deebcfb069bffc65bd689fe1c3be97c5dca1f73a1c4780dee0176631976f2a28`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
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
$ docker pull fluentd@sha256:3b853bd23906c1816408ee609316cf8a7689aaaed1a014b6b49c24c283253917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76219400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe7763fe67625f4e48d6335a64e16721a223a5e4ac2c941f400c1f60eb6cffc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:12:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:15:22 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:15:22 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:15:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:15:22 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:15:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:15:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:15:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:15:22 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:20:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:20:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:20:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:20:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:20:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:20:38 GMT
USER fluent
# Tue, 03 Feb 2026 04:20:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:20:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05a0d4e4c16ffceb79d0ceb06d11084a791121ea4ec19243e3c00fc55e1c3a9`  
		Last Modified: Tue, 03 Feb 2026 03:15:31 GMT  
		Size: 1.3 MB (1287315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1fac4a7d33f7c6e4838767d92d0c06220d4b9591f1d776ae44ca7d1ea57199`  
		Last Modified: Tue, 03 Feb 2026 03:15:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bcb1ba844e9351be780393e4bc60c9be1ac35bf50222c960c76e6868b82db9`  
		Last Modified: Tue, 03 Feb 2026 03:15:32 GMT  
		Size: 37.7 MB (37661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb85ea55567993abd8de7ddf9b6df00275cfbb8f3f67e4bcb5f6b1b534b758`  
		Last Modified: Tue, 03 Feb 2026 03:15:31 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826baa5ad40ce02adbb9a52eb6e9eecc051c53bbf52c491873c96c76f5efeadd`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 6.0 MB (5974359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a6b69ff9695911dd096813746068afe6c322e38821ec149cc20f915ec1fe19`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937fed61a281bb4c0ffffe86c2f800a7c9d155304169105d6f0501aeaf1d8ef6`  
		Last Modified: Tue, 03 Feb 2026 04:20:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c28cbdcfa4bd3ad55967f7507ac1cfb9b32ee3531fca9300c778368b679dd`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:74fe03478a8f0fc59dadcb3a07950709dbb46f791269948488612d45543c3a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab65a08a3539869a2ac4ee95a9a76f3a98cb8ee8d5d96f3e737e0321116b608a`

```dockerfile
```

-	Layers:
	-	`sha256:a088033117d481385bbd97fe239532f4e569c29f56a2d55db2e0d716b5f0a77b`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 2.3 MB (2277381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d54feef28c7ae499a398916390dc5d61e81f890249114e4b8cbf2cf1c03954`  
		Last Modified: Tue, 03 Feb 2026 04:20:46 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:993d8f0aaa967ddc0f698b8365afed5414ad4367a5c8a99c4f3cb59a472b6fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80956432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cbc0b218744753b427be375028e1f6daf0d9b6e355098614bfb02be378032a`
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
# Tue, 03 Feb 2026 12:55:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 12:55:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 12:55:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 12:55:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 12:55:43 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 12:55:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 12:55:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 12:55:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 12:55:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 12:55:44 GMT
USER fluent
# Tue, 03 Feb 2026 12:55:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 12:55:44 GMT
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
	-	`sha256:3e35a71ba93612b0ce930f63c0e5018382079e39ba594dce5e721ce5ba2f00ee`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 6.5 MB (6524989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b64524936aa6d70341004113eba904d7e77974ebee5acfe68770b70cb11e3c`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9240d8876f06d9424ba6b4cabd8d5a5c4c219f06d2978fc0af9da543a15a3`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00f0253dc79d24e9ad9476f1c0e799f94b4ae208a14706fe887e170e6bbd3ba`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:da3d5fa8b3bbf8f6d6ed0a2f0db9289b76fff2560178f2e562ca017d75fb9107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937c9fa20a00a14724d04ee95168366ce66d8e0ab48d5513c53a1c04811984cd`

```dockerfile
```

-	Layers:
	-	`sha256:d61b558bcd3bcad47197215cfa1938a506fa6a38cae7bd624f1307f5e6065239`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 2.3 MB (2283728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e26ea783bb474be04dbb088c5fce469219107fd192f4f8fe6067c6d3d67040`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
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
$ docker pull fluentd@sha256:271bf34fe9ded0e997f03d0e68913ff78aeb89568060083887a6650cdb4537ad
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
$ docker pull fluentd@sha256:45c609aa35a6efbbf7ba404bb177c4a99beafcf726b35af540630df793f0229c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79177985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3742aea87a869860fd82d04ba4e0f2679c87240dbd6cb0ae997cf0bf5660a797`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:13:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:13:20 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:15:56 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:15:56 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:15:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:15:56 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:15:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:15:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:15:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:15:56 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:26:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:26:07 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:26:07 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:26:08 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:26:08 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:26:08 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:26:08 GMT
USER fluent
# Tue, 03 Feb 2026 04:26:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:26:08 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd62801a76356b1b2a4bd7d0e0af507d64d67295bb586f272377f03f69211cb`  
		Last Modified: Tue, 03 Feb 2026 03:16:06 GMT  
		Size: 1.3 MB (1279351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559eac235c75feecce250b6f5bf2035a78c5d732256b9803c22f73f5fab57c4`  
		Last Modified: Tue, 03 Feb 2026 03:16:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80098ee487838645ca286b994643ee6cd611bfde9dd33e14009a0cb6111d368f`  
		Last Modified: Tue, 03 Feb 2026 03:16:07 GMT  
		Size: 42.1 MB (42112727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f5098c7eff479e8cf2942ce700947554a5460f03a9c982c9a0c7971ed8e830`  
		Last Modified: Tue, 03 Feb 2026 03:16:06 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64f9e55a08318c5b342595d089796c90c4ea9709834ccdb0c62a668dd6ded4`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 6.0 MB (6004917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ba26a50d4e36f5948e8e96b92fe65b04b6453629121b5c4884c9628c0b85ae`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073b4135eb33889189bc6c314c38ac61829dae1bf884092fbd5f27cfd2c8db1d`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c2b7869fc658a75615a950a30320230d90acba798b6e51f0a93cecf18077a81`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ebef43c47a752172b97918a1a5f174058a98c9377883163bed7c8c5e953780e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42803b2651c6d9f54ecec768e7b60ef379c0af1f3d20bf483d6b980e2b856353`

```dockerfile
```

-	Layers:
	-	`sha256:c37f44765165c6e318ddd053d9fbcba71f602ba78c7418b30ccea04294084872`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
		Size: 2.3 MB (2280193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fa5c2b07161651b899a277dc1fd27269aaad60f8cea33acd8f5cfbf9acfa8d6`  
		Last Modified: Tue, 03 Feb 2026 04:26:16 GMT  
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
$ docker pull fluentd@sha256:ed1f60c202bd2fd7d98b1cbafc3ce6b37b52247d52a8a9e99ae4fc5e292b82e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70894341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bbd347cae3af93c81731a0e5fa643bc53a41f5db36f63c5da866f110fa8c69`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 04:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 04:37:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 04:39:47 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:39:47 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 04:39:47 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 04:39:47 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 04:39:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 04:39:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 04:39:47 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 04:39:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:39:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 04:39:47 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 05:25:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 05:25:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 05:25:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 05:25:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 05:25:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 05:25:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 05:25:42 GMT
USER fluent
# Tue, 03 Feb 2026 05:25:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 05:25:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b80b6adb1ac78286c039e72a54aa2f5853d41b835f2b869690c3949c3d00d1d`  
		Last Modified: Tue, 03 Feb 2026 04:39:56 GMT  
		Size: 1.2 MB (1236625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f91969b4a8b878ca7237b13f3af6a5a1eca4dfb8f3119c7e9108f5f6b1f1dc7`  
		Last Modified: Tue, 03 Feb 2026 04:39:56 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36aaa96e15b5b0d514b77b2d44142ad2ab78e7fa7af8c06826351eeb6c6150f5`  
		Last Modified: Tue, 03 Feb 2026 04:39:57 GMT  
		Size: 37.8 MB (37767555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7547a185449487deefabd7025cd804d78a0399cfc8c6831d9d5bff6f759b04`  
		Last Modified: Tue, 03 Feb 2026 04:39:56 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1431a47248ff3557223eef91a10b044459456f051f2ab32938fce8648356d0c3`  
		Last Modified: Tue, 03 Feb 2026 05:25:50 GMT  
		Size: 5.7 MB (5674015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8aa139ec92adbfa6f1b5db0c8f0e7ccae4310e417abaf2d1a8349c0526705d`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4adeb0eecdc2d96ed8a202e0baf9cd32b9dd955f9e7d737f58ec1f8bcf2e9e33`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445d4a93ae7daf648fc2f59b06be5556058ade490bfb67b3e6225032f18d9b2c`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7e6b00425c55f72458df62fc405d2f703fa5e29c1ee8673415e9b2a68d068659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c60e27b0b62b91d2aa8a8c9a759a344fb0255aa6c09bddd3a3fb757aedf38f1`

```dockerfile
```

-	Layers:
	-	`sha256:611381c7004cc77d13fe926de8025d98cfd0a4e2c6f5c8698525f9d4698b7060`  
		Last Modified: Tue, 03 Feb 2026 05:25:50 GMT  
		Size: 2.3 MB (2281605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deebcfb069bffc65bd689fe1c3be97c5dca1f73a1c4780dee0176631976f2a28`  
		Last Modified: Tue, 03 Feb 2026 05:25:49 GMT  
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
$ docker pull fluentd@sha256:3b853bd23906c1816408ee609316cf8a7689aaaed1a014b6b49c24c283253917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76219400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe7763fe67625f4e48d6335a64e16721a223a5e4ac2c941f400c1f60eb6cffc`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 03:12:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 03 Feb 2026 03:15:22 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:15:22 GMT
ENV RUBY_VERSION=3.4.8
# Tue, 03 Feb 2026 03:15:22 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Tue, 03 Feb 2026 03:15:22 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Tue, 03 Feb 2026 03:15:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 03 Feb 2026 03:15:22 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:22 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 03 Feb 2026 03:15:22 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:15:22 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 03 Feb 2026 03:15:22 GMT
CMD ["irb"]
# Tue, 03 Feb 2026 04:20:38 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 04:20:38 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 04:20:38 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 04:20:38 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 04:20:38 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 04:20:38 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 04:20:38 GMT
USER fluent
# Tue, 03 Feb 2026 04:20:38 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 04:20:38 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05a0d4e4c16ffceb79d0ceb06d11084a791121ea4ec19243e3c00fc55e1c3a9`  
		Last Modified: Tue, 03 Feb 2026 03:15:31 GMT  
		Size: 1.3 MB (1287315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1fac4a7d33f7c6e4838767d92d0c06220d4b9591f1d776ae44ca7d1ea57199`  
		Last Modified: Tue, 03 Feb 2026 03:15:21 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bcb1ba844e9351be780393e4bc60c9be1ac35bf50222c960c76e6868b82db9`  
		Last Modified: Tue, 03 Feb 2026 03:15:32 GMT  
		Size: 37.7 MB (37661473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb85ea55567993abd8de7ddf9b6df00275cfbb8f3f67e4bcb5f6b1b534b758`  
		Last Modified: Tue, 03 Feb 2026 03:15:31 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826baa5ad40ce02adbb9a52eb6e9eecc051c53bbf52c491873c96c76f5efeadd`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 6.0 MB (5974359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a6b69ff9695911dd096813746068afe6c322e38821ec149cc20f915ec1fe19`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937fed61a281bb4c0ffffe86c2f800a7c9d155304169105d6f0501aeaf1d8ef6`  
		Last Modified: Tue, 03 Feb 2026 04:20:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7c28cbdcfa4bd3ad55967f7507ac1cfb9b32ee3531fca9300c778368b679dd`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:74fe03478a8f0fc59dadcb3a07950709dbb46f791269948488612d45543c3a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab65a08a3539869a2ac4ee95a9a76f3a98cb8ee8d5d96f3e737e0321116b608a`

```dockerfile
```

-	Layers:
	-	`sha256:a088033117d481385bbd97fe239532f4e569c29f56a2d55db2e0d716b5f0a77b`  
		Last Modified: Tue, 03 Feb 2026 04:20:47 GMT  
		Size: 2.3 MB (2277381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d54feef28c7ae499a398916390dc5d61e81f890249114e4b8cbf2cf1c03954`  
		Last Modified: Tue, 03 Feb 2026 04:20:46 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:993d8f0aaa967ddc0f698b8365afed5414ad4367a5c8a99c4f3cb59a472b6fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (80956432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cbc0b218744753b427be375028e1f6daf0d9b6e355098614bfb02be378032a`
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
# Tue, 03 Feb 2026 12:55:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 03 Feb 2026 12:55:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Tue, 03 Feb 2026 12:55:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 03 Feb 2026 12:55:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 03 Feb 2026 12:55:43 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 03 Feb 2026 12:55:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 03 Feb 2026 12:55:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 03 Feb 2026 12:55:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 03 Feb 2026 12:55:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 03 Feb 2026 12:55:44 GMT
USER fluent
# Tue, 03 Feb 2026 12:55:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 03 Feb 2026 12:55:44 GMT
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
	-	`sha256:3e35a71ba93612b0ce930f63c0e5018382079e39ba594dce5e721ce5ba2f00ee`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 6.5 MB (6524989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b64524936aa6d70341004113eba904d7e77974ebee5acfe68770b70cb11e3c`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f9240d8876f06d9424ba6b4cabd8d5a5c4c219f06d2978fc0af9da543a15a3`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00f0253dc79d24e9ad9476f1c0e799f94b4ae208a14706fe887e170e6bbd3ba`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:da3d5fa8b3bbf8f6d6ed0a2f0db9289b76fff2560178f2e562ca017d75fb9107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937c9fa20a00a14724d04ee95168366ce66d8e0ab48d5513c53a1c04811984cd`

```dockerfile
```

-	Layers:
	-	`sha256:d61b558bcd3bcad47197215cfa1938a506fa6a38cae7bd624f1307f5e6065239`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
		Size: 2.3 MB (2283728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87e26ea783bb474be04dbb088c5fce469219107fd192f4f8fe6067c6d3d67040`  
		Last Modified: Tue, 03 Feb 2026 12:56:10 GMT  
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

## `fluentd:v1.19.2-1.0`

```console
$ docker pull fluentd@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `fluentd:v1.19.2-debian-1.0`

```console
$ docker pull fluentd@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0
