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
$ docker pull fluentd@sha256:dcbc40508693421a01428cd5112d60c5726c0e79ca9ed870d4e668aeee718ccb
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
$ docker pull fluentd@sha256:2f4043c322f55eec6c6708e4efd629c144448e0a196244c1902a0f1a6c43e721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79240276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d713ba17c405e8e96c3994d35aef5158cf916d53682838c284731869598b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:28:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:31:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:31:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:31:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:33:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:33:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 03:33:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:33:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:33:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:33:51 GMT
USER fluent
# Tue, 07 Apr 2026 03:33:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:33:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78c84e44d70408c199a2896d0fe6d15b64efcceafe0e09550d5177ecdab72b5`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 1.3 MB (1279868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c086a7638e3fda68aac0522c41b07f5f10ac23fed584ee16a13498e0a4947d`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b6e55e1373be9c47416cd4ec47847af123c40d71aaeeb5c34653eb3e287ceb`  
		Last Modified: Tue, 07 Apr 2026 02:31:37 GMT  
		Size: 42.1 MB (42127244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2e954b41c2ddc19fb451b0eacc5ef3bbf6542b210296a77ae759a1277d7d38`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2f4817d01410fa0935c2ac51032921ff607e7de054d59d4cce546f23f28273`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 6.1 MB (6055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287ffb4f171600c7eaad32b94171730f57d10ee2704dc3f2d14f2ad79786dfb5`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ab56bccb331339769e77903e049fb948862d2955c250bc976c836191f85d5d`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e04c8092324d16d133bf8a28c5ecbd2a61e71e004a3732458aa69a376d141b`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:bd420eafe75e77c9b004aec3deedb09835a4aa36c85624938eb39fd5e3965b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa3403daf8ff28a64fa6d7bb54ee31b8e3672d3c5ba284d163bad93de84c4bc`

```dockerfile
```

-	Layers:
	-	`sha256:4ea95f6fc3952ecf0f8d41802f1f42d8aeacfe1e3f3954bfb29d13bc89c83b77`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 2.3 MB (2281700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e469a7bf6b1dbca433e02e1e6cfafc8563fc1568ec1f275b79b96f94afa2a287`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:737d41da6bfb0ce9ebc6ada5309f93a3c66b48aa251d12b62c1338633d2b906c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73091229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fddf682d8379469a82e2365369a447e62450bf54b18d429978c6bdea48fce26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:42:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:42:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 03:45:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:45:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:40:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:40:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 04:40:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:40:17 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:40:17 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:40:17 GMT
USER fluent
# Tue, 07 Apr 2026 04:40:17 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:40:17 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f83fcfefaffee8aa367effced408a0e6a87a5e59cdee33c2ca23721e3666bb`  
		Last Modified: Tue, 07 Apr 2026 03:45:13 GMT  
		Size: 1.3 MB (1263659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9350562d97a8b76eee53f9378f84c348e2e8ce41eb494a8f9acfd953ee73661d`  
		Last Modified: Tue, 07 Apr 2026 03:45:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff55ef1d37d6eddef2754669cb01a902319f33e3b5835659ce3c7fbe987cf169`  
		Last Modified: Tue, 07 Apr 2026 03:45:14 GMT  
		Size: 37.9 MB (37924109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db8d12e894040067d04d239a563bb338afdefd7e3ab192ce444708a3e277ac`  
		Last Modified: Tue, 07 Apr 2026 03:45:12 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594bfd195b76e112143930963588f6fc3d3585286f3a7be63979448e52d19bfa`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 6.0 MB (5957259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a637356205a8b660cd31964cf17283ddf1c0f2f1e8d40211a9b693f0fe4f18e`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34cdc5b6faa040070007317eaf98b4c1a3767447b6a72c5856e9fb68ac2cbc1`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc11c1d16b742a1ca4e45e2a3dd99b84782bfb227a6332cab341ed34dfd39ad0`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:4ff05bbc8133861b058fbd1d7a8f5afe687d1fa480c668942864f709ec142794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aaed9763b5c76a7ae5965cd090e83cb34052428ced62536562e131a965a9c3`

```dockerfile
```

-	Layers:
	-	`sha256:41c7bea2c8853c86ec41712b331858bf289f07d6f25b7985e8a9bbb031dfb61a`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 2.3 MB (2284671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2589f3eaa3dee5c0c385b127f1f2689c74618d980ec8b9305bba92d694b08048`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:e79ade4311d7653af470029e4dd6340fe8bd1dbc7feb9be95a6aa1ccc787bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70955862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e1393d31b464a3412ae704c38cafaddbb09bbde369bdfc9bf352677d315dc4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:17:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 03:19:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:19:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:19:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:19:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:35:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:35:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 04:35:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:35:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:35:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:35:40 GMT
USER fluent
# Tue, 07 Apr 2026 04:35:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:35:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66e9f844a8fcc6c0af5b1c95ad1e0c477f48277d9bfab72116a2780faf5f9e`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 1.2 MB (1237567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fb85dc50c757ea6577b3fef8fabfe4a5abb87834dc45f032c1f9a56274f658`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dba43d16f47f9f243dd54e854300da3d235512c9a3641611cbfb6a1de8acdbc`  
		Last Modified: Tue, 07 Apr 2026 03:20:07 GMT  
		Size: 37.8 MB (37781086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7219bd5fc4e67916c070402dd93cca9ba0ab97e52a6923882144b109de88b3c`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141b3b04696ed9a81f5a230237c23991f9fecd1a7624de095ed4d3410499d3f9`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 5.7 MB (5725160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c3c03706ded85063032a9d8666ebe800cfc8427865f7ce985d65a43403ad9`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e68b06e5892c7aae5c0f861b67c1fc1c5a16655cf23ab80110bdeec81d96a0`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58caa9811c5a3c5eac8958d7fb2b43e5b7f1dbf70ebc23667af645e4246dbbd`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:1f0ac058d80c84f4f1d24af7904e537319937583d902b9eb0de2fdda90b2a9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189d1c1f21a2aa342c7214cee2c6ae0f9ca01f5e80c45fb34673fd3f7a2b5df7`

```dockerfile
```

-	Layers:
	-	`sha256:0398d0b4efc9f877bb05a5f1db9ddb082bd71d19f8f44f0b140e41ea356b4572`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 2.3 MB (2283112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096351bc515e41f330c8af901593b4e186a73576011831dd97a67de4e5500535`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:5cce0c8f22191219a6dab87853fae5e3e70996a52ae486fc14329e2514f100f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79527060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bea47c3c5267b89121771f533137d1186e370d46c8779428e5380ffb976f37`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:35:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:37:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:37:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:37:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:44:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:44:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 03:44:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:44:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:44:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:44:51 GMT
USER fluent
# Tue, 07 Apr 2026 03:44:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:44:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65aef497c0f85b6d39008607e5c5e436adafd67d8f206feae2950d981405d5`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 1.3 MB (1261734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd6aa133452fc14cef07cf3b140623bbe92c243c23385fa35d4d320f16755a`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca299d5f81a969b938936930c899ebb4daf7c60e8cf953c60d068e3ed060ff7d`  
		Last Modified: Tue, 07 Apr 2026 02:38:04 GMT  
		Size: 42.1 MB (42078752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1127b79141bdf4702192334328307d206e11c6aa31d052e1a23797b019cd9227`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e77547b311d9fb65f8903175cf04e5cc5c5a83b89a0e2da0019f714e91518f`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 6.0 MB (6045630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e11cc2e00ad994abe260d5ad67dfd7491d4266f259fb05315a980488851c80`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600215398464d6cd5bb29d30abc13a266e4a12d8126c5190ad0350e31d5095e`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308cea664c0c58ae66f713e47f9fcfa93cd6b3d58923b00fbc4b983426bd718`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:ea36c0b2d597b14ac8970e16032efdf1a0cb0d0fd61aed56a44962c730fd428a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c056e8f74287d6dacfe03164e50b2b2ab903feb17e1fd90f1803861183181b`

```dockerfile
```

-	Layers:
	-	`sha256:6262f51f5062ebb2bf664a7edd66726710fadb66def54eb761ea06e7f85f0d7b`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 2.3 MB (2281972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f572ef13dddf9baf0bfc02b5007754aac61b224d1192f5b5cce4df8f4867580`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:f71d5e351b72e7080643d00c1cb42debfb7367ccce87e49e4314c8e98f2eb0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458af0a8e9243ed9d51a6ff0601606accae6cb5c314be65370c88c6e2177e213`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:11:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:13:48 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:13:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:13:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:13:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:13:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:13:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:13:49 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 02:58:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 02:58:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 02:58:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 02:58:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 02:58:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 02:58:14 GMT
USER fluent
# Tue, 07 Apr 2026 02:58:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8220afc2b68e6e2441c42d82813901ef61d54f0e858868c36c3612d0f61a341`  
		Last Modified: Tue, 07 Apr 2026 02:13:57 GMT  
		Size: 1.3 MB (1287482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fdd62850e20d9f1696e3113057a3b0eb0bdb0f9a4c9fdb88eb6a48d0f3de3d`  
		Last Modified: Tue, 07 Apr 2026 02:13:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000327029938d76c0a103cbdf0da6867dae4ab25f9bf2cca32934ae5aef4cd6`  
		Last Modified: Tue, 07 Apr 2026 02:14:01 GMT  
		Size: 37.7 MB (37661772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec682f2816027eb0ed1baf871971b8c84a53d2ff5fa00c51528c6060549421c`  
		Last Modified: Tue, 07 Apr 2026 02:13:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777517475398395007d48f1fa04ee2cccbb8e6318ef2a7e1ea4f637f3bbbd50f`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 6.0 MB (6027416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a27cad93f702fee81631e0fb1b3e29127c72e2029e0b2efe88c8cd7bb3a382`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c2494ca7bdadb78327be12121cd7cb1b03db4939073ad1648b796ae4a8b285`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facba3baf4499b30506b0806ae082c0064dbce45068f01ece331d0b48dd0c257`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:4a7704dc3805278c40c0a35a8307f6206601a6187a60eeccf92353c2987d13e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dea069ae02f1df9e010055368eb15d47748d2987673ffbcc01bb3140acc5fe`

```dockerfile
```

-	Layers:
	-	`sha256:052c3f5588970e59551554ee94604141d545b1e343406b49645d12a7248ed3f1`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 2.3 MB (2278888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330c4d027f478fbe798e139879f8147c758446000966eaf690cb24db14d17da6`  
		Last Modified: Tue, 07 Apr 2026 02:58:21 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:5ca27c30dabb58c53477d40b8ca406827f6300bd53bb3ade76b6ea09e8a92474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81012672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81aebf04b6260f3428764074def53f2349211f293c045a753766b9a5605afe7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 05:02:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 05:02:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 05:15:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 05:15:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 05:15:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 05:15:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 10:00:54 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 10:00:54 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 10:00:54 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 10:00:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 10:00:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 10:00:56 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 10:00:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 10:00:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 10:00:56 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 10:00:56 GMT
USER fluent
# Tue, 17 Mar 2026 10:00:56 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 10:00:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93820ad1ad41073212dddc80e0d6a6669254071632dab96b9d735edd949550f`  
		Last Modified: Tue, 17 Mar 2026 05:06:45 GMT  
		Size: 1.3 MB (1309779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ff3ee9989c0371a76ab538d2924e74397f4bb3f6ac768e15d4d5f03c96402e`  
		Last Modified: Tue, 17 Mar 2026 05:06:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109974bac0a835d036eb6e55dcad5291a70fcea494a2d03ace97ad3f98e43d44`  
		Last Modified: Tue, 17 Mar 2026 05:15:43 GMT  
		Size: 39.5 MB (39531800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad87bfd03039df023a7d263c23b46c6b986ce6468169d1c514b599f2c28a8f0`  
		Last Modified: Tue, 17 Mar 2026 05:15:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e23befd4447ac944e5e597c45bb016c354ad0d4cfb701b061d89ddfa22e702`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 6.6 MB (6575865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb279357921aae75c4b2280d8e3cf42a3920e93f2626c907357ac4a02a81bf8`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d73d2efba8ba8c2408b0c2bec3cbc19da7bd4a8fef8ae8342a524c24854d0b`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89f6cbf05c25c0aa3b13b42b9a208c0dd3649c68ea9d32941b142a7641e3cd8`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:15d80de4b5aead9c49246bbb15ef30c147c11b5cc5f1bdbb32160d7033cb5694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d4196d0d2e4c48d24d80a1aa76e5d18291d88849a8f61fce0445906000131c`

```dockerfile
```

-	Layers:
	-	`sha256:355d41fa1974e49c50fc3c1cf640e4efa6d2d459c80bb63b3d28a3b34492b917`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 2.3 MB (2285173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5965e9ff86788a8d995c45b05b9d73eb74cc77d985fbe196d3d183fe76c19c71`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:2f6961489a154b12a8b57595e6032f35ca07e24385b637fcd4646204e88fa6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76770974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0df4efcf86d4de2778e0e97599249ecce1aa9a16d50463561fb529dcde22f97`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:34:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 04:38:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 04:38:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 04:38:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:38:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 06:06:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 06:06:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 06:06:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 06:06:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 06:06:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 06:06:44 GMT
USER fluent
# Tue, 07 Apr 2026 06:06:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 06:06:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f1969e985ea39592094e95f8819f85d22b80808f05e339da5e17920cb7d05`  
		Last Modified: Tue, 07 Apr 2026 04:38:31 GMT  
		Size: 1.3 MB (1294728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b233ac00b24f834a7c3df8aed372379f83062378f27202d9f757b2504747185e`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0e908d5e1ac4b763f917e8f45d21b6b5822ecdcafcbcd10a3e2f156ce1d6e`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 39.2 MB (39206458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3b563c8673d991a48d188be4aaf4b921aced9bcb4638feed907718b6ef5dc4`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f737b275a09b30f87841b28577b17c902c2882c611244171c3e53a878c332`  
		Last Modified: Tue, 07 Apr 2026 06:06:58 GMT  
		Size: 6.4 MB (6431974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e238e6eab8962e5a6c9b89865fa14244ef03dd1c847435148e7de751c02a40b`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b0afeb97c9b9b8939b7ee8fcc6d94cbf03fdb12f18a1f5467abb2b26862920`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d13856a47ace03f81cc0aaa29c3102ab510bd97afcdfc1cdf8eb5bc3ec69e6`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:8435c6158f323083ad90c173a3b6cc1b8bc48bc952f34d1da7fc19d095a1d907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597c1ea3ff724140183fd893099f655117d120af93e0711ade84ec749f570141`

```dockerfile
```

-	Layers:
	-	`sha256:822b1fbf5b2de0999dd7426f6c87d0b382f23259963ddaad996a6b2aa7827ed6`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 2.3 MB (2283145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9350a8304d80d98fd56d5d4233b7eddd449129fbf6101b6914e4e1ac328dab37`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:6b94498ab5e6e3c98f6950102fb2565ccc028ba35886b6619e9d8a0c13f28c10
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
$ docker pull fluentd@sha256:65465303ccbcae716ddd9b9f903ccabc1f1d363413f7faacf339dba5fd504696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81808698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e294bc2f22d7acda198219be2b744031d207e9a08351cf70a7557e2034db37c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:30:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:32:54 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:32:54 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 02:32:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 02:32:54 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 02:32:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:32:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:32:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:32:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:32:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:32:54 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:33:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:33:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 03:33:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 03:33:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 03:33:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:33:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:33:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:33:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:33:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:33:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:33:41 GMT
USER fluent
# Tue, 07 Apr 2026 03:33:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:33:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a2f62ccbdd4f96866ec34d9038e30a7e3e2032812b0d14dc0b72d6c32839bb`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 3.5 MB (3510220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488e98f61afb008694e765a3e3cd336997f6441617c72b14f054323676671a3`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bc7dd9050b32d5189edd6dc83aafeeab67823832bc0cf9f88dbfdbe36f1de8`  
		Last Modified: Tue, 07 Apr 2026 02:33:05 GMT  
		Size: 35.8 MB (35781374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428046dab03b578219772e5157ba6906f54d3bbe6f50c55c2bd97a4a92733340`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d8031fccef1125397d42453e99f06bceaf376b5796af23ca89c79ecc4043d5`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 14.3 MB (14278374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0902dc64cda3c4bac7180654561609ec3cfd8459ee8f6d63f10ee49a9afe6ff`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6894273bebed7dab12d7e0581f405f14368cc4fcccc1cc85700f790bab82f2`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e957cec1091f9bd2e056264b252e4ca1261af7d1b7ef5b0bdb4fdf4acf634b7c`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:58543d969e5ed415cbfde4fb35276ec6f71a03aac1d6a83d25d44ce42723af01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36265f959d198310c86d530dbc8fbed6d3301b1700110173fab410f7d104593`

```dockerfile
```

-	Layers:
	-	`sha256:5b045d494467f8d0945277ec21bbc28a033ef5faf7f3014040dcf7050b92b098`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11bd2e5f6078021cffaa53e5a914ed9d5ad80b592a36db99c416f727737a31d`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3d97b1fbc8aa0beea936780ea9ecd6abecadad86ad8c4696ae46e6096e8504d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75193241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d02fffa1b423fdc566d9132781dcbae3d61fbef6af5e70c30136144bce91b9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:42:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:45:23 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:45:23 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 03:45:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 03:45:23 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 03:45:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:45:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:45:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:45:23 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:40:15 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:40:15 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 04:40:15 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 04:40:15 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 04:40:16 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:40:16 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:40:16 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:40:16 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:40:16 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:40:16 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:40:16 GMT
USER fluent
# Tue, 07 Apr 2026 04:40:16 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:40:16 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4748d6bbb5a5b9e671dcabe2f909bdd7514f760a5cfdcd37d5b04627424120f2`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 25.8 MB (25765667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b4426e57bea0b833df8594d2540044d7a21e1274e68bf45fa3cdf2e8fa0ac8`  
		Last Modified: Tue, 07 Apr 2026 03:45:31 GMT  
		Size: 3.1 MB (3081038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f153981f06f92b8d22f8da0e634bf0fe6714689fb7ab0bcfc1baf1b9c2b621f1`  
		Last Modified: Tue, 07 Apr 2026 03:45:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8b2805588972951a4fbc43a40b26713ce4e2f5ac1b697daa21190108858763`  
		Last Modified: Tue, 07 Apr 2026 03:45:33 GMT  
		Size: 32.1 MB (32079179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c367451fbd7179ee48ece11d1e1dc60497b8a415cf2e9a0f8ec2befab82ebcb7`  
		Last Modified: Tue, 07 Apr 2026 03:45:31 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a7da62daa7ba7c9c110fe412c5620d6ec0ae00f511a83059348ad234fc9357`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 14.3 MB (14264960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a26b6d2fdb9b65a99847d9ee56a3a1a67c933088b121b9d4889027d57096032`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1ac51bfdcedcfdcbdc630830107b20b37da6acfec83bde0d98fab248fe3eb`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abc9bf738e0cf785eed3f85e6c6e4e48a8e5670d0c3d29ee6c3c3832f206601`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:25602ed59bf650c3329f1d4cbbe92c67782124aacca3be7092ed0de17cce1f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4917a50adb0351f494868af013bc139e10e97606bdf760d0bf3f6c206a093b`

```dockerfile
```

-	Layers:
	-	`sha256:2b7d09b3c91bce5b4bc1bee1569c91131f06e8f613dd135b71851a06c832f383`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 2.7 MB (2674277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2928510fa6d11f2c40bf6577eea7f64ece689aa4cbda02bd582650d51a5ff31e`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:d2c065e7ec99b5cfb5422e5592a83bade68e83323eefa3e5a6467689073e8345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72950763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5cb05839d3d5d890f9bda839337feb3049e2cbf45f807668cc6a827c877652`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:16:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:16:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:23:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:23:53 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 03:23:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 03:23:53 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 03:23:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:23:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:23:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:23:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:23:53 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:35:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:35:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 04:35:28 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 04:35:28 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 04:35:29 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:35:29 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:35:29 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:35:29 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:35:29 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:35:29 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:35:29 GMT
USER fluent
# Tue, 07 Apr 2026 04:35:29 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:35:29 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44696ece9e073f10315496957fbd053f03d988a2cbc41378207739fc6f1fece4`  
		Last Modified: Tue, 07 Apr 2026 03:18:45 GMT  
		Size: 2.9 MB (2913806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044da362ff6c56b57b64acec7e2f7c31e3b9912f6f4e987e7c71d8df1e19b944`  
		Last Modified: Tue, 07 Apr 2026 03:18:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc8e815d6ae2ee8db531fc723385404da3e1ac706e43ab27101a062226208f`  
		Last Modified: Tue, 07 Apr 2026 03:24:02 GMT  
		Size: 31.9 MB (31910112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e36dd7e1aae93f70026fae2e3b261cfccc10cafa167c64166ddfb699c13f2`  
		Last Modified: Tue, 07 Apr 2026 03:24:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d4660fdb9b8144c48dcbeb62aa720e2433f5f375ef17c878052d478e3ce61`  
		Last Modified: Tue, 07 Apr 2026 04:35:38 GMT  
		Size: 14.2 MB (14182989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdd8290497aff4a70bba13116abddcc918cbeef0fddec91c896847cb38cbbd6`  
		Last Modified: Tue, 07 Apr 2026 04:35:38 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f54f640f50e661def023f7cf061ee10cf5f5d6a158b4de303ca36a2d690d346`  
		Last Modified: Tue, 07 Apr 2026 04:35:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4e0625babedae224222020862b08af39e87091e2c9a94f72eebfdd71e9ca8f`  
		Last Modified: Tue, 07 Apr 2026 04:35:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2470d04cf0f95dbd1c41c0d3f1966c1804c477aef362080448bad593f285019c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a04ba8a56dfc4af486b90049c0c64f98c6786bcd058119fae66d43016907eeb`

```dockerfile
```

-	Layers:
	-	`sha256:815362b74547c13f80ed3c12c84d3800af10b9068c22911abe6cb5874b9bc947`  
		Last Modified: Tue, 07 Apr 2026 04:35:38 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5df563d6a4e4b7cfbb07a690c13d0deda5dc08b5d46b29d7ff1de4084db4d80`  
		Last Modified: Tue, 07 Apr 2026 04:35:37 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a1e0c578950dfc0293cb8039eff68f62a612d90f9fd789148919e67495dc344a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81425738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb2aae52f25d19fbf5e03f8b5fb2378d1db9a7963bf8af9fad789c0a5058728`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:36:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:38:34 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:38:34 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 02:38:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 02:38:34 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 02:38:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:38:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:38:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:38:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:38:34 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:38:34 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:44:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:44:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 03:44:44 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 03:44:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 03:44:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:44:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:44:45 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:44:45 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:44:45 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:44:45 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:44:45 GMT
USER fluent
# Tue, 07 Apr 2026 03:44:45 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:44:45 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4b814341080ea0669ffdb8c1e02e5c2a116c4608d198a3d08f3c029924756b`  
		Last Modified: Tue, 07 Apr 2026 02:38:44 GMT  
		Size: 3.3 MB (3341530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46ba08e757dcafac0ac5f396798db88ed260293c5ee020748674a9f8f514b0`  
		Last Modified: Tue, 07 Apr 2026 02:38:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b295af23ac90626d176903210387bff25716d874ba37ab991dc39f79e83bd0a`  
		Last Modified: Tue, 07 Apr 2026 02:38:45 GMT  
		Size: 35.7 MB (35687819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a722297e2a7d7c8ca69099b282161bb3a9e93ee8805c99b7812a8929cd4fb64`  
		Last Modified: Tue, 07 Apr 2026 02:38:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df33d5042feeff57f560154db97d42380138a3e7e6f9410ea490fb41167d4177`  
		Last Modified: Tue, 07 Apr 2026 03:44:54 GMT  
		Size: 14.3 MB (14277829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0e531c28e28bb12a97feffcaea382a38bbe83d14fa5d4643fe39d3d134941f`  
		Last Modified: Tue, 07 Apr 2026 03:44:54 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0808072d1a66cdabc812de81e2311dca06f09687f5174f166e64083c9c56a8bf`  
		Last Modified: Tue, 07 Apr 2026 03:44:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb40f776fd95052564c5c157480d65019fd2c255ccb0f72588c20a7e966fe7f`  
		Last Modified: Tue, 07 Apr 2026 03:44:54 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1dc9f7c777845e21e3531ca7379d680b225e0891efda0ef35d224cbe073c83a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709101465fbccffa5ea2e6f4ded175e5054b627dfb8ab0e8dc9327a9cfde5a8c`

```dockerfile
```

-	Layers:
	-	`sha256:be1bd74020a3f4af1305fd9e8fc35c4531f7a38842d80f06907687135fc332cc`  
		Last Modified: Tue, 07 Apr 2026 03:44:54 GMT  
		Size: 2.7 MB (2670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7c763d632466ae433740529b2c080146abf72188db097b5d3f7a21c65be9bc`  
		Last Modified: Tue, 07 Apr 2026 03:44:53 GMT  
		Size: 21.2 KB (21166 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:654a495fc96a6f2e756d2b6f7569bcad8990894168dd96ad68cd284368ebeb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78687829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c59be4743b967d692e9fc7ec43170d56d61eb3b31e164358b2ac1abd069d08`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:11:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:16:31 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:16:31 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 02:16:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 02:16:31 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 02:16:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:16:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:16:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:16:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:16:31 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:16:31 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 02:58:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 02:58:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 02:58:06 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 02:58:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 02:58:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 02:58:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 02:58:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 02:58:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 02:58:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 02:58:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 02:58:06 GMT
USER fluent
# Tue, 07 Apr 2026 02:58:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e032c0f3018bbbf4f40485135f2cdb496ef1c7813c589d6503b9798b4a9ef61`  
		Last Modified: Tue, 07 Apr 2026 02:14:18 GMT  
		Size: 3.5 MB (3512891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eea1bf52869be0bf678d06b5ef1ca88485cd974a173eba58f4be09f4a8d932a`  
		Last Modified: Tue, 07 Apr 2026 02:14:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17324062944fc9aa65bedba6ba0dc9ffcd23437f3b33c19adcb829274c4e2f25`  
		Last Modified: Tue, 07 Apr 2026 02:16:42 GMT  
		Size: 31.9 MB (31884179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065f640d820cc19feaef5f4a079b4e65e99e443f96cfb20daf61a6fdaff1b086`  
		Last Modified: Tue, 07 Apr 2026 02:16:39 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae8c7a5a6f06e9df87f6032435602838a1624fd17d7085449ee2d8d5447161d`  
		Last Modified: Tue, 07 Apr 2026 02:58:14 GMT  
		Size: 14.1 MB (14066596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae40a0df8a00ec3a4575538bbc8cbfd263d4f2e710f7258893260dafc342583`  
		Last Modified: Tue, 07 Apr 2026 02:58:14 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04569b8abd6c08e265017ae54689befa9ae98846c698d7929e970151ef51e80e`  
		Last Modified: Tue, 07 Apr 2026 02:58:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c1b2af524e4b7a6339f60653bc70216ad2454966be305366c0e9910cad220`  
		Last Modified: Tue, 07 Apr 2026 02:58:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:e8a744b890d282139476a739d794aaf4cbf49e52927f816049dc67256f5c6098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328bcc772d9a437592a393bb6743305458a8c0cb5d2f5936e58d2f83065a8376`

```dockerfile
```

-	Layers:
	-	`sha256:f072166cbfdd6d0c73829f7243f9c9998aba2a3fed29c1373028497da41cf5d1`  
		Last Modified: Tue, 07 Apr 2026 02:58:13 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:febb624dd4b749f22a509213feb224b1c3e55b3160cdf72811f41e0c483aa36b`  
		Last Modified: Tue, 07 Apr 2026 02:58:13 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8f9be2d3ac054b0b505fe3587123183d00781bbb014e77e26248ac5faf5e6a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84100073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5256e761f2b662974b128b1295202d837aa771f62984e3c1a7382819719265`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Thu, 26 Mar 2026 18:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Mar 2026 18:31:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:37:54 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:37:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:37:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:37:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:37:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:37:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:37:55 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:38:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:38:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:38:43 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:38:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:38:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:38:45 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:38:48 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:38:48 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:38:48 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:38:48 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:38:48 GMT
USER fluent
# Fri, 27 Mar 2026 19:38:48 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:38:48 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6dd432af990aeed0dd4fd76d6d1fe507bfd33f78826731a1300e5c6f93423f`  
		Last Modified: Thu, 26 Mar 2026 18:35:43 GMT  
		Size: 3.7 MB (3710764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73847511305cedc00f17cc76877ca78c47c8d883a71664a7a3430ea3065709fa`  
		Last Modified: Thu, 26 Mar 2026 18:35:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec79745a4682555cfd3bbd00deced64e2558785bed015802f59239a475cc4c3`  
		Last Modified: Fri, 27 Mar 2026 18:38:14 GMT  
		Size: 33.6 MB (33627300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaf3905224c31d262cdb12adc36066b5968e6248de1c9d70415996c492692f0`  
		Last Modified: Fri, 27 Mar 2026 18:38:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c917494d478356534ce5f21e72f00784c81c8ba3f12d3852e9cbe0dd7bce87a9`  
		Last Modified: Fri, 27 Mar 2026 19:39:10 GMT  
		Size: 14.7 MB (14681243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310ec82e0f0c2b233061b98988fcfadc3cc5ea0fa441ef0160091c5b975b00e6`  
		Last Modified: Fri, 27 Mar 2026 19:39:10 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322746ba42505e58bdfd482e1f90cb841219d197d7b790aeeeb8fcb2850cf150`  
		Last Modified: Fri, 27 Mar 2026 19:39:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f1dcaa24632076c7c7353dd6a098b9149cbb12e7fce605b609850ab0fcc11e`  
		Last Modified: Fri, 27 Mar 2026 19:39:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d08973970efabecb7030eddf8191faf12d79abd70a2d113def9296e27cd9c290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3870cbfd60fc2fadd0d6ab1f03d2c13bb45122c8473f0f5bda92531b9e1e0363`

```dockerfile
```

-	Layers:
	-	`sha256:dd0f7f181cced10abd787cf0f2f4478cd6cda699ac7409f653431388839bee3b`  
		Last Modified: Fri, 27 Mar 2026 19:39:10 GMT  
		Size: 2.7 MB (2674899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:997817d36b72965e05fe07e086b1431920cb8e1a352bb26eb081434a946e407a`  
		Last Modified: Fri, 27 Mar 2026 19:39:09 GMT  
		Size: 21.1 KB (21105 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:bb456788472dc70bb260812388d7a9db0f41d18f3b5b4943bbd5238ddd70b308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77346182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979705190ed67c1709fb558609ff58883601a20a522a76e3b107bb7d87ada4b5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:36:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 04:42:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:42:32 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 04:42:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 04:42:32 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 04:42:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 04:42:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 04:42:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 04:42:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:42:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 04:42:33 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 06:06:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 06:06:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 06:06:56 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 06:06:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 06:06:56 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 06:06:56 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 06:06:56 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 06:06:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 06:06:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 06:06:56 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 06:06:56 GMT
USER fluent
# Tue, 07 Apr 2026 06:06:56 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 06:06:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c644c009cfb244ea86a1dd8f34039561e8c632c7ea9de18b7b84dda34374e973`  
		Last Modified: Tue, 07 Apr 2026 04:39:57 GMT  
		Size: 3.2 MB (3171201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e626e8e24686904fb217e122f4ad73975d089b96576c84e8dd4904151e7b`  
		Last Modified: Tue, 07 Apr 2026 04:39:57 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcc7a4af710710def677b25912742abb4fd1f37371b39f72f60d402321739d5`  
		Last Modified: Tue, 07 Apr 2026 04:42:46 GMT  
		Size: 32.9 MB (32875073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f6cee55d8c5d810d030694681a087d227079477d66536d54c121d6fc586091`  
		Last Modified: Tue, 07 Apr 2026 04:42:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07787258b5b8a12131e42c9301ac07377f935a93c12fd0e42643d56c56e2134e`  
		Last Modified: Tue, 07 Apr 2026 06:07:10 GMT  
		Size: 14.4 MB (14405882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3aaf72bd67a179a3f05b1cf084d32f94d6387830b905108e4a0eb3a6362169`  
		Last Modified: Tue, 07 Apr 2026 06:07:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e03072ea5a8ec9ec64cb7143ddc28ea5d768fcefa164347d8de146a30394c4`  
		Last Modified: Tue, 07 Apr 2026 06:07:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423d60747685ad9b144f542fba16d3fa74eb4ef90c5d6e281553b78199036bf6`  
		Last Modified: Tue, 07 Apr 2026 06:07:10 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7171e307caff7c037016af576fbfde75cbe4e569f87e304c5307cef21606835d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b9898a78a1cb860123c03d72274834d6f4ab58c7a3a3f3cd276798c10fe42c`

```dockerfile
```

-	Layers:
	-	`sha256:25e7f4ce2d2f6ec02e1d6afa4f8a3d33637f73853bd465bde1f121bc3e3cddc6`  
		Last Modified: Tue, 07 Apr 2026 06:07:09 GMT  
		Size: 2.7 MB (2667307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4caab2bfa0356427498646fbe06e300e9c045ac31a85f3cd4da2c2a4da8c7f3c`  
		Last Modified: Tue, 07 Apr 2026 06:07:10 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.11-debian-1.0`

```console
$ docker pull fluentd@sha256:6b94498ab5e6e3c98f6950102fb2565ccc028ba35886b6619e9d8a0c13f28c10
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
$ docker pull fluentd@sha256:65465303ccbcae716ddd9b9f903ccabc1f1d363413f7faacf339dba5fd504696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81808698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e294bc2f22d7acda198219be2b744031d207e9a08351cf70a7557e2034db37c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:30:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:30:48 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:32:54 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:32:54 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 02:32:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 02:32:54 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 02:32:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:32:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:32:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:32:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:32:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:32:54 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:33:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:33:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 03:33:40 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 03:33:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 03:33:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:33:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:33:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:33:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:33:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:33:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:33:41 GMT
USER fluent
# Tue, 07 Apr 2026 03:33:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:33:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a2f62ccbdd4f96866ec34d9038e30a7e3e2032812b0d14dc0b72d6c32839bb`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 3.5 MB (3510220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488e98f61afb008694e765a3e3cd336997f6441617c72b14f054323676671a3`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bc7dd9050b32d5189edd6dc83aafeeab67823832bc0cf9f88dbfdbe36f1de8`  
		Last Modified: Tue, 07 Apr 2026 02:33:05 GMT  
		Size: 35.8 MB (35781374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428046dab03b578219772e5157ba6906f54d3bbe6f50c55c2bd97a4a92733340`  
		Last Modified: Tue, 07 Apr 2026 02:33:03 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d8031fccef1125397d42453e99f06bceaf376b5796af23ca89c79ecc4043d5`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 14.3 MB (14278374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0902dc64cda3c4bac7180654561609ec3cfd8459ee8f6d63f10ee49a9afe6ff`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6894273bebed7dab12d7e0581f405f14368cc4fcccc1cc85700f790bab82f2`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e957cec1091f9bd2e056264b252e4ca1261af7d1b7ef5b0bdb4fdf4acf634b7c`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:58543d969e5ed415cbfde4fb35276ec6f71a03aac1d6a83d25d44ce42723af01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36265f959d198310c86d530dbc8fbed6d3301b1700110173fab410f7d104593`

```dockerfile
```

-	Layers:
	-	`sha256:5b045d494467f8d0945277ec21bbc28a033ef5faf7f3014040dcf7050b92b098`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 2.7 MB (2670482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11bd2e5f6078021cffaa53e5a914ed9d5ad80b592a36db99c416f727737a31d`  
		Last Modified: Tue, 07 Apr 2026 03:33:50 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3d97b1fbc8aa0beea936780ea9ecd6abecadad86ad8c4696ae46e6096e8504d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75193241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d02fffa1b423fdc566d9132781dcbae3d61fbef6af5e70c30136144bce91b9`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:42:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:42:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:45:23 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:45:23 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 03:45:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 03:45:23 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 03:45:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:45:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:45:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:45:23 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:40:15 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:40:15 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 04:40:15 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 04:40:15 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 04:40:16 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:40:16 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:40:16 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:40:16 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:40:16 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:40:16 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:40:16 GMT
USER fluent
# Tue, 07 Apr 2026 04:40:16 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:40:16 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4748d6bbb5a5b9e671dcabe2f909bdd7514f760a5cfdcd37d5b04627424120f2`  
		Last Modified: Tue, 07 Apr 2026 00:10:57 GMT  
		Size: 25.8 MB (25765667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b4426e57bea0b833df8594d2540044d7a21e1274e68bf45fa3cdf2e8fa0ac8`  
		Last Modified: Tue, 07 Apr 2026 03:45:31 GMT  
		Size: 3.1 MB (3081038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f153981f06f92b8d22f8da0e634bf0fe6714689fb7ab0bcfc1baf1b9c2b621f1`  
		Last Modified: Tue, 07 Apr 2026 03:45:31 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8b2805588972951a4fbc43a40b26713ce4e2f5ac1b697daa21190108858763`  
		Last Modified: Tue, 07 Apr 2026 03:45:33 GMT  
		Size: 32.1 MB (32079179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c367451fbd7179ee48ece11d1e1dc60497b8a415cf2e9a0f8ec2befab82ebcb7`  
		Last Modified: Tue, 07 Apr 2026 03:45:31 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a7da62daa7ba7c9c110fe412c5620d6ec0ae00f511a83059348ad234fc9357`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 14.3 MB (14264960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a26b6d2fdb9b65a99847d9ee56a3a1a67c933088b121b9d4889027d57096032`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff1ac51bfdcedcfdcbdc630830107b20b37da6acfec83bde0d98fab248fe3eb`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abc9bf738e0cf785eed3f85e6c6e4e48a8e5670d0c3d29ee6c3c3832f206601`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:25602ed59bf650c3329f1d4cbbe92c67782124aacca3be7092ed0de17cce1f39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4917a50adb0351f494868af013bc139e10e97606bdf760d0bf3f6c206a093b`

```dockerfile
```

-	Layers:
	-	`sha256:2b7d09b3c91bce5b4bc1bee1569c91131f06e8f613dd135b71851a06c832f383`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 2.7 MB (2674277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2928510fa6d11f2c40bf6577eea7f64ece689aa4cbda02bd582650d51a5ff31e`  
		Last Modified: Tue, 07 Apr 2026 04:40:24 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:d2c065e7ec99b5cfb5422e5592a83bade68e83323eefa3e5a6467689073e8345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72950763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df5cb05839d3d5d890f9bda839337feb3049e2cbf45f807668cc6a827c877652`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:16:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:16:04 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:23:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:23:53 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 03:23:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 03:23:53 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 03:23:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:23:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:23:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:23:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:23:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:23:53 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:35:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:35:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 04:35:28 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 04:35:28 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 04:35:29 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:35:29 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:35:29 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:35:29 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:35:29 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:35:29 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:35:29 GMT
USER fluent
# Tue, 07 Apr 2026 04:35:29 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:35:29 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44696ece9e073f10315496957fbd053f03d988a2cbc41378207739fc6f1fece4`  
		Last Modified: Tue, 07 Apr 2026 03:18:45 GMT  
		Size: 2.9 MB (2913806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044da362ff6c56b57b64acec7e2f7c31e3b9912f6f4e987e7c71d8df1e19b944`  
		Last Modified: Tue, 07 Apr 2026 03:18:45 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fc8e815d6ae2ee8db531fc723385404da3e1ac706e43ab27101a062226208f`  
		Last Modified: Tue, 07 Apr 2026 03:24:02 GMT  
		Size: 31.9 MB (31910112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417e36dd7e1aae93f70026fae2e3b261cfccc10cafa167c64166ddfb699c13f2`  
		Last Modified: Tue, 07 Apr 2026 03:24:01 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52d4660fdb9b8144c48dcbeb62aa720e2433f5f375ef17c878052d478e3ce61`  
		Last Modified: Tue, 07 Apr 2026 04:35:38 GMT  
		Size: 14.2 MB (14182989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdd8290497aff4a70bba13116abddcc918cbeef0fddec91c896847cb38cbbd6`  
		Last Modified: Tue, 07 Apr 2026 04:35:38 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f54f640f50e661def023f7cf061ee10cf5f5d6a158b4de303ca36a2d690d346`  
		Last Modified: Tue, 07 Apr 2026 04:35:38 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4e0625babedae224222020862b08af39e87091e2c9a94f72eebfdd71e9ca8f`  
		Last Modified: Tue, 07 Apr 2026 04:35:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2470d04cf0f95dbd1c41c0d3f1966c1804c477aef362080448bad593f285019c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a04ba8a56dfc4af486b90049c0c64f98c6786bcd058119fae66d43016907eeb`

```dockerfile
```

-	Layers:
	-	`sha256:815362b74547c13f80ed3c12c84d3800af10b9068c22911abe6cb5874b9bc947`  
		Last Modified: Tue, 07 Apr 2026 04:35:38 GMT  
		Size: 2.7 MB (2672708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5df563d6a4e4b7cfbb07a690c13d0deda5dc08b5d46b29d7ff1de4084db4d80`  
		Last Modified: Tue, 07 Apr 2026 04:35:37 GMT  
		Size: 21.1 KB (21149 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a1e0c578950dfc0293cb8039eff68f62a612d90f9fd789148919e67495dc344a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81425738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb2aae52f25d19fbf5e03f8b5fb2378d1db9a7963bf8af9fad789c0a5058728`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:36:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:36:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:38:34 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:38:34 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 02:38:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 02:38:34 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 02:38:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:38:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:38:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:38:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:38:34 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:38:34 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:44:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:44:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 03:44:44 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 03:44:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 03:44:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:44:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:44:45 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:44:45 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:44:45 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:44:45 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:44:45 GMT
USER fluent
# Tue, 07 Apr 2026 03:44:45 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:44:45 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4b814341080ea0669ffdb8c1e02e5c2a116c4608d198a3d08f3c029924756b`  
		Last Modified: Tue, 07 Apr 2026 02:38:44 GMT  
		Size: 3.3 MB (3341530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab46ba08e757dcafac0ac5f396798db88ed260293c5ee020748674a9f8f514b0`  
		Last Modified: Tue, 07 Apr 2026 02:38:44 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b295af23ac90626d176903210387bff25716d874ba37ab991dc39f79e83bd0a`  
		Last Modified: Tue, 07 Apr 2026 02:38:45 GMT  
		Size: 35.7 MB (35687819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a722297e2a7d7c8ca69099b282161bb3a9e93ee8805c99b7812a8929cd4fb64`  
		Last Modified: Tue, 07 Apr 2026 02:38:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df33d5042feeff57f560154db97d42380138a3e7e6f9410ea490fb41167d4177`  
		Last Modified: Tue, 07 Apr 2026 03:44:54 GMT  
		Size: 14.3 MB (14277829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0e531c28e28bb12a97feffcaea382a38bbe83d14fa5d4643fe39d3d134941f`  
		Last Modified: Tue, 07 Apr 2026 03:44:54 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0808072d1a66cdabc812de81e2311dca06f09687f5174f166e64083c9c56a8bf`  
		Last Modified: Tue, 07 Apr 2026 03:44:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb40f776fd95052564c5c157480d65019fd2c255ccb0f72588c20a7e966fe7f`  
		Last Modified: Tue, 07 Apr 2026 03:44:54 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1dc9f7c777845e21e3531ca7379d680b225e0891efda0ef35d224cbe073c83a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709101465fbccffa5ea2e6f4ded175e5054b627dfb8ab0e8dc9327a9cfde5a8c`

```dockerfile
```

-	Layers:
	-	`sha256:be1bd74020a3f4af1305fd9e8fc35c4531f7a38842d80f06907687135fc332cc`  
		Last Modified: Tue, 07 Apr 2026 03:44:54 GMT  
		Size: 2.7 MB (2670722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7c763d632466ae433740529b2c080146abf72188db097b5d3f7a21c65be9bc`  
		Last Modified: Tue, 07 Apr 2026 03:44:53 GMT  
		Size: 21.2 KB (21166 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:654a495fc96a6f2e756d2b6f7569bcad8990894168dd96ad68cd284368ebeb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78687829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c59be4743b967d692e9fc7ec43170d56d61eb3b31e164358b2ac1abd069d08`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:11:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:16:31 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:16:31 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 02:16:31 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 02:16:31 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 02:16:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:16:31 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:16:31 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:16:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:16:31 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:16:31 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 02:58:06 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 02:58:06 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 02:58:06 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 02:58:06 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 02:58:06 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 02:58:06 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 02:58:06 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 02:58:06 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 02:58:06 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 02:58:06 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 02:58:06 GMT
USER fluent
# Tue, 07 Apr 2026 02:58:06 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:06 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e032c0f3018bbbf4f40485135f2cdb496ef1c7813c589d6503b9798b4a9ef61`  
		Last Modified: Tue, 07 Apr 2026 02:14:18 GMT  
		Size: 3.5 MB (3512891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eea1bf52869be0bf678d06b5ef1ca88485cd974a173eba58f4be09f4a8d932a`  
		Last Modified: Tue, 07 Apr 2026 02:14:18 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17324062944fc9aa65bedba6ba0dc9ffcd23437f3b33c19adcb829274c4e2f25`  
		Last Modified: Tue, 07 Apr 2026 02:16:42 GMT  
		Size: 31.9 MB (31884179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065f640d820cc19feaef5f4a079b4e65e99e443f96cfb20daf61a6fdaff1b086`  
		Last Modified: Tue, 07 Apr 2026 02:16:39 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae8c7a5a6f06e9df87f6032435602838a1624fd17d7085449ee2d8d5447161d`  
		Last Modified: Tue, 07 Apr 2026 02:58:14 GMT  
		Size: 14.1 MB (14066596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae40a0df8a00ec3a4575538bbc8cbfd263d4f2e710f7258893260dafc342583`  
		Last Modified: Tue, 07 Apr 2026 02:58:14 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04569b8abd6c08e265017ae54689befa9ae98846c698d7929e970151ef51e80e`  
		Last Modified: Tue, 07 Apr 2026 02:58:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c1b2af524e4b7a6339f60653bc70216ad2454966be305366c0e9910cad220`  
		Last Modified: Tue, 07 Apr 2026 02:58:14 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:e8a744b890d282139476a739d794aaf4cbf49e52927f816049dc67256f5c6098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328bcc772d9a437592a393bb6743305458a8c0cb5d2f5936e58d2f83065a8376`

```dockerfile
```

-	Layers:
	-	`sha256:f072166cbfdd6d0c73829f7243f9c9998aba2a3fed29c1373028497da41cf5d1`  
		Last Modified: Tue, 07 Apr 2026 02:58:13 GMT  
		Size: 2.7 MB (2667661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:febb624dd4b749f22a509213feb224b1c3e55b3160cdf72811f41e0c483aa36b`  
		Last Modified: Tue, 07 Apr 2026 02:58:13 GMT  
		Size: 21.0 KB (21047 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8f9be2d3ac054b0b505fe3587123183d00781bbb014e77e26248ac5faf5e6a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84100073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5256e761f2b662974b128b1295202d837aa771f62984e3c1a7382819719265`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Thu, 26 Mar 2026 18:31:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Mar 2026 18:31:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 27 Mar 2026 18:37:54 GMT
ENV LANG=C.UTF-8
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_VERSION=3.2.11
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Fri, 27 Mar 2026 18:37:54 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Fri, 27 Mar 2026 18:37:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 27 Mar 2026 18:37:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 27 Mar 2026 18:37:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 27 Mar 2026 18:37:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Mar 2026 18:37:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 27 Mar 2026 18:37:55 GMT
CMD ["irb"]
# Fri, 27 Mar 2026 19:38:43 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 27 Mar 2026 19:38:43 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Fri, 27 Mar 2026 19:38:43 GMT
ENV TINI_VERSION=0.18.0
# Fri, 27 Mar 2026 19:38:43 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 27 Mar 2026 19:38:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 27 Mar 2026 19:38:45 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 27 Mar 2026 19:38:48 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 27 Mar 2026 19:38:48 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 27 Mar 2026 19:38:48 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 27 Mar 2026 19:38:48 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 27 Mar 2026 19:38:48 GMT
USER fluent
# Fri, 27 Mar 2026 19:38:48 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 27 Mar 2026 19:38:48 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6dd432af990aeed0dd4fd76d6d1fe507bfd33f78826731a1300e5c6f93423f`  
		Last Modified: Thu, 26 Mar 2026 18:35:43 GMT  
		Size: 3.7 MB (3710764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73847511305cedc00f17cc76877ca78c47c8d883a71664a7a3430ea3065709fa`  
		Last Modified: Thu, 26 Mar 2026 18:35:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec79745a4682555cfd3bbd00deced64e2558785bed015802f59239a475cc4c3`  
		Last Modified: Fri, 27 Mar 2026 18:38:14 GMT  
		Size: 33.6 MB (33627300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaf3905224c31d262cdb12adc36066b5968e6248de1c9d70415996c492692f0`  
		Last Modified: Fri, 27 Mar 2026 18:38:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c917494d478356534ce5f21e72f00784c81c8ba3f12d3852e9cbe0dd7bce87a9`  
		Last Modified: Fri, 27 Mar 2026 19:39:10 GMT  
		Size: 14.7 MB (14681243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310ec82e0f0c2b233061b98988fcfadc3cc5ea0fa441ef0160091c5b975b00e6`  
		Last Modified: Fri, 27 Mar 2026 19:39:10 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322746ba42505e58bdfd482e1f90cb841219d197d7b790aeeeb8fcb2850cf150`  
		Last Modified: Fri, 27 Mar 2026 19:39:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f1dcaa24632076c7c7353dd6a098b9149cbb12e7fce605b609850ab0fcc11e`  
		Last Modified: Fri, 27 Mar 2026 19:39:10 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:d08973970efabecb7030eddf8191faf12d79abd70a2d113def9296e27cd9c290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3870cbfd60fc2fadd0d6ab1f03d2c13bb45122c8473f0f5bda92531b9e1e0363`

```dockerfile
```

-	Layers:
	-	`sha256:dd0f7f181cced10abd787cf0f2f4478cd6cda699ac7409f653431388839bee3b`  
		Last Modified: Fri, 27 Mar 2026 19:39:10 GMT  
		Size: 2.7 MB (2674899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:997817d36b72965e05fe07e086b1431920cb8e1a352bb26eb081434a946e407a`  
		Last Modified: Fri, 27 Mar 2026 19:39:09 GMT  
		Size: 21.1 KB (21105 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:bb456788472dc70bb260812388d7a9db0f41d18f3b5b4943bbd5238ddd70b308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77346182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979705190ed67c1709fb558609ff58883601a20a522a76e3b107bb7d87ada4b5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 04:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:36:41 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 04:42:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:42:32 GMT
ENV RUBY_VERSION=3.2.11
# Tue, 07 Apr 2026 04:42:32 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.11.tar.xz
# Tue, 07 Apr 2026 04:42:32 GMT
ENV RUBY_DOWNLOAD_SHA256=c13aec0c206725d5d356acbae6e5fd8bffd92dc325aec14fd5dd7795d4b763d2
# Tue, 07 Apr 2026 04:42:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 04:42:32 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 04:42:32 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 04:42:32 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:42:33 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 04:42:33 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 06:06:56 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 06:06:56 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Tue, 07 Apr 2026 06:06:56 GMT
ENV TINI_VERSION=0.18.0
# Tue, 07 Apr 2026 06:06:56 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Tue, 07 Apr 2026 06:06:56 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 06:06:56 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 06:06:56 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 06:06:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 06:06:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 06:06:56 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 06:06:56 GMT
USER fluent
# Tue, 07 Apr 2026 06:06:56 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 06:06:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c644c009cfb244ea86a1dd8f34039561e8c632c7ea9de18b7b84dda34374e973`  
		Last Modified: Tue, 07 Apr 2026 04:39:57 GMT  
		Size: 3.2 MB (3171201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b665e626e8e24686904fb217e122f4ad73975d089b96576c84e8dd4904151e7b`  
		Last Modified: Tue, 07 Apr 2026 04:39:57 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bcc7a4af710710def677b25912742abb4fd1f37371b39f72f60d402321739d5`  
		Last Modified: Tue, 07 Apr 2026 04:42:46 GMT  
		Size: 32.9 MB (32875073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f6cee55d8c5d810d030694681a087d227079477d66536d54c121d6fc586091`  
		Last Modified: Tue, 07 Apr 2026 04:42:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07787258b5b8a12131e42c9301ac07377f935a93c12fd0e42643d56c56e2134e`  
		Last Modified: Tue, 07 Apr 2026 06:07:10 GMT  
		Size: 14.4 MB (14405882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3aaf72bd67a179a3f05b1cf084d32f94d6387830b905108e4a0eb3a6362169`  
		Last Modified: Tue, 07 Apr 2026 06:07:09 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e03072ea5a8ec9ec64cb7143ddc28ea5d768fcefa164347d8de146a30394c4`  
		Last Modified: Tue, 07 Apr 2026 06:07:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423d60747685ad9b144f542fba16d3fa74eb4ef90c5d6e281553b78199036bf6`  
		Last Modified: Tue, 07 Apr 2026 06:07:10 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7171e307caff7c037016af576fbfde75cbe4e569f87e304c5307cef21606835d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b9898a78a1cb860123c03d72274834d6f4ab58c7a3a3f3cd276798c10fe42c`

```dockerfile
```

-	Layers:
	-	`sha256:25e7f4ce2d2f6ec02e1d6afa4f8a3d33637f73853bd465bde1f121bc3e3cddc6`  
		Last Modified: Tue, 07 Apr 2026 06:07:09 GMT  
		Size: 2.7 MB (2667307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4caab2bfa0356427498646fbe06e300e9c045ac31a85f3cd4da2c2a4da8c7f3c`  
		Last Modified: Tue, 07 Apr 2026 06:07:10 GMT  
		Size: 21.1 KB (21072 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:dcbc40508693421a01428cd5112d60c5726c0e79ca9ed870d4e668aeee718ccb
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
$ docker pull fluentd@sha256:2f4043c322f55eec6c6708e4efd629c144448e0a196244c1902a0f1a6c43e721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79240276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d713ba17c405e8e96c3994d35aef5158cf916d53682838c284731869598b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:28:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:31:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:31:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:31:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:33:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:33:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 03:33:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:33:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:33:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:33:51 GMT
USER fluent
# Tue, 07 Apr 2026 03:33:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:33:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78c84e44d70408c199a2896d0fe6d15b64efcceafe0e09550d5177ecdab72b5`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 1.3 MB (1279868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c086a7638e3fda68aac0522c41b07f5f10ac23fed584ee16a13498e0a4947d`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b6e55e1373be9c47416cd4ec47847af123c40d71aaeeb5c34653eb3e287ceb`  
		Last Modified: Tue, 07 Apr 2026 02:31:37 GMT  
		Size: 42.1 MB (42127244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2e954b41c2ddc19fb451b0eacc5ef3bbf6542b210296a77ae759a1277d7d38`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2f4817d01410fa0935c2ac51032921ff607e7de054d59d4cce546f23f28273`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 6.1 MB (6055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287ffb4f171600c7eaad32b94171730f57d10ee2704dc3f2d14f2ad79786dfb5`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ab56bccb331339769e77903e049fb948862d2955c250bc976c836191f85d5d`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e04c8092324d16d133bf8a28c5ecbd2a61e71e004a3732458aa69a376d141b`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bd420eafe75e77c9b004aec3deedb09835a4aa36c85624938eb39fd5e3965b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa3403daf8ff28a64fa6d7bb54ee31b8e3672d3c5ba284d163bad93de84c4bc`

```dockerfile
```

-	Layers:
	-	`sha256:4ea95f6fc3952ecf0f8d41802f1f42d8aeacfe1e3f3954bfb29d13bc89c83b77`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 2.3 MB (2281700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e469a7bf6b1dbca433e02e1e6cfafc8563fc1568ec1f275b79b96f94afa2a287`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:737d41da6bfb0ce9ebc6ada5309f93a3c66b48aa251d12b62c1338633d2b906c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73091229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fddf682d8379469a82e2365369a447e62450bf54b18d429978c6bdea48fce26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:42:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:42:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 03:45:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:45:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:40:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:40:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 04:40:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:40:17 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:40:17 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:40:17 GMT
USER fluent
# Tue, 07 Apr 2026 04:40:17 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:40:17 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f83fcfefaffee8aa367effced408a0e6a87a5e59cdee33c2ca23721e3666bb`  
		Last Modified: Tue, 07 Apr 2026 03:45:13 GMT  
		Size: 1.3 MB (1263659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9350562d97a8b76eee53f9378f84c348e2e8ce41eb494a8f9acfd953ee73661d`  
		Last Modified: Tue, 07 Apr 2026 03:45:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff55ef1d37d6eddef2754669cb01a902319f33e3b5835659ce3c7fbe987cf169`  
		Last Modified: Tue, 07 Apr 2026 03:45:14 GMT  
		Size: 37.9 MB (37924109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db8d12e894040067d04d239a563bb338afdefd7e3ab192ce444708a3e277ac`  
		Last Modified: Tue, 07 Apr 2026 03:45:12 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594bfd195b76e112143930963588f6fc3d3585286f3a7be63979448e52d19bfa`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 6.0 MB (5957259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a637356205a8b660cd31964cf17283ddf1c0f2f1e8d40211a9b693f0fe4f18e`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34cdc5b6faa040070007317eaf98b4c1a3767447b6a72c5856e9fb68ac2cbc1`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc11c1d16b742a1ca4e45e2a3dd99b84782bfb227a6332cab341ed34dfd39ad0`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4ff05bbc8133861b058fbd1d7a8f5afe687d1fa480c668942864f709ec142794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aaed9763b5c76a7ae5965cd090e83cb34052428ced62536562e131a965a9c3`

```dockerfile
```

-	Layers:
	-	`sha256:41c7bea2c8853c86ec41712b331858bf289f07d6f25b7985e8a9bbb031dfb61a`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 2.3 MB (2284671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2589f3eaa3dee5c0c385b127f1f2689c74618d980ec8b9305bba92d694b08048`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:e79ade4311d7653af470029e4dd6340fe8bd1dbc7feb9be95a6aa1ccc787bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70955862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e1393d31b464a3412ae704c38cafaddbb09bbde369bdfc9bf352677d315dc4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:17:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 03:19:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:19:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:19:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:19:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:35:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:35:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 04:35:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:35:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:35:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:35:40 GMT
USER fluent
# Tue, 07 Apr 2026 04:35:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:35:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66e9f844a8fcc6c0af5b1c95ad1e0c477f48277d9bfab72116a2780faf5f9e`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 1.2 MB (1237567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fb85dc50c757ea6577b3fef8fabfe4a5abb87834dc45f032c1f9a56274f658`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dba43d16f47f9f243dd54e854300da3d235512c9a3641611cbfb6a1de8acdbc`  
		Last Modified: Tue, 07 Apr 2026 03:20:07 GMT  
		Size: 37.8 MB (37781086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7219bd5fc4e67916c070402dd93cca9ba0ab97e52a6923882144b109de88b3c`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141b3b04696ed9a81f5a230237c23991f9fecd1a7624de095ed4d3410499d3f9`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 5.7 MB (5725160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c3c03706ded85063032a9d8666ebe800cfc8427865f7ce985d65a43403ad9`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e68b06e5892c7aae5c0f861b67c1fc1c5a16655cf23ab80110bdeec81d96a0`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58caa9811c5a3c5eac8958d7fb2b43e5b7f1dbf70ebc23667af645e4246dbbd`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1f0ac058d80c84f4f1d24af7904e537319937583d902b9eb0de2fdda90b2a9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189d1c1f21a2aa342c7214cee2c6ae0f9ca01f5e80c45fb34673fd3f7a2b5df7`

```dockerfile
```

-	Layers:
	-	`sha256:0398d0b4efc9f877bb05a5f1db9ddb082bd71d19f8f44f0b140e41ea356b4572`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 2.3 MB (2283112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096351bc515e41f330c8af901593b4e186a73576011831dd97a67de4e5500535`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:5cce0c8f22191219a6dab87853fae5e3e70996a52ae486fc14329e2514f100f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79527060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bea47c3c5267b89121771f533137d1186e370d46c8779428e5380ffb976f37`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:35:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:37:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:37:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:37:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:44:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:44:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 03:44:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:44:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:44:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:44:51 GMT
USER fluent
# Tue, 07 Apr 2026 03:44:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:44:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65aef497c0f85b6d39008607e5c5e436adafd67d8f206feae2950d981405d5`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 1.3 MB (1261734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd6aa133452fc14cef07cf3b140623bbe92c243c23385fa35d4d320f16755a`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca299d5f81a969b938936930c899ebb4daf7c60e8cf953c60d068e3ed060ff7d`  
		Last Modified: Tue, 07 Apr 2026 02:38:04 GMT  
		Size: 42.1 MB (42078752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1127b79141bdf4702192334328307d206e11c6aa31d052e1a23797b019cd9227`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e77547b311d9fb65f8903175cf04e5cc5c5a83b89a0e2da0019f714e91518f`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 6.0 MB (6045630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e11cc2e00ad994abe260d5ad67dfd7491d4266f259fb05315a980488851c80`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600215398464d6cd5bb29d30abc13a266e4a12d8126c5190ad0350e31d5095e`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308cea664c0c58ae66f713e47f9fcfa93cd6b3d58923b00fbc4b983426bd718`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ea36c0b2d597b14ac8970e16032efdf1a0cb0d0fd61aed56a44962c730fd428a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c056e8f74287d6dacfe03164e50b2b2ab903feb17e1fd90f1803861183181b`

```dockerfile
```

-	Layers:
	-	`sha256:6262f51f5062ebb2bf664a7edd66726710fadb66def54eb761ea06e7f85f0d7b`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 2.3 MB (2281972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f572ef13dddf9baf0bfc02b5007754aac61b224d1192f5b5cce4df8f4867580`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:f71d5e351b72e7080643d00c1cb42debfb7367ccce87e49e4314c8e98f2eb0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458af0a8e9243ed9d51a6ff0601606accae6cb5c314be65370c88c6e2177e213`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:11:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:13:48 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:13:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:13:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:13:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:13:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:13:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:13:49 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 02:58:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 02:58:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 02:58:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 02:58:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 02:58:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 02:58:14 GMT
USER fluent
# Tue, 07 Apr 2026 02:58:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8220afc2b68e6e2441c42d82813901ef61d54f0e858868c36c3612d0f61a341`  
		Last Modified: Tue, 07 Apr 2026 02:13:57 GMT  
		Size: 1.3 MB (1287482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fdd62850e20d9f1696e3113057a3b0eb0bdb0f9a4c9fdb88eb6a48d0f3de3d`  
		Last Modified: Tue, 07 Apr 2026 02:13:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000327029938d76c0a103cbdf0da6867dae4ab25f9bf2cca32934ae5aef4cd6`  
		Last Modified: Tue, 07 Apr 2026 02:14:01 GMT  
		Size: 37.7 MB (37661772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec682f2816027eb0ed1baf871971b8c84a53d2ff5fa00c51528c6060549421c`  
		Last Modified: Tue, 07 Apr 2026 02:13:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777517475398395007d48f1fa04ee2cccbb8e6318ef2a7e1ea4f637f3bbbd50f`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 6.0 MB (6027416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a27cad93f702fee81631e0fb1b3e29127c72e2029e0b2efe88c8cd7bb3a382`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c2494ca7bdadb78327be12121cd7cb1b03db4939073ad1648b796ae4a8b285`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facba3baf4499b30506b0806ae082c0064dbce45068f01ece331d0b48dd0c257`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4a7704dc3805278c40c0a35a8307f6206601a6187a60eeccf92353c2987d13e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dea069ae02f1df9e010055368eb15d47748d2987673ffbcc01bb3140acc5fe`

```dockerfile
```

-	Layers:
	-	`sha256:052c3f5588970e59551554ee94604141d545b1e343406b49645d12a7248ed3f1`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 2.3 MB (2278888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330c4d027f478fbe798e139879f8147c758446000966eaf690cb24db14d17da6`  
		Last Modified: Tue, 07 Apr 2026 02:58:21 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:5ca27c30dabb58c53477d40b8ca406827f6300bd53bb3ade76b6ea09e8a92474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81012672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81aebf04b6260f3428764074def53f2349211f293c045a753766b9a5605afe7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 05:02:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 05:02:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 05:15:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 05:15:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 05:15:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 05:15:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 10:00:54 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 10:00:54 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 10:00:54 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 10:00:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 10:00:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 10:00:56 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 10:00:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 10:00:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 10:00:56 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 10:00:56 GMT
USER fluent
# Tue, 17 Mar 2026 10:00:56 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 10:00:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93820ad1ad41073212dddc80e0d6a6669254071632dab96b9d735edd949550f`  
		Last Modified: Tue, 17 Mar 2026 05:06:45 GMT  
		Size: 1.3 MB (1309779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ff3ee9989c0371a76ab538d2924e74397f4bb3f6ac768e15d4d5f03c96402e`  
		Last Modified: Tue, 17 Mar 2026 05:06:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109974bac0a835d036eb6e55dcad5291a70fcea494a2d03ace97ad3f98e43d44`  
		Last Modified: Tue, 17 Mar 2026 05:15:43 GMT  
		Size: 39.5 MB (39531800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad87bfd03039df023a7d263c23b46c6b986ce6468169d1c514b599f2c28a8f0`  
		Last Modified: Tue, 17 Mar 2026 05:15:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e23befd4447ac944e5e597c45bb016c354ad0d4cfb701b061d89ddfa22e702`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 6.6 MB (6575865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb279357921aae75c4b2280d8e3cf42a3920e93f2626c907357ac4a02a81bf8`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d73d2efba8ba8c2408b0c2bec3cbc19da7bd4a8fef8ae8342a524c24854d0b`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89f6cbf05c25c0aa3b13b42b9a208c0dd3649c68ea9d32941b142a7641e3cd8`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:15d80de4b5aead9c49246bbb15ef30c147c11b5cc5f1bdbb32160d7033cb5694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d4196d0d2e4c48d24d80a1aa76e5d18291d88849a8f61fce0445906000131c`

```dockerfile
```

-	Layers:
	-	`sha256:355d41fa1974e49c50fc3c1cf640e4efa6d2d459c80bb63b3d28a3b34492b917`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 2.3 MB (2285173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5965e9ff86788a8d995c45b05b9d73eb74cc77d985fbe196d3d183fe76c19c71`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; s390x

```console
$ docker pull fluentd@sha256:2f6961489a154b12a8b57595e6032f35ca07e24385b637fcd4646204e88fa6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76770974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0df4efcf86d4de2778e0e97599249ecce1aa9a16d50463561fb529dcde22f97`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:34:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 04:38:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 04:38:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 04:38:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:38:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 06:06:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 06:06:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 06:06:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 06:06:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 06:06:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 06:06:44 GMT
USER fluent
# Tue, 07 Apr 2026 06:06:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 06:06:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f1969e985ea39592094e95f8819f85d22b80808f05e339da5e17920cb7d05`  
		Last Modified: Tue, 07 Apr 2026 04:38:31 GMT  
		Size: 1.3 MB (1294728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b233ac00b24f834a7c3df8aed372379f83062378f27202d9f757b2504747185e`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0e908d5e1ac4b763f917e8f45d21b6b5822ecdcafcbcd10a3e2f156ce1d6e`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 39.2 MB (39206458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3b563c8673d991a48d188be4aaf4b921aced9bcb4638feed907718b6ef5dc4`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f737b275a09b30f87841b28577b17c902c2882c611244171c3e53a878c332`  
		Last Modified: Tue, 07 Apr 2026 06:06:58 GMT  
		Size: 6.4 MB (6431974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e238e6eab8962e5a6c9b89865fa14244ef03dd1c847435148e7de751c02a40b`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b0afeb97c9b9b8939b7ee8fcc6d94cbf03fdb12f18a1f5467abb2b26862920`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d13856a47ace03f81cc0aaa29c3102ab510bd97afcdfc1cdf8eb5bc3ec69e6`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8435c6158f323083ad90c173a3b6cc1b8bc48bc952f34d1da7fc19d095a1d907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597c1ea3ff724140183fd893099f655117d120af93e0711ade84ec749f570141`

```dockerfile
```

-	Layers:
	-	`sha256:822b1fbf5b2de0999dd7426f6c87d0b382f23259963ddaad996a6b2aa7827ed6`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 2.3 MB (2283145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9350a8304d80d98fd56d5d4233b7eddd449129fbf6101b6914e4e1ac328dab37`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:dcbc40508693421a01428cd5112d60c5726c0e79ca9ed870d4e668aeee718ccb
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
$ docker pull fluentd@sha256:2f4043c322f55eec6c6708e4efd629c144448e0a196244c1902a0f1a6c43e721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79240276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d713ba17c405e8e96c3994d35aef5158cf916d53682838c284731869598b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:28:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:31:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:31:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:31:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:33:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:33:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 03:33:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:33:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:33:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:33:51 GMT
USER fluent
# Tue, 07 Apr 2026 03:33:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:33:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78c84e44d70408c199a2896d0fe6d15b64efcceafe0e09550d5177ecdab72b5`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 1.3 MB (1279868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c086a7638e3fda68aac0522c41b07f5f10ac23fed584ee16a13498e0a4947d`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b6e55e1373be9c47416cd4ec47847af123c40d71aaeeb5c34653eb3e287ceb`  
		Last Modified: Tue, 07 Apr 2026 02:31:37 GMT  
		Size: 42.1 MB (42127244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2e954b41c2ddc19fb451b0eacc5ef3bbf6542b210296a77ae759a1277d7d38`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2f4817d01410fa0935c2ac51032921ff607e7de054d59d4cce546f23f28273`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 6.1 MB (6055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287ffb4f171600c7eaad32b94171730f57d10ee2704dc3f2d14f2ad79786dfb5`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ab56bccb331339769e77903e049fb948862d2955c250bc976c836191f85d5d`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e04c8092324d16d133bf8a28c5ecbd2a61e71e004a3732458aa69a376d141b`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bd420eafe75e77c9b004aec3deedb09835a4aa36c85624938eb39fd5e3965b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa3403daf8ff28a64fa6d7bb54ee31b8e3672d3c5ba284d163bad93de84c4bc`

```dockerfile
```

-	Layers:
	-	`sha256:4ea95f6fc3952ecf0f8d41802f1f42d8aeacfe1e3f3954bfb29d13bc89c83b77`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 2.3 MB (2281700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e469a7bf6b1dbca433e02e1e6cfafc8563fc1568ec1f275b79b96f94afa2a287`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:737d41da6bfb0ce9ebc6ada5309f93a3c66b48aa251d12b62c1338633d2b906c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73091229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fddf682d8379469a82e2365369a447e62450bf54b18d429978c6bdea48fce26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:42:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:42:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 03:45:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:45:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:40:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:40:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 04:40:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:40:17 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:40:17 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:40:17 GMT
USER fluent
# Tue, 07 Apr 2026 04:40:17 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:40:17 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f83fcfefaffee8aa367effced408a0e6a87a5e59cdee33c2ca23721e3666bb`  
		Last Modified: Tue, 07 Apr 2026 03:45:13 GMT  
		Size: 1.3 MB (1263659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9350562d97a8b76eee53f9378f84c348e2e8ce41eb494a8f9acfd953ee73661d`  
		Last Modified: Tue, 07 Apr 2026 03:45:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff55ef1d37d6eddef2754669cb01a902319f33e3b5835659ce3c7fbe987cf169`  
		Last Modified: Tue, 07 Apr 2026 03:45:14 GMT  
		Size: 37.9 MB (37924109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db8d12e894040067d04d239a563bb338afdefd7e3ab192ce444708a3e277ac`  
		Last Modified: Tue, 07 Apr 2026 03:45:12 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594bfd195b76e112143930963588f6fc3d3585286f3a7be63979448e52d19bfa`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 6.0 MB (5957259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a637356205a8b660cd31964cf17283ddf1c0f2f1e8d40211a9b693f0fe4f18e`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34cdc5b6faa040070007317eaf98b4c1a3767447b6a72c5856e9fb68ac2cbc1`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc11c1d16b742a1ca4e45e2a3dd99b84782bfb227a6332cab341ed34dfd39ad0`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4ff05bbc8133861b058fbd1d7a8f5afe687d1fa480c668942864f709ec142794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aaed9763b5c76a7ae5965cd090e83cb34052428ced62536562e131a965a9c3`

```dockerfile
```

-	Layers:
	-	`sha256:41c7bea2c8853c86ec41712b331858bf289f07d6f25b7985e8a9bbb031dfb61a`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 2.3 MB (2284671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2589f3eaa3dee5c0c385b127f1f2689c74618d980ec8b9305bba92d694b08048`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:e79ade4311d7653af470029e4dd6340fe8bd1dbc7feb9be95a6aa1ccc787bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70955862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e1393d31b464a3412ae704c38cafaddbb09bbde369bdfc9bf352677d315dc4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:17:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 03:19:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:19:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:19:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:19:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:35:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:35:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 04:35:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:35:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:35:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:35:40 GMT
USER fluent
# Tue, 07 Apr 2026 04:35:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:35:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66e9f844a8fcc6c0af5b1c95ad1e0c477f48277d9bfab72116a2780faf5f9e`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 1.2 MB (1237567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fb85dc50c757ea6577b3fef8fabfe4a5abb87834dc45f032c1f9a56274f658`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dba43d16f47f9f243dd54e854300da3d235512c9a3641611cbfb6a1de8acdbc`  
		Last Modified: Tue, 07 Apr 2026 03:20:07 GMT  
		Size: 37.8 MB (37781086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7219bd5fc4e67916c070402dd93cca9ba0ab97e52a6923882144b109de88b3c`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141b3b04696ed9a81f5a230237c23991f9fecd1a7624de095ed4d3410499d3f9`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 5.7 MB (5725160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c3c03706ded85063032a9d8666ebe800cfc8427865f7ce985d65a43403ad9`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e68b06e5892c7aae5c0f861b67c1fc1c5a16655cf23ab80110bdeec81d96a0`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58caa9811c5a3c5eac8958d7fb2b43e5b7f1dbf70ebc23667af645e4246dbbd`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1f0ac058d80c84f4f1d24af7904e537319937583d902b9eb0de2fdda90b2a9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189d1c1f21a2aa342c7214cee2c6ae0f9ca01f5e80c45fb34673fd3f7a2b5df7`

```dockerfile
```

-	Layers:
	-	`sha256:0398d0b4efc9f877bb05a5f1db9ddb082bd71d19f8f44f0b140e41ea356b4572`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 2.3 MB (2283112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096351bc515e41f330c8af901593b4e186a73576011831dd97a67de4e5500535`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:5cce0c8f22191219a6dab87853fae5e3e70996a52ae486fc14329e2514f100f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79527060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bea47c3c5267b89121771f533137d1186e370d46c8779428e5380ffb976f37`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:35:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:37:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:37:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:37:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:44:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:44:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 03:44:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:44:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:44:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:44:51 GMT
USER fluent
# Tue, 07 Apr 2026 03:44:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:44:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65aef497c0f85b6d39008607e5c5e436adafd67d8f206feae2950d981405d5`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 1.3 MB (1261734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd6aa133452fc14cef07cf3b140623bbe92c243c23385fa35d4d320f16755a`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca299d5f81a969b938936930c899ebb4daf7c60e8cf953c60d068e3ed060ff7d`  
		Last Modified: Tue, 07 Apr 2026 02:38:04 GMT  
		Size: 42.1 MB (42078752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1127b79141bdf4702192334328307d206e11c6aa31d052e1a23797b019cd9227`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e77547b311d9fb65f8903175cf04e5cc5c5a83b89a0e2da0019f714e91518f`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 6.0 MB (6045630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e11cc2e00ad994abe260d5ad67dfd7491d4266f259fb05315a980488851c80`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600215398464d6cd5bb29d30abc13a266e4a12d8126c5190ad0350e31d5095e`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308cea664c0c58ae66f713e47f9fcfa93cd6b3d58923b00fbc4b983426bd718`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:ea36c0b2d597b14ac8970e16032efdf1a0cb0d0fd61aed56a44962c730fd428a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c056e8f74287d6dacfe03164e50b2b2ab903feb17e1fd90f1803861183181b`

```dockerfile
```

-	Layers:
	-	`sha256:6262f51f5062ebb2bf664a7edd66726710fadb66def54eb761ea06e7f85f0d7b`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 2.3 MB (2281972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f572ef13dddf9baf0bfc02b5007754aac61b224d1192f5b5cce4df8f4867580`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:f71d5e351b72e7080643d00c1cb42debfb7367ccce87e49e4314c8e98f2eb0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458af0a8e9243ed9d51a6ff0601606accae6cb5c314be65370c88c6e2177e213`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:11:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:13:48 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:13:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:13:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:13:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:13:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:13:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:13:49 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 02:58:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 02:58:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 02:58:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 02:58:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 02:58:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 02:58:14 GMT
USER fluent
# Tue, 07 Apr 2026 02:58:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8220afc2b68e6e2441c42d82813901ef61d54f0e858868c36c3612d0f61a341`  
		Last Modified: Tue, 07 Apr 2026 02:13:57 GMT  
		Size: 1.3 MB (1287482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fdd62850e20d9f1696e3113057a3b0eb0bdb0f9a4c9fdb88eb6a48d0f3de3d`  
		Last Modified: Tue, 07 Apr 2026 02:13:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000327029938d76c0a103cbdf0da6867dae4ab25f9bf2cca32934ae5aef4cd6`  
		Last Modified: Tue, 07 Apr 2026 02:14:01 GMT  
		Size: 37.7 MB (37661772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec682f2816027eb0ed1baf871971b8c84a53d2ff5fa00c51528c6060549421c`  
		Last Modified: Tue, 07 Apr 2026 02:13:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777517475398395007d48f1fa04ee2cccbb8e6318ef2a7e1ea4f637f3bbbd50f`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 6.0 MB (6027416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a27cad93f702fee81631e0fb1b3e29127c72e2029e0b2efe88c8cd7bb3a382`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c2494ca7bdadb78327be12121cd7cb1b03db4939073ad1648b796ae4a8b285`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facba3baf4499b30506b0806ae082c0064dbce45068f01ece331d0b48dd0c257`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4a7704dc3805278c40c0a35a8307f6206601a6187a60eeccf92353c2987d13e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dea069ae02f1df9e010055368eb15d47748d2987673ffbcc01bb3140acc5fe`

```dockerfile
```

-	Layers:
	-	`sha256:052c3f5588970e59551554ee94604141d545b1e343406b49645d12a7248ed3f1`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 2.3 MB (2278888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330c4d027f478fbe798e139879f8147c758446000966eaf690cb24db14d17da6`  
		Last Modified: Tue, 07 Apr 2026 02:58:21 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:5ca27c30dabb58c53477d40b8ca406827f6300bd53bb3ade76b6ea09e8a92474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81012672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81aebf04b6260f3428764074def53f2349211f293c045a753766b9a5605afe7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 05:02:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 05:02:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 05:15:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 05:15:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 05:15:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 05:15:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 10:00:54 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 10:00:54 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 10:00:54 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 10:00:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 10:00:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 10:00:56 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 10:00:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 10:00:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 10:00:56 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 10:00:56 GMT
USER fluent
# Tue, 17 Mar 2026 10:00:56 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 10:00:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93820ad1ad41073212dddc80e0d6a6669254071632dab96b9d735edd949550f`  
		Last Modified: Tue, 17 Mar 2026 05:06:45 GMT  
		Size: 1.3 MB (1309779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ff3ee9989c0371a76ab538d2924e74397f4bb3f6ac768e15d4d5f03c96402e`  
		Last Modified: Tue, 17 Mar 2026 05:06:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109974bac0a835d036eb6e55dcad5291a70fcea494a2d03ace97ad3f98e43d44`  
		Last Modified: Tue, 17 Mar 2026 05:15:43 GMT  
		Size: 39.5 MB (39531800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad87bfd03039df023a7d263c23b46c6b986ce6468169d1c514b599f2c28a8f0`  
		Last Modified: Tue, 17 Mar 2026 05:15:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e23befd4447ac944e5e597c45bb016c354ad0d4cfb701b061d89ddfa22e702`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 6.6 MB (6575865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb279357921aae75c4b2280d8e3cf42a3920e93f2626c907357ac4a02a81bf8`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d73d2efba8ba8c2408b0c2bec3cbc19da7bd4a8fef8ae8342a524c24854d0b`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89f6cbf05c25c0aa3b13b42b9a208c0dd3649c68ea9d32941b142a7641e3cd8`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:15d80de4b5aead9c49246bbb15ef30c147c11b5cc5f1bdbb32160d7033cb5694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d4196d0d2e4c48d24d80a1aa76e5d18291d88849a8f61fce0445906000131c`

```dockerfile
```

-	Layers:
	-	`sha256:355d41fa1974e49c50fc3c1cf640e4efa6d2d459c80bb63b3d28a3b34492b917`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 2.3 MB (2285173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5965e9ff86788a8d995c45b05b9d73eb74cc77d985fbe196d3d183fe76c19c71`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:2f6961489a154b12a8b57595e6032f35ca07e24385b637fcd4646204e88fa6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76770974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0df4efcf86d4de2778e0e97599249ecce1aa9a16d50463561fb529dcde22f97`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:34:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 04:38:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 04:38:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 04:38:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:38:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 06:06:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 06:06:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 06:06:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 06:06:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 06:06:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 06:06:44 GMT
USER fluent
# Tue, 07 Apr 2026 06:06:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 06:06:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f1969e985ea39592094e95f8819f85d22b80808f05e339da5e17920cb7d05`  
		Last Modified: Tue, 07 Apr 2026 04:38:31 GMT  
		Size: 1.3 MB (1294728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b233ac00b24f834a7c3df8aed372379f83062378f27202d9f757b2504747185e`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0e908d5e1ac4b763f917e8f45d21b6b5822ecdcafcbcd10a3e2f156ce1d6e`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 39.2 MB (39206458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3b563c8673d991a48d188be4aaf4b921aced9bcb4638feed907718b6ef5dc4`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f737b275a09b30f87841b28577b17c902c2882c611244171c3e53a878c332`  
		Last Modified: Tue, 07 Apr 2026 06:06:58 GMT  
		Size: 6.4 MB (6431974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e238e6eab8962e5a6c9b89865fa14244ef03dd1c847435148e7de751c02a40b`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b0afeb97c9b9b8939b7ee8fcc6d94cbf03fdb12f18a1f5467abb2b26862920`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d13856a47ace03f81cc0aaa29c3102ab510bd97afcdfc1cdf8eb5bc3ec69e6`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8435c6158f323083ad90c173a3b6cc1b8bc48bc952f34d1da7fc19d095a1d907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597c1ea3ff724140183fd893099f655117d120af93e0711ade84ec749f570141`

```dockerfile
```

-	Layers:
	-	`sha256:822b1fbf5b2de0999dd7426f6c87d0b382f23259963ddaad996a6b2aa7827ed6`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 2.3 MB (2283145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9350a8304d80d98fd56d5d4233b7eddd449129fbf6101b6914e4e1ac328dab37`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-1.0`

```console
$ docker pull fluentd@sha256:dcbc40508693421a01428cd5112d60c5726c0e79ca9ed870d4e668aeee718ccb
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
$ docker pull fluentd@sha256:2f4043c322f55eec6c6708e4efd629c144448e0a196244c1902a0f1a6c43e721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79240276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d713ba17c405e8e96c3994d35aef5158cf916d53682838c284731869598b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:28:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:31:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:31:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:31:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:33:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:33:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 03:33:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:33:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:33:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:33:51 GMT
USER fluent
# Tue, 07 Apr 2026 03:33:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:33:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78c84e44d70408c199a2896d0fe6d15b64efcceafe0e09550d5177ecdab72b5`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 1.3 MB (1279868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c086a7638e3fda68aac0522c41b07f5f10ac23fed584ee16a13498e0a4947d`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b6e55e1373be9c47416cd4ec47847af123c40d71aaeeb5c34653eb3e287ceb`  
		Last Modified: Tue, 07 Apr 2026 02:31:37 GMT  
		Size: 42.1 MB (42127244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2e954b41c2ddc19fb451b0eacc5ef3bbf6542b210296a77ae759a1277d7d38`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2f4817d01410fa0935c2ac51032921ff607e7de054d59d4cce546f23f28273`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 6.1 MB (6055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287ffb4f171600c7eaad32b94171730f57d10ee2704dc3f2d14f2ad79786dfb5`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ab56bccb331339769e77903e049fb948862d2955c250bc976c836191f85d5d`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e04c8092324d16d133bf8a28c5ecbd2a61e71e004a3732458aa69a376d141b`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bd420eafe75e77c9b004aec3deedb09835a4aa36c85624938eb39fd5e3965b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa3403daf8ff28a64fa6d7bb54ee31b8e3672d3c5ba284d163bad93de84c4bc`

```dockerfile
```

-	Layers:
	-	`sha256:4ea95f6fc3952ecf0f8d41802f1f42d8aeacfe1e3f3954bfb29d13bc89c83b77`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 2.3 MB (2281700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e469a7bf6b1dbca433e02e1e6cfafc8563fc1568ec1f275b79b96f94afa2a287`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:737d41da6bfb0ce9ebc6ada5309f93a3c66b48aa251d12b62c1338633d2b906c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73091229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fddf682d8379469a82e2365369a447e62450bf54b18d429978c6bdea48fce26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:42:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:42:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 03:45:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:45:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:40:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:40:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 04:40:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:40:17 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:40:17 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:40:17 GMT
USER fluent
# Tue, 07 Apr 2026 04:40:17 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:40:17 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f83fcfefaffee8aa367effced408a0e6a87a5e59cdee33c2ca23721e3666bb`  
		Last Modified: Tue, 07 Apr 2026 03:45:13 GMT  
		Size: 1.3 MB (1263659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9350562d97a8b76eee53f9378f84c348e2e8ce41eb494a8f9acfd953ee73661d`  
		Last Modified: Tue, 07 Apr 2026 03:45:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff55ef1d37d6eddef2754669cb01a902319f33e3b5835659ce3c7fbe987cf169`  
		Last Modified: Tue, 07 Apr 2026 03:45:14 GMT  
		Size: 37.9 MB (37924109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db8d12e894040067d04d239a563bb338afdefd7e3ab192ce444708a3e277ac`  
		Last Modified: Tue, 07 Apr 2026 03:45:12 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594bfd195b76e112143930963588f6fc3d3585286f3a7be63979448e52d19bfa`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 6.0 MB (5957259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a637356205a8b660cd31964cf17283ddf1c0f2f1e8d40211a9b693f0fe4f18e`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34cdc5b6faa040070007317eaf98b4c1a3767447b6a72c5856e9fb68ac2cbc1`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc11c1d16b742a1ca4e45e2a3dd99b84782bfb227a6332cab341ed34dfd39ad0`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4ff05bbc8133861b058fbd1d7a8f5afe687d1fa480c668942864f709ec142794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aaed9763b5c76a7ae5965cd090e83cb34052428ced62536562e131a965a9c3`

```dockerfile
```

-	Layers:
	-	`sha256:41c7bea2c8853c86ec41712b331858bf289f07d6f25b7985e8a9bbb031dfb61a`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 2.3 MB (2284671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2589f3eaa3dee5c0c385b127f1f2689c74618d980ec8b9305bba92d694b08048`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:e79ade4311d7653af470029e4dd6340fe8bd1dbc7feb9be95a6aa1ccc787bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70955862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e1393d31b464a3412ae704c38cafaddbb09bbde369bdfc9bf352677d315dc4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:17:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 03:19:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:19:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:19:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:19:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:35:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:35:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 04:35:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:35:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:35:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:35:40 GMT
USER fluent
# Tue, 07 Apr 2026 04:35:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:35:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66e9f844a8fcc6c0af5b1c95ad1e0c477f48277d9bfab72116a2780faf5f9e`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 1.2 MB (1237567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fb85dc50c757ea6577b3fef8fabfe4a5abb87834dc45f032c1f9a56274f658`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dba43d16f47f9f243dd54e854300da3d235512c9a3641611cbfb6a1de8acdbc`  
		Last Modified: Tue, 07 Apr 2026 03:20:07 GMT  
		Size: 37.8 MB (37781086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7219bd5fc4e67916c070402dd93cca9ba0ab97e52a6923882144b109de88b3c`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141b3b04696ed9a81f5a230237c23991f9fecd1a7624de095ed4d3410499d3f9`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 5.7 MB (5725160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c3c03706ded85063032a9d8666ebe800cfc8427865f7ce985d65a43403ad9`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e68b06e5892c7aae5c0f861b67c1fc1c5a16655cf23ab80110bdeec81d96a0`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58caa9811c5a3c5eac8958d7fb2b43e5b7f1dbf70ebc23667af645e4246dbbd`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1f0ac058d80c84f4f1d24af7904e537319937583d902b9eb0de2fdda90b2a9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189d1c1f21a2aa342c7214cee2c6ae0f9ca01f5e80c45fb34673fd3f7a2b5df7`

```dockerfile
```

-	Layers:
	-	`sha256:0398d0b4efc9f877bb05a5f1db9ddb082bd71d19f8f44f0b140e41ea356b4572`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 2.3 MB (2283112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096351bc515e41f330c8af901593b4e186a73576011831dd97a67de4e5500535`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:5cce0c8f22191219a6dab87853fae5e3e70996a52ae486fc14329e2514f100f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79527060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bea47c3c5267b89121771f533137d1186e370d46c8779428e5380ffb976f37`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:35:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:37:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:37:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:37:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:44:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:44:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 03:44:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:44:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:44:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:44:51 GMT
USER fluent
# Tue, 07 Apr 2026 03:44:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:44:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65aef497c0f85b6d39008607e5c5e436adafd67d8f206feae2950d981405d5`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 1.3 MB (1261734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd6aa133452fc14cef07cf3b140623bbe92c243c23385fa35d4d320f16755a`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca299d5f81a969b938936930c899ebb4daf7c60e8cf953c60d068e3ed060ff7d`  
		Last Modified: Tue, 07 Apr 2026 02:38:04 GMT  
		Size: 42.1 MB (42078752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1127b79141bdf4702192334328307d206e11c6aa31d052e1a23797b019cd9227`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e77547b311d9fb65f8903175cf04e5cc5c5a83b89a0e2da0019f714e91518f`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 6.0 MB (6045630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e11cc2e00ad994abe260d5ad67dfd7491d4266f259fb05315a980488851c80`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600215398464d6cd5bb29d30abc13a266e4a12d8126c5190ad0350e31d5095e`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308cea664c0c58ae66f713e47f9fcfa93cd6b3d58923b00fbc4b983426bd718`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ea36c0b2d597b14ac8970e16032efdf1a0cb0d0fd61aed56a44962c730fd428a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c056e8f74287d6dacfe03164e50b2b2ab903feb17e1fd90f1803861183181b`

```dockerfile
```

-	Layers:
	-	`sha256:6262f51f5062ebb2bf664a7edd66726710fadb66def54eb761ea06e7f85f0d7b`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 2.3 MB (2281972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f572ef13dddf9baf0bfc02b5007754aac61b224d1192f5b5cce4df8f4867580`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:f71d5e351b72e7080643d00c1cb42debfb7367ccce87e49e4314c8e98f2eb0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458af0a8e9243ed9d51a6ff0601606accae6cb5c314be65370c88c6e2177e213`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:11:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:13:48 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:13:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:13:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:13:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:13:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:13:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:13:49 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 02:58:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 02:58:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 02:58:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 02:58:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 02:58:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 02:58:14 GMT
USER fluent
# Tue, 07 Apr 2026 02:58:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8220afc2b68e6e2441c42d82813901ef61d54f0e858868c36c3612d0f61a341`  
		Last Modified: Tue, 07 Apr 2026 02:13:57 GMT  
		Size: 1.3 MB (1287482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fdd62850e20d9f1696e3113057a3b0eb0bdb0f9a4c9fdb88eb6a48d0f3de3d`  
		Last Modified: Tue, 07 Apr 2026 02:13:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000327029938d76c0a103cbdf0da6867dae4ab25f9bf2cca32934ae5aef4cd6`  
		Last Modified: Tue, 07 Apr 2026 02:14:01 GMT  
		Size: 37.7 MB (37661772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec682f2816027eb0ed1baf871971b8c84a53d2ff5fa00c51528c6060549421c`  
		Last Modified: Tue, 07 Apr 2026 02:13:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777517475398395007d48f1fa04ee2cccbb8e6318ef2a7e1ea4f637f3bbbd50f`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 6.0 MB (6027416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a27cad93f702fee81631e0fb1b3e29127c72e2029e0b2efe88c8cd7bb3a382`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c2494ca7bdadb78327be12121cd7cb1b03db4939073ad1648b796ae4a8b285`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facba3baf4499b30506b0806ae082c0064dbce45068f01ece331d0b48dd0c257`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4a7704dc3805278c40c0a35a8307f6206601a6187a60eeccf92353c2987d13e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dea069ae02f1df9e010055368eb15d47748d2987673ffbcc01bb3140acc5fe`

```dockerfile
```

-	Layers:
	-	`sha256:052c3f5588970e59551554ee94604141d545b1e343406b49645d12a7248ed3f1`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 2.3 MB (2278888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330c4d027f478fbe798e139879f8147c758446000966eaf690cb24db14d17da6`  
		Last Modified: Tue, 07 Apr 2026 02:58:21 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:5ca27c30dabb58c53477d40b8ca406827f6300bd53bb3ade76b6ea09e8a92474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81012672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81aebf04b6260f3428764074def53f2349211f293c045a753766b9a5605afe7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 05:02:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 05:02:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 05:15:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 05:15:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 05:15:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 05:15:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 10:00:54 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 10:00:54 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 10:00:54 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 10:00:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 10:00:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 10:00:56 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 10:00:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 10:00:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 10:00:56 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 10:00:56 GMT
USER fluent
# Tue, 17 Mar 2026 10:00:56 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 10:00:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93820ad1ad41073212dddc80e0d6a6669254071632dab96b9d735edd949550f`  
		Last Modified: Tue, 17 Mar 2026 05:06:45 GMT  
		Size: 1.3 MB (1309779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ff3ee9989c0371a76ab538d2924e74397f4bb3f6ac768e15d4d5f03c96402e`  
		Last Modified: Tue, 17 Mar 2026 05:06:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109974bac0a835d036eb6e55dcad5291a70fcea494a2d03ace97ad3f98e43d44`  
		Last Modified: Tue, 17 Mar 2026 05:15:43 GMT  
		Size: 39.5 MB (39531800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad87bfd03039df023a7d263c23b46c6b986ce6468169d1c514b599f2c28a8f0`  
		Last Modified: Tue, 17 Mar 2026 05:15:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e23befd4447ac944e5e597c45bb016c354ad0d4cfb701b061d89ddfa22e702`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 6.6 MB (6575865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb279357921aae75c4b2280d8e3cf42a3920e93f2626c907357ac4a02a81bf8`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d73d2efba8ba8c2408b0c2bec3cbc19da7bd4a8fef8ae8342a524c24854d0b`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89f6cbf05c25c0aa3b13b42b9a208c0dd3649c68ea9d32941b142a7641e3cd8`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:15d80de4b5aead9c49246bbb15ef30c147c11b5cc5f1bdbb32160d7033cb5694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d4196d0d2e4c48d24d80a1aa76e5d18291d88849a8f61fce0445906000131c`

```dockerfile
```

-	Layers:
	-	`sha256:355d41fa1974e49c50fc3c1cf640e4efa6d2d459c80bb63b3d28a3b34492b917`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 2.3 MB (2285173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5965e9ff86788a8d995c45b05b9d73eb74cc77d985fbe196d3d183fe76c19c71`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:2f6961489a154b12a8b57595e6032f35ca07e24385b637fcd4646204e88fa6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76770974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0df4efcf86d4de2778e0e97599249ecce1aa9a16d50463561fb529dcde22f97`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:34:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 04:38:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 04:38:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 04:38:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:38:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 06:06:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 06:06:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 06:06:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 06:06:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 06:06:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 06:06:44 GMT
USER fluent
# Tue, 07 Apr 2026 06:06:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 06:06:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f1969e985ea39592094e95f8819f85d22b80808f05e339da5e17920cb7d05`  
		Last Modified: Tue, 07 Apr 2026 04:38:31 GMT  
		Size: 1.3 MB (1294728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b233ac00b24f834a7c3df8aed372379f83062378f27202d9f757b2504747185e`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0e908d5e1ac4b763f917e8f45d21b6b5822ecdcafcbcd10a3e2f156ce1d6e`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 39.2 MB (39206458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3b563c8673d991a48d188be4aaf4b921aced9bcb4638feed907718b6ef5dc4`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f737b275a09b30f87841b28577b17c902c2882c611244171c3e53a878c332`  
		Last Modified: Tue, 07 Apr 2026 06:06:58 GMT  
		Size: 6.4 MB (6431974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e238e6eab8962e5a6c9b89865fa14244ef03dd1c847435148e7de751c02a40b`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b0afeb97c9b9b8939b7ee8fcc6d94cbf03fdb12f18a1f5467abb2b26862920`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d13856a47ace03f81cc0aaa29c3102ab510bd97afcdfc1cdf8eb5bc3ec69e6`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8435c6158f323083ad90c173a3b6cc1b8bc48bc952f34d1da7fc19d095a1d907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597c1ea3ff724140183fd893099f655117d120af93e0711ade84ec749f570141`

```dockerfile
```

-	Layers:
	-	`sha256:822b1fbf5b2de0999dd7426f6c87d0b382f23259963ddaad996a6b2aa7827ed6`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 2.3 MB (2283145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9350a8304d80d98fd56d5d4233b7eddd449129fbf6101b6914e4e1ac328dab37`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-debian-1.0`

```console
$ docker pull fluentd@sha256:dcbc40508693421a01428cd5112d60c5726c0e79ca9ed870d4e668aeee718ccb
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
$ docker pull fluentd@sha256:2f4043c322f55eec6c6708e4efd629c144448e0a196244c1902a0f1a6c43e721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79240276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3d713ba17c405e8e96c3994d35aef5158cf916d53682838c284731869598b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:28:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:28:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:31:27 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:31:27 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:31:27 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:31:27 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:31:27 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:33:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:33:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 03:33:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:33:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:33:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:33:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:33:51 GMT
USER fluent
# Tue, 07 Apr 2026 03:33:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:33:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78c84e44d70408c199a2896d0fe6d15b64efcceafe0e09550d5177ecdab72b5`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 1.3 MB (1279868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c086a7638e3fda68aac0522c41b07f5f10ac23fed584ee16a13498e0a4947d`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b6e55e1373be9c47416cd4ec47847af123c40d71aaeeb5c34653eb3e287ceb`  
		Last Modified: Tue, 07 Apr 2026 02:31:37 GMT  
		Size: 42.1 MB (42127244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2e954b41c2ddc19fb451b0eacc5ef3bbf6542b210296a77ae759a1277d7d38`  
		Last Modified: Tue, 07 Apr 2026 02:31:36 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2f4817d01410fa0935c2ac51032921ff607e7de054d59d4cce546f23f28273`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 6.1 MB (6055126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287ffb4f171600c7eaad32b94171730f57d10ee2704dc3f2d14f2ad79786dfb5`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ab56bccb331339769e77903e049fb948862d2955c250bc976c836191f85d5d`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e04c8092324d16d133bf8a28c5ecbd2a61e71e004a3732458aa69a376d141b`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bd420eafe75e77c9b004aec3deedb09835a4aa36c85624938eb39fd5e3965b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa3403daf8ff28a64fa6d7bb54ee31b8e3672d3c5ba284d163bad93de84c4bc`

```dockerfile
```

-	Layers:
	-	`sha256:4ea95f6fc3952ecf0f8d41802f1f42d8aeacfe1e3f3954bfb29d13bc89c83b77`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 2.3 MB (2281700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e469a7bf6b1dbca433e02e1e6cfafc8563fc1568ec1f275b79b96f94afa2a287`  
		Last Modified: Tue, 07 Apr 2026 03:34:00 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:737d41da6bfb0ce9ebc6ada5309f93a3c66b48aa251d12b62c1338633d2b906c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73091229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fddf682d8379469a82e2365369a447e62450bf54b18d429978c6bdea48fce26`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:42:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:42:01 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 03:45:04 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 03:45:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:04 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:45:04 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:45:04 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:45:04 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:40:17 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:40:17 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 04:40:17 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:40:17 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:40:17 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:40:17 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:40:17 GMT
USER fluent
# Tue, 07 Apr 2026 04:40:17 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:40:17 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a32056c13d69abfd2a107f36cfc2049bdb6b52dbb76427fb9c1f688273f6bce`  
		Last Modified: Tue, 07 Apr 2026 00:11:10 GMT  
		Size: 27.9 MB (27943808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f83fcfefaffee8aa367effced408a0e6a87a5e59cdee33c2ca23721e3666bb`  
		Last Modified: Tue, 07 Apr 2026 03:45:13 GMT  
		Size: 1.3 MB (1263659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9350562d97a8b76eee53f9378f84c348e2e8ce41eb494a8f9acfd953ee73661d`  
		Last Modified: Tue, 07 Apr 2026 03:45:12 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff55ef1d37d6eddef2754669cb01a902319f33e3b5835659ce3c7fbe987cf169`  
		Last Modified: Tue, 07 Apr 2026 03:45:14 GMT  
		Size: 37.9 MB (37924109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7db8d12e894040067d04d239a563bb338afdefd7e3ab192ce444708a3e277ac`  
		Last Modified: Tue, 07 Apr 2026 03:45:12 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594bfd195b76e112143930963588f6fc3d3585286f3a7be63979448e52d19bfa`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 6.0 MB (5957259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a637356205a8b660cd31964cf17283ddf1c0f2f1e8d40211a9b693f0fe4f18e`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34cdc5b6faa040070007317eaf98b4c1a3767447b6a72c5856e9fb68ac2cbc1`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc11c1d16b742a1ca4e45e2a3dd99b84782bfb227a6332cab341ed34dfd39ad0`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4ff05bbc8133861b058fbd1d7a8f5afe687d1fa480c668942864f709ec142794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aaed9763b5c76a7ae5965cd090e83cb34052428ced62536562e131a965a9c3`

```dockerfile
```

-	Layers:
	-	`sha256:41c7bea2c8853c86ec41712b331858bf289f07d6f25b7985e8a9bbb031dfb61a`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 2.3 MB (2284671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2589f3eaa3dee5c0c385b127f1f2689c74618d980ec8b9305bba92d694b08048`  
		Last Modified: Tue, 07 Apr 2026 04:40:25 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:e79ade4311d7653af470029e4dd6340fe8bd1dbc7feb9be95a6aa1ccc787bf3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70955862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e1393d31b464a3412ae704c38cafaddbb09bbde369bdfc9bf352677d315dc4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:17:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:17:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 03:19:57 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 03:19:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 03:19:57 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 03:19:57 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:19:57 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 03:19:57 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 04:35:40 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 04:35:40 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 04:35:40 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 04:35:40 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 04:35:40 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 04:35:40 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 04:35:40 GMT
USER fluent
# Tue, 07 Apr 2026 04:35:40 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 04:35:40 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4c6d27739d1db2f26843c4e427219b60cd29d0d75a2f4c9eae2e732971275433`  
		Last Modified: Tue, 07 Apr 2026 01:00:39 GMT  
		Size: 26.2 MB (26209653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e66e9f844a8fcc6c0af5b1c95ad1e0c477f48277d9bfab72116a2780faf5f9e`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 1.2 MB (1237567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fb85dc50c757ea6577b3fef8fabfe4a5abb87834dc45f032c1f9a56274f658`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dba43d16f47f9f243dd54e854300da3d235512c9a3641611cbfb6a1de8acdbc`  
		Last Modified: Tue, 07 Apr 2026 03:20:07 GMT  
		Size: 37.8 MB (37781086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7219bd5fc4e67916c070402dd93cca9ba0ab97e52a6923882144b109de88b3c`  
		Last Modified: Tue, 07 Apr 2026 03:20:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141b3b04696ed9a81f5a230237c23991f9fecd1a7624de095ed4d3410499d3f9`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 5.7 MB (5725160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c3c03706ded85063032a9d8666ebe800cfc8427865f7ce985d65a43403ad9`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e68b06e5892c7aae5c0f861b67c1fc1c5a16655cf23ab80110bdeec81d96a0`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58caa9811c5a3c5eac8958d7fb2b43e5b7f1dbf70ebc23667af645e4246dbbd`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1f0ac058d80c84f4f1d24af7904e537319937583d902b9eb0de2fdda90b2a9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189d1c1f21a2aa342c7214cee2c6ae0f9ca01f5e80c45fb34673fd3f7a2b5df7`

```dockerfile
```

-	Layers:
	-	`sha256:0398d0b4efc9f877bb05a5f1db9ddb082bd71d19f8f44f0b140e41ea356b4572`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 2.3 MB (2283112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096351bc515e41f330c8af901593b4e186a73576011831dd97a67de4e5500535`  
		Last Modified: Tue, 07 Apr 2026 04:35:50 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:5cce0c8f22191219a6dab87853fae5e3e70996a52ae486fc14329e2514f100f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79527060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bea47c3c5267b89121771f533137d1186e370d46c8779428e5380ffb976f37`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:35:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:35:11 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:37:53 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:37:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:37:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:37:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:37:53 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:37:53 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 03:44:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 03:44:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 03:44:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 03:44:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 03:44:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 03:44:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 03:44:51 GMT
USER fluent
# Tue, 07 Apr 2026 03:44:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 03:44:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65aef497c0f85b6d39008607e5c5e436adafd67d8f206feae2950d981405d5`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 1.3 MB (1261734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9fd6aa133452fc14cef07cf3b140623bbe92c243c23385fa35d4d320f16755a`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca299d5f81a969b938936930c899ebb4daf7c60e8cf953c60d068e3ed060ff7d`  
		Last Modified: Tue, 07 Apr 2026 02:38:04 GMT  
		Size: 42.1 MB (42078752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1127b79141bdf4702192334328307d206e11c6aa31d052e1a23797b019cd9227`  
		Last Modified: Tue, 07 Apr 2026 02:38:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e77547b311d9fb65f8903175cf04e5cc5c5a83b89a0e2da0019f714e91518f`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 6.0 MB (6045630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88e11cc2e00ad994abe260d5ad67dfd7491d4266f259fb05315a980488851c80`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e600215398464d6cd5bb29d30abc13a266e4a12d8126c5190ad0350e31d5095e`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9308cea664c0c58ae66f713e47f9fcfa93cd6b3d58923b00fbc4b983426bd718`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:ea36c0b2d597b14ac8970e16032efdf1a0cb0d0fd61aed56a44962c730fd428a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c056e8f74287d6dacfe03164e50b2b2ab903feb17e1fd90f1803861183181b`

```dockerfile
```

-	Layers:
	-	`sha256:6262f51f5062ebb2bf664a7edd66726710fadb66def54eb761ea06e7f85f0d7b`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 2.3 MB (2281972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f572ef13dddf9baf0bfc02b5007754aac61b224d1192f5b5cce4df8f4867580`  
		Last Modified: Tue, 07 Apr 2026 03:45:00 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:f71d5e351b72e7080643d00c1cb42debfb7367ccce87e49e4314c8e98f2eb0cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76270319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458af0a8e9243ed9d51a6ff0601606accae6cb5c314be65370c88c6e2177e213`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:11:18 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 02:13:48 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 02:13:48 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 02:13:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 02:13:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 02:13:48 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 02:13:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:13:49 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 02:13:49 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 02:58:14 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 02:58:14 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 02:58:14 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 02:58:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 02:58:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 02:58:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 02:58:14 GMT
USER fluent
# Tue, 07 Apr 2026 02:58:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 02:58:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8220afc2b68e6e2441c42d82813901ef61d54f0e858868c36c3612d0f61a341`  
		Last Modified: Tue, 07 Apr 2026 02:13:57 GMT  
		Size: 1.3 MB (1287482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fdd62850e20d9f1696e3113057a3b0eb0bdb0f9a4c9fdb88eb6a48d0f3de3d`  
		Last Modified: Tue, 07 Apr 2026 02:13:56 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8000327029938d76c0a103cbdf0da6867dae4ab25f9bf2cca32934ae5aef4cd6`  
		Last Modified: Tue, 07 Apr 2026 02:14:01 GMT  
		Size: 37.7 MB (37661772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec682f2816027eb0ed1baf871971b8c84a53d2ff5fa00c51528c6060549421c`  
		Last Modified: Tue, 07 Apr 2026 02:13:57 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777517475398395007d48f1fa04ee2cccbb8e6318ef2a7e1ea4f637f3bbbd50f`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 6.0 MB (6027416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a27cad93f702fee81631e0fb1b3e29127c72e2029e0b2efe88c8cd7bb3a382`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c2494ca7bdadb78327be12121cd7cb1b03db4939073ad1648b796ae4a8b285`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facba3baf4499b30506b0806ae082c0064dbce45068f01ece331d0b48dd0c257`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4a7704dc3805278c40c0a35a8307f6206601a6187a60eeccf92353c2987d13e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28dea069ae02f1df9e010055368eb15d47748d2987673ffbcc01bb3140acc5fe`

```dockerfile
```

-	Layers:
	-	`sha256:052c3f5588970e59551554ee94604141d545b1e343406b49645d12a7248ed3f1`  
		Last Modified: Tue, 07 Apr 2026 02:58:22 GMT  
		Size: 2.3 MB (2278888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330c4d027f478fbe798e139879f8147c758446000966eaf690cb24db14d17da6`  
		Last Modified: Tue, 07 Apr 2026 02:58:21 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:5ca27c30dabb58c53477d40b8ca406827f6300bd53bb3ade76b6ea09e8a92474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81012672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81aebf04b6260f3428764074def53f2349211f293c045a753766b9a5605afe7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 05:02:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 05:02:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 17 Mar 2026 05:15:24 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 17 Mar 2026 05:15:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 17 Mar 2026 05:15:24 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 17 Mar 2026 05:15:24 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 05:15:24 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 17 Mar 2026 05:15:24 GMT
CMD ["irb"]
# Tue, 17 Mar 2026 10:00:54 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 17 Mar 2026 10:00:54 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 17 Mar 2026 10:00:54 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 17 Mar 2026 10:00:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 17 Mar 2026 10:00:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 17 Mar 2026 10:00:56 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 17 Mar 2026 10:00:56 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 17 Mar 2026 10:00:56 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 17 Mar 2026 10:00:56 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 17 Mar 2026 10:00:56 GMT
USER fluent
# Tue, 17 Mar 2026 10:00:56 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 17 Mar 2026 10:00:56 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93820ad1ad41073212dddc80e0d6a6669254071632dab96b9d735edd949550f`  
		Last Modified: Tue, 17 Mar 2026 05:06:45 GMT  
		Size: 1.3 MB (1309779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ff3ee9989c0371a76ab538d2924e74397f4bb3f6ac768e15d4d5f03c96402e`  
		Last Modified: Tue, 17 Mar 2026 05:06:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109974bac0a835d036eb6e55dcad5291a70fcea494a2d03ace97ad3f98e43d44`  
		Last Modified: Tue, 17 Mar 2026 05:15:43 GMT  
		Size: 39.5 MB (39531800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad87bfd03039df023a7d263c23b46c6b986ce6468169d1c514b599f2c28a8f0`  
		Last Modified: Tue, 17 Mar 2026 05:15:42 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e23befd4447ac944e5e597c45bb016c354ad0d4cfb701b061d89ddfa22e702`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 6.6 MB (6575865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb279357921aae75c4b2280d8e3cf42a3920e93f2626c907357ac4a02a81bf8`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d73d2efba8ba8c2408b0c2bec3cbc19da7bd4a8fef8ae8342a524c24854d0b`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89f6cbf05c25c0aa3b13b42b9a208c0dd3649c68ea9d32941b142a7641e3cd8`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:15d80de4b5aead9c49246bbb15ef30c147c11b5cc5f1bdbb32160d7033cb5694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d4196d0d2e4c48d24d80a1aa76e5d18291d88849a8f61fce0445906000131c`

```dockerfile
```

-	Layers:
	-	`sha256:355d41fa1974e49c50fc3c1cf640e4efa6d2d459c80bb63b3d28a3b34492b917`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 2.3 MB (2285173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5965e9ff86788a8d995c45b05b9d73eb74cc77d985fbe196d3d183fe76c19c71`  
		Last Modified: Tue, 17 Mar 2026 10:01:22 GMT  
		Size: 21.4 KB (21376 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:2f6961489a154b12a8b57595e6032f35ca07e24385b637fcd4646204e88fa6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76770974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0df4efcf86d4de2778e0e97599249ecce1aa9a16d50463561fb529dcde22f97`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 04:34:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:34:56 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 07 Apr 2026 04:38:16 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 07 Apr 2026 04:38:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 07 Apr 2026 04:38:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 07 Apr 2026 04:38:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 04:38:16 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 07 Apr 2026 04:38:16 GMT
CMD ["irb"]
# Tue, 07 Apr 2026 06:06:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Tue, 07 Apr 2026 06:06:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Tue, 07 Apr 2026 06:06:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
COPY entrypoint.sh /bin/ # buildkit
# Tue, 07 Apr 2026 06:06:44 GMT
ENV FLUENTD_CONF=fluent.conf
# Tue, 07 Apr 2026 06:06:44 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Tue, 07 Apr 2026 06:06:44 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Tue, 07 Apr 2026 06:06:44 GMT
USER fluent
# Tue, 07 Apr 2026 06:06:44 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Tue, 07 Apr 2026 06:06:44 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f1969e985ea39592094e95f8819f85d22b80808f05e339da5e17920cb7d05`  
		Last Modified: Tue, 07 Apr 2026 04:38:31 GMT  
		Size: 1.3 MB (1294728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b233ac00b24f834a7c3df8aed372379f83062378f27202d9f757b2504747185e`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a0e908d5e1ac4b763f917e8f45d21b6b5822ecdcafcbcd10a3e2f156ce1d6e`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 39.2 MB (39206458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3b563c8673d991a48d188be4aaf4b921aced9bcb4638feed907718b6ef5dc4`  
		Last Modified: Tue, 07 Apr 2026 04:38:32 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7f737b275a09b30f87841b28577b17c902c2882c611244171c3e53a878c332`  
		Last Modified: Tue, 07 Apr 2026 06:06:58 GMT  
		Size: 6.4 MB (6431974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e238e6eab8962e5a6c9b89865fa14244ef03dd1c847435148e7de751c02a40b`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b0afeb97c9b9b8939b7ee8fcc6d94cbf03fdb12f18a1f5467abb2b26862920`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d13856a47ace03f81cc0aaa29c3102ab510bd97afcdfc1cdf8eb5bc3ec69e6`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8435c6158f323083ad90c173a3b6cc1b8bc48bc952f34d1da7fc19d095a1d907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597c1ea3ff724140183fd893099f655117d120af93e0711ade84ec749f570141`

```dockerfile
```

-	Layers:
	-	`sha256:822b1fbf5b2de0999dd7426f6c87d0b382f23259963ddaad996a6b2aa7827ed6`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 2.3 MB (2283145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9350a8304d80d98fd56d5d4233b7eddd449129fbf6101b6914e4e1ac328dab37`  
		Last Modified: Tue, 07 Apr 2026 06:06:56 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
