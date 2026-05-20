<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.19-1`](#fluentdv119-1)
-	[`fluentd:v1.19-debian-1`](#fluentdv119-debian-1)
-	[`fluentd:v1.19.2-1.0`](#fluentdv1192-10)
-	[`fluentd:v1.19.2-debian-1.0`](#fluentdv1192-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:a8afee19237b7c269e0ad943f4d7b66cf290d1aecf856fe7f6f480d5ad577b87
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
$ docker pull fluentd@sha256:00f76d25091b25cf42af10b5b8b0e184ef46c37da9654754581f727063be9856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79255022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62910f165807c3441ceadffa6ecaaa96fd0df004c645b721b1bcde139249569`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:51:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:34 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 19 May 2026 23:53:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:34 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:34 GMT
CMD ["irb"]
# Wed, 20 May 2026 00:42:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 00:42:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 00:42:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 00:42:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 00:42:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 00:42:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 00:42:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 00:42:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 00:42:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 00:42:42 GMT
USER fluent
# Wed, 20 May 2026 00:42:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 00:42:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae509a998d8cc25f86fa4f526ccfd3705bd9f1cdca6b1b3e5dde600c5503c8f8`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 1.3 MB (1279968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74962092651f83b43187b825e403ac93d24a5181f9ce1560f2048cb675a93a3`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3262473bfa79eafa8c9058c39e428100724eeb68ce81266365aa60667dffafe`  
		Last Modified: Tue, 19 May 2026 23:53:43 GMT  
		Size: 42.1 MB (42127140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba9eca8660ca68e09841c5da2d4e95a207217797f889c661969cd56adadb63d`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a9eb26a7e329dced11d3949926d121f7c796c796b1fc11f7b12985503d850`  
		Last Modified: Wed, 20 May 2026 00:42:53 GMT  
		Size: 6.1 MB (6065591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ae1d65594255316e8b520c558272744cf5de02d0e70e88fd27cca5472022c9`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff9be9611b0755a0d7c799c2b31f819f7441dd1bd513d3ed78f20070a5e8c04`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d30ebd71cff00e52701b7628b7438f5eb05107462f3c16c488ae63115c29ce6`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:5c9e8fddecf115ca8ef240cc97838dac301ebad813f0f4bb97fb4a2df8663223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd3d78ccc58da38f5c9784225881c8f8e808b08b3a013d1bcc82291d46b4027`

```dockerfile
```

-	Layers:
	-	`sha256:69756b18478f4cc81288a43dc2b274637ab0808892f69299c7a46ce2bc4f376b`  
		Last Modified: Wed, 20 May 2026 00:42:53 GMT  
		Size: 2.3 MB (2281822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4464ac2f2e453244abc0de5ed98d4a248c543e78699b999dd1652d669fdedf78`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3deeebb820fbfa4c392f5bf9a0698e6fe21c35187f8fd6543d4b665b3660a1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73112123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a45a7c8d6b7dab645bfc30843eb6f32797714e337f1844a353ab4b47e23bd4c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:36:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:36:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:39:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 00:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:39:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:39:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:39:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:39:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:39:20 GMT
CMD ["irb"]
# Wed, 20 May 2026 01:54:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 01:54:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 01:54:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 01:54:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 01:54:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 01:54:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 01:54:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 01:54:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 01:54:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 01:54:14 GMT
USER fluent
# Wed, 20 May 2026 01:54:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 01:54:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96895aa837a127026eac95d26c75abbb54babbb5e762050dadd64de4a4cdf26b`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 1.3 MB (1263760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab57a91c1b877ddd64d9568132be395821962d3f9abd509d21b78fbb37d4ce59`  
		Last Modified: Wed, 20 May 2026 00:39:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7c7a49c9a601347b5bc7885069679efc572a7d07d471b0d729f46f3f26606`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 37.9 MB (37924207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae01ed4844d48ccad3e6e0c04da1c92633f098629f45d62660416eba51d518d`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435e0feeac4798a35e86ed15b1039dcbd7564a9d1463c1d272f71afdf4b5a6c7`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 6.0 MB (5967895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a88cbf410a462245cdf6c313f99016571ca1333a989f427d18cc0d8af13d1d`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a511f40be0082bccf64ada0f042b0817dce09d595da6ea8ffac8ba4a47af61`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b4d5734bead9accdc01648bf81a931cdab381f24a53c405d69d26d7740f4e4`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:4fbbf16de9fd37b8ad02ffc8ff711f6fb23db4db59ca30ef6b7a479d63be9911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac22b6680d7de4ef960a8ba1f903176de9f4d275f4307e36b4508e8e2c78785`

```dockerfile
```

-	Layers:
	-	`sha256:ffc4528a925dfb651506aa4af4d84b57e259458e081ff07bc63d3fac108efda9`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 2.3 MB (2284793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69f5031a63ffa26d07f230fc90c0cd130909dd2454f15aad4f5becee518760d4`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:17b4125ec36408635ec7cfa349a5ed826017e2bf7e5c44206a2a69682ba3f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70960827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eba3e25015f42e83adbf7a505edf08f56ea185dd7d2275e1d653fc44da17273`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:12:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:15:11 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 01:15:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:15:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:15:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:15:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:15:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:15:11 GMT
CMD ["irb"]
# Wed, 20 May 2026 02:18:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 02:18:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 02:18:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 02:18:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 02:18:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 02:18:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 02:18:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 02:18:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 02:18:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 02:18:51 GMT
USER fluent
# Wed, 20 May 2026 02:18:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 02:18:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0e18f2eb3a8e56bd5a9ae9ab99db08dcf4799a8c083e10a4634e7b53fd7f2`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 1.2 MB (1237685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99435c1ef4eea2241c80a26de27a40623cbd18ae90074a36770ba95dd49ee2e`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4f726d4647f840eb32e17ab3eac6cd69521f1b0ea37a25100585f11ab43f2c`  
		Last Modified: Wed, 20 May 2026 01:15:20 GMT  
		Size: 37.8 MB (37781022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418179391d555c02f2342c5b411ca11f3df309ba00f80724924c50cd1369500`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015697a1eccf89e0b031fe60053f9a706b1a2b8b2f06ae62e7ce9959fbfd1e8f`  
		Last Modified: Wed, 20 May 2026 02:19:00 GMT  
		Size: 5.7 MB (5733897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bc52d940d104b1c67a9254a4647201fc4de5287bc08f7f67a7fedc3d96d161`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641b991a2723adf71945a9dca05376e4908849b4846c28b4b082949bdee94ce0`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd085d4f1bd88ed9d7df2521f8dc417ec111dd4d70c32a5cd07f33a0aa13ad1a`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:b3aa02b23374c872acce7d6637246def14b74cfa03be1e25e51ab9603936b181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc08142d2f496ae5d62f9e06db6eacac4419377aecaae6e62ba38141a6ab582`

```dockerfile
```

-	Layers:
	-	`sha256:ccd7c8b017d42e010b1e7b8b4e8efb4664779c34f51ec4d43129fc5b42c63e19`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 2.3 MB (2283234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a949fdba9ae187c7a9ff9ac9d419614042df451a2343917d40cc425ffefb7692`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:ce3631f5ca630ab6347a9df8f96824c814e7f49fb24e536cbfa5c302face8cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79544961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c70ed8618efb22b7953c7f3b73edc4e61129698e809006b4a660a229e1e7b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:59:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:01:38 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 00:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:01:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:01:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:01:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:01:38 GMT
CMD ["irb"]
# Wed, 20 May 2026 00:45:26 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 00:45:26 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 00:45:26 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 00:45:26 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 00:45:26 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 00:45:26 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 00:45:26 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 00:45:26 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 00:45:26 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 00:45:26 GMT
USER fluent
# Wed, 20 May 2026 00:45:26 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 00:45:26 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0598190532e5fd5fa7f406a5f319138ca25758feb0a64da1b3449f88ee3521`  
		Last Modified: Wed, 20 May 2026 00:01:47 GMT  
		Size: 1.3 MB (1262002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15451c3fcbf117446c70cfdc658a97fef17103b8aac67f9d0f6802d157bd9b46`  
		Last Modified: Wed, 20 May 2026 00:01:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f64a0da9b1063193969c2698804e6a46b382e111eaf1458b40462d9cfe9d2f6`  
		Last Modified: Wed, 20 May 2026 00:01:48 GMT  
		Size: 42.1 MB (42078709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b2a3b4652676c008170445be657c4eb9ad8e3438b155e354ce5530a206af77`  
		Last Modified: Wed, 20 May 2026 00:01:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c468e08f650d3fff69045c6c8375b0a6c8a16d598528d7615fd37b3b57ec048`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 6.1 MB (6059940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e6ef0caacaf679fbbbd825fa41b30bd764a7d8245761de4517c992ae005bb`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04afc7675db41ded07504e36e5275da1bbcafcb0c24b8ae92c8cecaa8e7dd842`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc75834da573e2d5e8b320011cc488ea14c4991de83d8301f3d53e1c75c7b358`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:1ab31f62a213d35770ef2044e29445ac0521d04ed3dd854d1f1378ddf3109e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d3b20a204acc80741a498fb9d4108366013dac8043dd87c9ccbcf9f5f2692`

```dockerfile
```

-	Layers:
	-	`sha256:5c7f3e39d6f5e68a0e9b8bf80c02dab50eac63bf0943af51de24ea1d34099e4a`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 2.3 MB (2282086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0f0cc04971ca7d3fa62832f8578b0f4e5c0d3098839dda7bf0c54caa537224`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:c410b212e6cdfc4092aacc1cce7dc5e1bbb7019fd56b8bc46cef136714c77934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76286643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66240acb7cefc429d068f7e294fbcc57cc4e40359a5c6e7e230bfaabd864ff76`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:50:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 19 May 2026 23:53:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:20 GMT
CMD ["irb"]
# Wed, 20 May 2026 03:02:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 03:02:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 03:02:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 03:02:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 03:02:10 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 03:02:10 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 03:02:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 03:02:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 03:02:10 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 03:02:10 GMT
USER fluent
# Wed, 20 May 2026 03:02:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 03:02:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af0b86f8e074f8013394c8982e198a1696c4342a8a353df1261a9436c962fc9`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 1.3 MB (1287842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b478f5fd5d558d3bc5b16b7358ad81ffe9e90dd8bc53036a1e39466601cef7`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04ada0bbc123da7765a41ed03bd4930b19f6d3d5b7e7a44c1387ac2fcadd1d6`  
		Last Modified: Tue, 19 May 2026 23:53:29 GMT  
		Size: 37.7 MB (37661953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55408ceb22509be948980234f637e5a5ae7adf6e80d24588739f6d90684f6216`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931a4801406d68f7b0827fd601ff8d85c52ab40f6ec0eb8c93e5a2f68fd850d0`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 6.0 MB (6039122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e24965accd62ef1ba63bcda357831f008d5a4a8e3617dddb25eaa65a024729`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2599cc634f1448c59392feca518e7674b2ddb84e80dd929c0d148c72e379ca16`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5002f177266084489472144ecab94c108374732a7e59372ba5a8b2b7246c1d59`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:cb0ae3f7faf6ea5bde3c605d94ebacdca656cc30d5a2ea84e185038d80ce97e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2322a8ffe133a3f97e021d2664428ee0363fbdd607c2d35fc5fe47861d5146d0`

```dockerfile
```

-	Layers:
	-	`sha256:4151cea6497c446e934bc121c3af58b3da29964f63ecd3edbb446fa9278fcadd`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 2.3 MB (2279010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4745c54e86bea1ab62463a9b51c5d5fb518733e07ae2e73070c9f3947738854d`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:2bd708cb0638677b5220c6d97aa100b65010de3ca9c61de375812de9b67f1408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81035751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5698ff2c3b2ac57e01a62d67a3db55da973d6c6dcf598c2408460267f3b11cbd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:19:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 05:19:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 05:30:44 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 05:30:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 05:30:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 05:30:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 05:30:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:30:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 05:30:44 GMT
CMD ["irb"]
# Wed, 20 May 2026 08:50:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 08:50:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 08:50:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 08:50:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 08:50:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 08:50:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 08:50:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 08:50:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 08:50:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 08:50:04 GMT
USER fluent
# Wed, 20 May 2026 08:50:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 08:50:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f690f4ce037264685118208392ba68615b070bc6f389b1e1885a1093b000b1f0`  
		Last Modified: Wed, 20 May 2026 05:23:51 GMT  
		Size: 1.3 MB (1310365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4e33c6b3845011d63383976c646a4dcd0c10a4713aba30ef20741a1896eb7f`  
		Last Modified: Wed, 20 May 2026 05:23:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe6678da6048b1e50dc773fe29b467aa363454d05597952dd57edad830c5353`  
		Last Modified: Wed, 20 May 2026 05:31:05 GMT  
		Size: 39.5 MB (39532615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5bff98a4e0df97e1384614181c51b83eebf65b689cf70c36d9a1b26734d75`  
		Last Modified: Wed, 20 May 2026 05:31:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb20c3317469b094fe8180f90d46e40dba015565bd05b35ce3c89be027a1668`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 6.6 MB (6589922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59651207e6bbd9adae5168f59e1bc2063370398010c50456fbf0c931ae89ce2d`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4713f74fa0ffb3c0b2142c3e03c518a022ecc9e6b4b6b3a5bb14439814f5b8e3`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbcb96a0ff2c8ac18fd477ba11a8541a44a668cc75d8ce01dcac496a1638bbc`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:014402d5443a94f2c18d0e9ff317f9fb8fbc35b46dc3192b23c3b3369239df17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567ebb2fc729ff8c19eb36b4e429500ccfb8dfba9937e61a8d68b10f55b96393`

```dockerfile
```

-	Layers:
	-	`sha256:410daf5971803e3d0c439a4e0604f8a3d8f6e9e6acdc6d3bfffbe70f3e7a7b8c`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 2.3 MB (2285357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9061b52197119010fb6dd03ae9101d03db1c8f48b7212b371d00f507bffc0a13`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:8dd53004a497bfad0ccc505119653b4cb98957304ad0e09434abd4e05d759ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb565636cec41efec7fdd058360af949ea1b207261427e2a1d5201545852a94`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:31:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:36:54 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 01:36:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:36:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:36:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:36:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:36:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:36:54 GMT
CMD ["irb"]
# Wed, 20 May 2026 02:49:46 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 02:49:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 02:49:46 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 02:49:46 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 02:49:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 02:49:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 02:49:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 02:49:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 02:49:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 02:49:46 GMT
USER fluent
# Wed, 20 May 2026 02:49:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 02:49:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affe7ff5a6816636d316cab96ab4ec627f6e94e4d270f3c01c842db6eea57b6f`  
		Last Modified: Wed, 20 May 2026 01:33:59 GMT  
		Size: 1.3 MB (1294927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4902876f154cc5231cbb8f09b165c7a1d8b9724ac03ed3fca0b398366de5fa`  
		Last Modified: Wed, 20 May 2026 01:33:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310d4b6bd5ac5f0cc164b6ab59e2ae6eb73067560ccb6b6e520297cdef1a983a`  
		Last Modified: Wed, 20 May 2026 01:37:08 GMT  
		Size: 39.2 MB (39207831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd386c7dfc77967e8045d8c6a68f53eaa51530b4b2963b25db4e5046a2f6e0c`  
		Last Modified: Wed, 20 May 2026 01:37:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5322372e9b5d777948aabd3791612864ff0a519e266990e6a3c615ad7ca8421f`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 6.4 MB (6447242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0183570fe8eaac934be4d9bb87824272f14093a8281235578299a8aa534a09`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964711b1e73271d5128a6436d93cd01ec2d45e5fd97c54978edf0741024109a6`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaad4409f71b88d7c936f76fe42a9c95ef1cb34a7a9384a6d72afc6cc725283`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:f5ef1068109c2e5e591362f5c238613e323d69f1d89b663a5d69ceda33a2188a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f203037d1ff5db53c4b41c69a9ac02bc565f4db06969b818a8ecbd9308d33969`

```dockerfile
```

-	Layers:
	-	`sha256:414057adf61949a138d296a9d8eedbcbfac679cfb4771026fa1f193e555e69b2`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 2.3 MB (2283267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d337cd30077e00434f231a07bee455acd6b4368b4e67760acc304e9401a7b292`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:a8afee19237b7c269e0ad943f4d7b66cf290d1aecf856fe7f6f480d5ad577b87
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
$ docker pull fluentd@sha256:00f76d25091b25cf42af10b5b8b0e184ef46c37da9654754581f727063be9856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79255022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62910f165807c3441ceadffa6ecaaa96fd0df004c645b721b1bcde139249569`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:51:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:34 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 19 May 2026 23:53:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:34 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:34 GMT
CMD ["irb"]
# Wed, 20 May 2026 00:42:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 00:42:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 00:42:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 00:42:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 00:42:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 00:42:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 00:42:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 00:42:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 00:42:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 00:42:42 GMT
USER fluent
# Wed, 20 May 2026 00:42:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 00:42:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae509a998d8cc25f86fa4f526ccfd3705bd9f1cdca6b1b3e5dde600c5503c8f8`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 1.3 MB (1279968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74962092651f83b43187b825e403ac93d24a5181f9ce1560f2048cb675a93a3`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3262473bfa79eafa8c9058c39e428100724eeb68ce81266365aa60667dffafe`  
		Last Modified: Tue, 19 May 2026 23:53:43 GMT  
		Size: 42.1 MB (42127140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba9eca8660ca68e09841c5da2d4e95a207217797f889c661969cd56adadb63d`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a9eb26a7e329dced11d3949926d121f7c796c796b1fc11f7b12985503d850`  
		Last Modified: Wed, 20 May 2026 00:42:53 GMT  
		Size: 6.1 MB (6065591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ae1d65594255316e8b520c558272744cf5de02d0e70e88fd27cca5472022c9`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff9be9611b0755a0d7c799c2b31f819f7441dd1bd513d3ed78f20070a5e8c04`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d30ebd71cff00e52701b7628b7438f5eb05107462f3c16c488ae63115c29ce6`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5c9e8fddecf115ca8ef240cc97838dac301ebad813f0f4bb97fb4a2df8663223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd3d78ccc58da38f5c9784225881c8f8e808b08b3a013d1bcc82291d46b4027`

```dockerfile
```

-	Layers:
	-	`sha256:69756b18478f4cc81288a43dc2b274637ab0808892f69299c7a46ce2bc4f376b`  
		Last Modified: Wed, 20 May 2026 00:42:53 GMT  
		Size: 2.3 MB (2281822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4464ac2f2e453244abc0de5ed98d4a248c543e78699b999dd1652d669fdedf78`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3deeebb820fbfa4c392f5bf9a0698e6fe21c35187f8fd6543d4b665b3660a1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73112123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a45a7c8d6b7dab645bfc30843eb6f32797714e337f1844a353ab4b47e23bd4c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:36:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:36:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:39:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 00:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:39:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:39:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:39:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:39:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:39:20 GMT
CMD ["irb"]
# Wed, 20 May 2026 01:54:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 01:54:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 01:54:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 01:54:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 01:54:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 01:54:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 01:54:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 01:54:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 01:54:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 01:54:14 GMT
USER fluent
# Wed, 20 May 2026 01:54:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 01:54:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96895aa837a127026eac95d26c75abbb54babbb5e762050dadd64de4a4cdf26b`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 1.3 MB (1263760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab57a91c1b877ddd64d9568132be395821962d3f9abd509d21b78fbb37d4ce59`  
		Last Modified: Wed, 20 May 2026 00:39:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7c7a49c9a601347b5bc7885069679efc572a7d07d471b0d729f46f3f26606`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 37.9 MB (37924207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae01ed4844d48ccad3e6e0c04da1c92633f098629f45d62660416eba51d518d`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435e0feeac4798a35e86ed15b1039dcbd7564a9d1463c1d272f71afdf4b5a6c7`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 6.0 MB (5967895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a88cbf410a462245cdf6c313f99016571ca1333a989f427d18cc0d8af13d1d`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a511f40be0082bccf64ada0f042b0817dce09d595da6ea8ffac8ba4a47af61`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b4d5734bead9accdc01648bf81a931cdab381f24a53c405d69d26d7740f4e4`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4fbbf16de9fd37b8ad02ffc8ff711f6fb23db4db59ca30ef6b7a479d63be9911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac22b6680d7de4ef960a8ba1f903176de9f4d275f4307e36b4508e8e2c78785`

```dockerfile
```

-	Layers:
	-	`sha256:ffc4528a925dfb651506aa4af4d84b57e259458e081ff07bc63d3fac108efda9`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 2.3 MB (2284793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69f5031a63ffa26d07f230fc90c0cd130909dd2454f15aad4f5becee518760d4`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:17b4125ec36408635ec7cfa349a5ed826017e2bf7e5c44206a2a69682ba3f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70960827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eba3e25015f42e83adbf7a505edf08f56ea185dd7d2275e1d653fc44da17273`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:12:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:15:11 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 01:15:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:15:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:15:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:15:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:15:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:15:11 GMT
CMD ["irb"]
# Wed, 20 May 2026 02:18:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 02:18:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 02:18:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 02:18:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 02:18:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 02:18:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 02:18:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 02:18:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 02:18:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 02:18:51 GMT
USER fluent
# Wed, 20 May 2026 02:18:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 02:18:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0e18f2eb3a8e56bd5a9ae9ab99db08dcf4799a8c083e10a4634e7b53fd7f2`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 1.2 MB (1237685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99435c1ef4eea2241c80a26de27a40623cbd18ae90074a36770ba95dd49ee2e`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4f726d4647f840eb32e17ab3eac6cd69521f1b0ea37a25100585f11ab43f2c`  
		Last Modified: Wed, 20 May 2026 01:15:20 GMT  
		Size: 37.8 MB (37781022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418179391d555c02f2342c5b411ca11f3df309ba00f80724924c50cd1369500`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015697a1eccf89e0b031fe60053f9a706b1a2b8b2f06ae62e7ce9959fbfd1e8f`  
		Last Modified: Wed, 20 May 2026 02:19:00 GMT  
		Size: 5.7 MB (5733897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bc52d940d104b1c67a9254a4647201fc4de5287bc08f7f67a7fedc3d96d161`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641b991a2723adf71945a9dca05376e4908849b4846c28b4b082949bdee94ce0`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd085d4f1bd88ed9d7df2521f8dc417ec111dd4d70c32a5cd07f33a0aa13ad1a`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b3aa02b23374c872acce7d6637246def14b74cfa03be1e25e51ab9603936b181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc08142d2f496ae5d62f9e06db6eacac4419377aecaae6e62ba38141a6ab582`

```dockerfile
```

-	Layers:
	-	`sha256:ccd7c8b017d42e010b1e7b8b4e8efb4664779c34f51ec4d43129fc5b42c63e19`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 2.3 MB (2283234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a949fdba9ae187c7a9ff9ac9d419614042df451a2343917d40cc425ffefb7692`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:ce3631f5ca630ab6347a9df8f96824c814e7f49fb24e536cbfa5c302face8cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79544961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c70ed8618efb22b7953c7f3b73edc4e61129698e809006b4a660a229e1e7b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:59:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:01:38 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 00:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:01:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:01:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:01:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:01:38 GMT
CMD ["irb"]
# Wed, 20 May 2026 00:45:26 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 00:45:26 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 00:45:26 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 00:45:26 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 00:45:26 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 00:45:26 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 00:45:26 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 00:45:26 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 00:45:26 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 00:45:26 GMT
USER fluent
# Wed, 20 May 2026 00:45:26 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 00:45:26 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0598190532e5fd5fa7f406a5f319138ca25758feb0a64da1b3449f88ee3521`  
		Last Modified: Wed, 20 May 2026 00:01:47 GMT  
		Size: 1.3 MB (1262002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15451c3fcbf117446c70cfdc658a97fef17103b8aac67f9d0f6802d157bd9b46`  
		Last Modified: Wed, 20 May 2026 00:01:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f64a0da9b1063193969c2698804e6a46b382e111eaf1458b40462d9cfe9d2f6`  
		Last Modified: Wed, 20 May 2026 00:01:48 GMT  
		Size: 42.1 MB (42078709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b2a3b4652676c008170445be657c4eb9ad8e3438b155e354ce5530a206af77`  
		Last Modified: Wed, 20 May 2026 00:01:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c468e08f650d3fff69045c6c8375b0a6c8a16d598528d7615fd37b3b57ec048`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 6.1 MB (6059940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e6ef0caacaf679fbbbd825fa41b30bd764a7d8245761de4517c992ae005bb`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04afc7675db41ded07504e36e5275da1bbcafcb0c24b8ae92c8cecaa8e7dd842`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc75834da573e2d5e8b320011cc488ea14c4991de83d8301f3d53e1c75c7b358`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1ab31f62a213d35770ef2044e29445ac0521d04ed3dd854d1f1378ddf3109e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d3b20a204acc80741a498fb9d4108366013dac8043dd87c9ccbcf9f5f2692`

```dockerfile
```

-	Layers:
	-	`sha256:5c7f3e39d6f5e68a0e9b8bf80c02dab50eac63bf0943af51de24ea1d34099e4a`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 2.3 MB (2282086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0f0cc04971ca7d3fa62832f8578b0f4e5c0d3098839dda7bf0c54caa537224`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:c410b212e6cdfc4092aacc1cce7dc5e1bbb7019fd56b8bc46cef136714c77934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76286643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66240acb7cefc429d068f7e294fbcc57cc4e40359a5c6e7e230bfaabd864ff76`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:50:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 19 May 2026 23:53:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:20 GMT
CMD ["irb"]
# Wed, 20 May 2026 03:02:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 03:02:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 03:02:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 03:02:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 03:02:10 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 03:02:10 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 03:02:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 03:02:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 03:02:10 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 03:02:10 GMT
USER fluent
# Wed, 20 May 2026 03:02:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 03:02:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af0b86f8e074f8013394c8982e198a1696c4342a8a353df1261a9436c962fc9`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 1.3 MB (1287842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b478f5fd5d558d3bc5b16b7358ad81ffe9e90dd8bc53036a1e39466601cef7`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04ada0bbc123da7765a41ed03bd4930b19f6d3d5b7e7a44c1387ac2fcadd1d6`  
		Last Modified: Tue, 19 May 2026 23:53:29 GMT  
		Size: 37.7 MB (37661953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55408ceb22509be948980234f637e5a5ae7adf6e80d24588739f6d90684f6216`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931a4801406d68f7b0827fd601ff8d85c52ab40f6ec0eb8c93e5a2f68fd850d0`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 6.0 MB (6039122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e24965accd62ef1ba63bcda357831f008d5a4a8e3617dddb25eaa65a024729`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2599cc634f1448c59392feca518e7674b2ddb84e80dd929c0d148c72e379ca16`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5002f177266084489472144ecab94c108374732a7e59372ba5a8b2b7246c1d59`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cb0ae3f7faf6ea5bde3c605d94ebacdca656cc30d5a2ea84e185038d80ce97e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2322a8ffe133a3f97e021d2664428ee0363fbdd607c2d35fc5fe47861d5146d0`

```dockerfile
```

-	Layers:
	-	`sha256:4151cea6497c446e934bc121c3af58b3da29964f63ecd3edbb446fa9278fcadd`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 2.3 MB (2279010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4745c54e86bea1ab62463a9b51c5d5fb518733e07ae2e73070c9f3947738854d`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:2bd708cb0638677b5220c6d97aa100b65010de3ca9c61de375812de9b67f1408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81035751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5698ff2c3b2ac57e01a62d67a3db55da973d6c6dcf598c2408460267f3b11cbd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:19:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 05:19:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 05:30:44 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 05:30:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 05:30:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 05:30:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 05:30:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:30:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 05:30:44 GMT
CMD ["irb"]
# Wed, 20 May 2026 08:50:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 08:50:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 08:50:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 08:50:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 08:50:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 08:50:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 08:50:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 08:50:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 08:50:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 08:50:04 GMT
USER fluent
# Wed, 20 May 2026 08:50:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 08:50:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f690f4ce037264685118208392ba68615b070bc6f389b1e1885a1093b000b1f0`  
		Last Modified: Wed, 20 May 2026 05:23:51 GMT  
		Size: 1.3 MB (1310365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4e33c6b3845011d63383976c646a4dcd0c10a4713aba30ef20741a1896eb7f`  
		Last Modified: Wed, 20 May 2026 05:23:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe6678da6048b1e50dc773fe29b467aa363454d05597952dd57edad830c5353`  
		Last Modified: Wed, 20 May 2026 05:31:05 GMT  
		Size: 39.5 MB (39532615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5bff98a4e0df97e1384614181c51b83eebf65b689cf70c36d9a1b26734d75`  
		Last Modified: Wed, 20 May 2026 05:31:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb20c3317469b094fe8180f90d46e40dba015565bd05b35ce3c89be027a1668`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 6.6 MB (6589922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59651207e6bbd9adae5168f59e1bc2063370398010c50456fbf0c931ae89ce2d`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4713f74fa0ffb3c0b2142c3e03c518a022ecc9e6b4b6b3a5bb14439814f5b8e3`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbcb96a0ff2c8ac18fd477ba11a8541a44a668cc75d8ce01dcac496a1638bbc`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:014402d5443a94f2c18d0e9ff317f9fb8fbc35b46dc3192b23c3b3369239df17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567ebb2fc729ff8c19eb36b4e429500ccfb8dfba9937e61a8d68b10f55b96393`

```dockerfile
```

-	Layers:
	-	`sha256:410daf5971803e3d0c439a4e0604f8a3d8f6e9e6acdc6d3bfffbe70f3e7a7b8c`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 2.3 MB (2285357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9061b52197119010fb6dd03ae9101d03db1c8f48b7212b371d00f507bffc0a13`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; s390x

```console
$ docker pull fluentd@sha256:8dd53004a497bfad0ccc505119653b4cb98957304ad0e09434abd4e05d759ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb565636cec41efec7fdd058360af949ea1b207261427e2a1d5201545852a94`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:31:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:36:54 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 01:36:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:36:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:36:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:36:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:36:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:36:54 GMT
CMD ["irb"]
# Wed, 20 May 2026 02:49:46 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 02:49:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 02:49:46 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 02:49:46 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 02:49:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 02:49:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 02:49:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 02:49:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 02:49:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 02:49:46 GMT
USER fluent
# Wed, 20 May 2026 02:49:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 02:49:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affe7ff5a6816636d316cab96ab4ec627f6e94e4d270f3c01c842db6eea57b6f`  
		Last Modified: Wed, 20 May 2026 01:33:59 GMT  
		Size: 1.3 MB (1294927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4902876f154cc5231cbb8f09b165c7a1d8b9724ac03ed3fca0b398366de5fa`  
		Last Modified: Wed, 20 May 2026 01:33:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310d4b6bd5ac5f0cc164b6ab59e2ae6eb73067560ccb6b6e520297cdef1a983a`  
		Last Modified: Wed, 20 May 2026 01:37:08 GMT  
		Size: 39.2 MB (39207831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd386c7dfc77967e8045d8c6a68f53eaa51530b4b2963b25db4e5046a2f6e0c`  
		Last Modified: Wed, 20 May 2026 01:37:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5322372e9b5d777948aabd3791612864ff0a519e266990e6a3c615ad7ca8421f`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 6.4 MB (6447242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0183570fe8eaac934be4d9bb87824272f14093a8281235578299a8aa534a09`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964711b1e73271d5128a6436d93cd01ec2d45e5fd97c54978edf0741024109a6`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaad4409f71b88d7c936f76fe42a9c95ef1cb34a7a9384a6d72afc6cc725283`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f5ef1068109c2e5e591362f5c238613e323d69f1d89b663a5d69ceda33a2188a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f203037d1ff5db53c4b41c69a9ac02bc565f4db06969b818a8ecbd9308d33969`

```dockerfile
```

-	Layers:
	-	`sha256:414057adf61949a138d296a9d8eedbcbfac679cfb4771026fa1f193e555e69b2`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 2.3 MB (2283267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d337cd30077e00434f231a07bee455acd6b4368b4e67760acc304e9401a7b292`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:a8afee19237b7c269e0ad943f4d7b66cf290d1aecf856fe7f6f480d5ad577b87
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
$ docker pull fluentd@sha256:00f76d25091b25cf42af10b5b8b0e184ef46c37da9654754581f727063be9856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79255022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62910f165807c3441ceadffa6ecaaa96fd0df004c645b721b1bcde139249569`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:51:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:34 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 19 May 2026 23:53:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:34 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:34 GMT
CMD ["irb"]
# Wed, 20 May 2026 00:42:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 00:42:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 00:42:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 00:42:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 00:42:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 00:42:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 00:42:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 00:42:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 00:42:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 00:42:42 GMT
USER fluent
# Wed, 20 May 2026 00:42:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 00:42:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae509a998d8cc25f86fa4f526ccfd3705bd9f1cdca6b1b3e5dde600c5503c8f8`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 1.3 MB (1279968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74962092651f83b43187b825e403ac93d24a5181f9ce1560f2048cb675a93a3`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3262473bfa79eafa8c9058c39e428100724eeb68ce81266365aa60667dffafe`  
		Last Modified: Tue, 19 May 2026 23:53:43 GMT  
		Size: 42.1 MB (42127140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba9eca8660ca68e09841c5da2d4e95a207217797f889c661969cd56adadb63d`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a9eb26a7e329dced11d3949926d121f7c796c796b1fc11f7b12985503d850`  
		Last Modified: Wed, 20 May 2026 00:42:53 GMT  
		Size: 6.1 MB (6065591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ae1d65594255316e8b520c558272744cf5de02d0e70e88fd27cca5472022c9`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff9be9611b0755a0d7c799c2b31f819f7441dd1bd513d3ed78f20070a5e8c04`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d30ebd71cff00e52701b7628b7438f5eb05107462f3c16c488ae63115c29ce6`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5c9e8fddecf115ca8ef240cc97838dac301ebad813f0f4bb97fb4a2df8663223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd3d78ccc58da38f5c9784225881c8f8e808b08b3a013d1bcc82291d46b4027`

```dockerfile
```

-	Layers:
	-	`sha256:69756b18478f4cc81288a43dc2b274637ab0808892f69299c7a46ce2bc4f376b`  
		Last Modified: Wed, 20 May 2026 00:42:53 GMT  
		Size: 2.3 MB (2281822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4464ac2f2e453244abc0de5ed98d4a248c543e78699b999dd1652d669fdedf78`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3deeebb820fbfa4c392f5bf9a0698e6fe21c35187f8fd6543d4b665b3660a1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73112123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a45a7c8d6b7dab645bfc30843eb6f32797714e337f1844a353ab4b47e23bd4c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:36:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:36:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:39:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 00:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:39:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:39:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:39:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:39:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:39:20 GMT
CMD ["irb"]
# Wed, 20 May 2026 01:54:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 01:54:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 01:54:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 01:54:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 01:54:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 01:54:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 01:54:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 01:54:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 01:54:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 01:54:14 GMT
USER fluent
# Wed, 20 May 2026 01:54:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 01:54:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96895aa837a127026eac95d26c75abbb54babbb5e762050dadd64de4a4cdf26b`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 1.3 MB (1263760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab57a91c1b877ddd64d9568132be395821962d3f9abd509d21b78fbb37d4ce59`  
		Last Modified: Wed, 20 May 2026 00:39:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7c7a49c9a601347b5bc7885069679efc572a7d07d471b0d729f46f3f26606`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 37.9 MB (37924207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae01ed4844d48ccad3e6e0c04da1c92633f098629f45d62660416eba51d518d`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435e0feeac4798a35e86ed15b1039dcbd7564a9d1463c1d272f71afdf4b5a6c7`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 6.0 MB (5967895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a88cbf410a462245cdf6c313f99016571ca1333a989f427d18cc0d8af13d1d`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a511f40be0082bccf64ada0f042b0817dce09d595da6ea8ffac8ba4a47af61`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b4d5734bead9accdc01648bf81a931cdab381f24a53c405d69d26d7740f4e4`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4fbbf16de9fd37b8ad02ffc8ff711f6fb23db4db59ca30ef6b7a479d63be9911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac22b6680d7de4ef960a8ba1f903176de9f4d275f4307e36b4508e8e2c78785`

```dockerfile
```

-	Layers:
	-	`sha256:ffc4528a925dfb651506aa4af4d84b57e259458e081ff07bc63d3fac108efda9`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 2.3 MB (2284793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69f5031a63ffa26d07f230fc90c0cd130909dd2454f15aad4f5becee518760d4`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:17b4125ec36408635ec7cfa349a5ed826017e2bf7e5c44206a2a69682ba3f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70960827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eba3e25015f42e83adbf7a505edf08f56ea185dd7d2275e1d653fc44da17273`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:12:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:15:11 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 01:15:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:15:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:15:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:15:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:15:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:15:11 GMT
CMD ["irb"]
# Wed, 20 May 2026 02:18:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 02:18:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 02:18:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 02:18:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 02:18:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 02:18:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 02:18:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 02:18:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 02:18:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 02:18:51 GMT
USER fluent
# Wed, 20 May 2026 02:18:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 02:18:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0e18f2eb3a8e56bd5a9ae9ab99db08dcf4799a8c083e10a4634e7b53fd7f2`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 1.2 MB (1237685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99435c1ef4eea2241c80a26de27a40623cbd18ae90074a36770ba95dd49ee2e`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4f726d4647f840eb32e17ab3eac6cd69521f1b0ea37a25100585f11ab43f2c`  
		Last Modified: Wed, 20 May 2026 01:15:20 GMT  
		Size: 37.8 MB (37781022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418179391d555c02f2342c5b411ca11f3df309ba00f80724924c50cd1369500`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015697a1eccf89e0b031fe60053f9a706b1a2b8b2f06ae62e7ce9959fbfd1e8f`  
		Last Modified: Wed, 20 May 2026 02:19:00 GMT  
		Size: 5.7 MB (5733897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bc52d940d104b1c67a9254a4647201fc4de5287bc08f7f67a7fedc3d96d161`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641b991a2723adf71945a9dca05376e4908849b4846c28b4b082949bdee94ce0`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd085d4f1bd88ed9d7df2521f8dc417ec111dd4d70c32a5cd07f33a0aa13ad1a`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b3aa02b23374c872acce7d6637246def14b74cfa03be1e25e51ab9603936b181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc08142d2f496ae5d62f9e06db6eacac4419377aecaae6e62ba38141a6ab582`

```dockerfile
```

-	Layers:
	-	`sha256:ccd7c8b017d42e010b1e7b8b4e8efb4664779c34f51ec4d43129fc5b42c63e19`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 2.3 MB (2283234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a949fdba9ae187c7a9ff9ac9d419614042df451a2343917d40cc425ffefb7692`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:ce3631f5ca630ab6347a9df8f96824c814e7f49fb24e536cbfa5c302face8cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79544961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c70ed8618efb22b7953c7f3b73edc4e61129698e809006b4a660a229e1e7b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:59:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:01:38 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 00:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:01:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:01:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:01:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:01:38 GMT
CMD ["irb"]
# Wed, 20 May 2026 00:45:26 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 00:45:26 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 00:45:26 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 00:45:26 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 00:45:26 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 00:45:26 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 00:45:26 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 00:45:26 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 00:45:26 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 00:45:26 GMT
USER fluent
# Wed, 20 May 2026 00:45:26 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 00:45:26 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0598190532e5fd5fa7f406a5f319138ca25758feb0a64da1b3449f88ee3521`  
		Last Modified: Wed, 20 May 2026 00:01:47 GMT  
		Size: 1.3 MB (1262002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15451c3fcbf117446c70cfdc658a97fef17103b8aac67f9d0f6802d157bd9b46`  
		Last Modified: Wed, 20 May 2026 00:01:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f64a0da9b1063193969c2698804e6a46b382e111eaf1458b40462d9cfe9d2f6`  
		Last Modified: Wed, 20 May 2026 00:01:48 GMT  
		Size: 42.1 MB (42078709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b2a3b4652676c008170445be657c4eb9ad8e3438b155e354ce5530a206af77`  
		Last Modified: Wed, 20 May 2026 00:01:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c468e08f650d3fff69045c6c8375b0a6c8a16d598528d7615fd37b3b57ec048`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 6.1 MB (6059940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e6ef0caacaf679fbbbd825fa41b30bd764a7d8245761de4517c992ae005bb`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04afc7675db41ded07504e36e5275da1bbcafcb0c24b8ae92c8cecaa8e7dd842`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc75834da573e2d5e8b320011cc488ea14c4991de83d8301f3d53e1c75c7b358`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:1ab31f62a213d35770ef2044e29445ac0521d04ed3dd854d1f1378ddf3109e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d3b20a204acc80741a498fb9d4108366013dac8043dd87c9ccbcf9f5f2692`

```dockerfile
```

-	Layers:
	-	`sha256:5c7f3e39d6f5e68a0e9b8bf80c02dab50eac63bf0943af51de24ea1d34099e4a`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 2.3 MB (2282086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0f0cc04971ca7d3fa62832f8578b0f4e5c0d3098839dda7bf0c54caa537224`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:c410b212e6cdfc4092aacc1cce7dc5e1bbb7019fd56b8bc46cef136714c77934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76286643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66240acb7cefc429d068f7e294fbcc57cc4e40359a5c6e7e230bfaabd864ff76`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:50:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 19 May 2026 23:53:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:20 GMT
CMD ["irb"]
# Wed, 20 May 2026 03:02:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 03:02:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 03:02:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 03:02:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 03:02:10 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 03:02:10 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 03:02:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 03:02:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 03:02:10 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 03:02:10 GMT
USER fluent
# Wed, 20 May 2026 03:02:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 03:02:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af0b86f8e074f8013394c8982e198a1696c4342a8a353df1261a9436c962fc9`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 1.3 MB (1287842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b478f5fd5d558d3bc5b16b7358ad81ffe9e90dd8bc53036a1e39466601cef7`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04ada0bbc123da7765a41ed03bd4930b19f6d3d5b7e7a44c1387ac2fcadd1d6`  
		Last Modified: Tue, 19 May 2026 23:53:29 GMT  
		Size: 37.7 MB (37661953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55408ceb22509be948980234f637e5a5ae7adf6e80d24588739f6d90684f6216`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931a4801406d68f7b0827fd601ff8d85c52ab40f6ec0eb8c93e5a2f68fd850d0`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 6.0 MB (6039122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e24965accd62ef1ba63bcda357831f008d5a4a8e3617dddb25eaa65a024729`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2599cc634f1448c59392feca518e7674b2ddb84e80dd929c0d148c72e379ca16`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5002f177266084489472144ecab94c108374732a7e59372ba5a8b2b7246c1d59`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:cb0ae3f7faf6ea5bde3c605d94ebacdca656cc30d5a2ea84e185038d80ce97e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2322a8ffe133a3f97e021d2664428ee0363fbdd607c2d35fc5fe47861d5146d0`

```dockerfile
```

-	Layers:
	-	`sha256:4151cea6497c446e934bc121c3af58b3da29964f63ecd3edbb446fa9278fcadd`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 2.3 MB (2279010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4745c54e86bea1ab62463a9b51c5d5fb518733e07ae2e73070c9f3947738854d`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:2bd708cb0638677b5220c6d97aa100b65010de3ca9c61de375812de9b67f1408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81035751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5698ff2c3b2ac57e01a62d67a3db55da973d6c6dcf598c2408460267f3b11cbd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:19:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 05:19:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 05:30:44 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 05:30:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 05:30:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 05:30:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 05:30:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:30:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 05:30:44 GMT
CMD ["irb"]
# Wed, 20 May 2026 08:50:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 08:50:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 08:50:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 08:50:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 08:50:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 08:50:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 08:50:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 08:50:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 08:50:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 08:50:04 GMT
USER fluent
# Wed, 20 May 2026 08:50:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 08:50:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f690f4ce037264685118208392ba68615b070bc6f389b1e1885a1093b000b1f0`  
		Last Modified: Wed, 20 May 2026 05:23:51 GMT  
		Size: 1.3 MB (1310365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4e33c6b3845011d63383976c646a4dcd0c10a4713aba30ef20741a1896eb7f`  
		Last Modified: Wed, 20 May 2026 05:23:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe6678da6048b1e50dc773fe29b467aa363454d05597952dd57edad830c5353`  
		Last Modified: Wed, 20 May 2026 05:31:05 GMT  
		Size: 39.5 MB (39532615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5bff98a4e0df97e1384614181c51b83eebf65b689cf70c36d9a1b26734d75`  
		Last Modified: Wed, 20 May 2026 05:31:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb20c3317469b094fe8180f90d46e40dba015565bd05b35ce3c89be027a1668`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 6.6 MB (6589922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59651207e6bbd9adae5168f59e1bc2063370398010c50456fbf0c931ae89ce2d`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4713f74fa0ffb3c0b2142c3e03c518a022ecc9e6b4b6b3a5bb14439814f5b8e3`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbcb96a0ff2c8ac18fd477ba11a8541a44a668cc75d8ce01dcac496a1638bbc`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:014402d5443a94f2c18d0e9ff317f9fb8fbc35b46dc3192b23c3b3369239df17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567ebb2fc729ff8c19eb36b4e429500ccfb8dfba9937e61a8d68b10f55b96393`

```dockerfile
```

-	Layers:
	-	`sha256:410daf5971803e3d0c439a4e0604f8a3d8f6e9e6acdc6d3bfffbe70f3e7a7b8c`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 2.3 MB (2285357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9061b52197119010fb6dd03ae9101d03db1c8f48b7212b371d00f507bffc0a13`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:8dd53004a497bfad0ccc505119653b4cb98957304ad0e09434abd4e05d759ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb565636cec41efec7fdd058360af949ea1b207261427e2a1d5201545852a94`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:31:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:36:54 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 01:36:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:36:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:36:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:36:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:36:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:36:54 GMT
CMD ["irb"]
# Wed, 20 May 2026 02:49:46 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 02:49:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 02:49:46 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 02:49:46 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 02:49:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 02:49:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 02:49:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 02:49:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 02:49:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 02:49:46 GMT
USER fluent
# Wed, 20 May 2026 02:49:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 02:49:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affe7ff5a6816636d316cab96ab4ec627f6e94e4d270f3c01c842db6eea57b6f`  
		Last Modified: Wed, 20 May 2026 01:33:59 GMT  
		Size: 1.3 MB (1294927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4902876f154cc5231cbb8f09b165c7a1d8b9724ac03ed3fca0b398366de5fa`  
		Last Modified: Wed, 20 May 2026 01:33:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310d4b6bd5ac5f0cc164b6ab59e2ae6eb73067560ccb6b6e520297cdef1a983a`  
		Last Modified: Wed, 20 May 2026 01:37:08 GMT  
		Size: 39.2 MB (39207831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd386c7dfc77967e8045d8c6a68f53eaa51530b4b2963b25db4e5046a2f6e0c`  
		Last Modified: Wed, 20 May 2026 01:37:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5322372e9b5d777948aabd3791612864ff0a519e266990e6a3c615ad7ca8421f`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 6.4 MB (6447242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0183570fe8eaac934be4d9bb87824272f14093a8281235578299a8aa534a09`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964711b1e73271d5128a6436d93cd01ec2d45e5fd97c54978edf0741024109a6`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaad4409f71b88d7c936f76fe42a9c95ef1cb34a7a9384a6d72afc6cc725283`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f5ef1068109c2e5e591362f5c238613e323d69f1d89b663a5d69ceda33a2188a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f203037d1ff5db53c4b41c69a9ac02bc565f4db06969b818a8ecbd9308d33969`

```dockerfile
```

-	Layers:
	-	`sha256:414057adf61949a138d296a9d8eedbcbfac679cfb4771026fa1f193e555e69b2`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 2.3 MB (2283267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d337cd30077e00434f231a07bee455acd6b4368b4e67760acc304e9401a7b292`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-1.0`

```console
$ docker pull fluentd@sha256:a8afee19237b7c269e0ad943f4d7b66cf290d1aecf856fe7f6f480d5ad577b87
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
$ docker pull fluentd@sha256:00f76d25091b25cf42af10b5b8b0e184ef46c37da9654754581f727063be9856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79255022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62910f165807c3441ceadffa6ecaaa96fd0df004c645b721b1bcde139249569`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:51:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:34 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 19 May 2026 23:53:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:34 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:34 GMT
CMD ["irb"]
# Wed, 20 May 2026 00:42:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 00:42:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 00:42:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 00:42:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 00:42:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 00:42:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 00:42:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 00:42:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 00:42:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 00:42:42 GMT
USER fluent
# Wed, 20 May 2026 00:42:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 00:42:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae509a998d8cc25f86fa4f526ccfd3705bd9f1cdca6b1b3e5dde600c5503c8f8`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 1.3 MB (1279968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74962092651f83b43187b825e403ac93d24a5181f9ce1560f2048cb675a93a3`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3262473bfa79eafa8c9058c39e428100724eeb68ce81266365aa60667dffafe`  
		Last Modified: Tue, 19 May 2026 23:53:43 GMT  
		Size: 42.1 MB (42127140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba9eca8660ca68e09841c5da2d4e95a207217797f889c661969cd56adadb63d`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a9eb26a7e329dced11d3949926d121f7c796c796b1fc11f7b12985503d850`  
		Last Modified: Wed, 20 May 2026 00:42:53 GMT  
		Size: 6.1 MB (6065591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ae1d65594255316e8b520c558272744cf5de02d0e70e88fd27cca5472022c9`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff9be9611b0755a0d7c799c2b31f819f7441dd1bd513d3ed78f20070a5e8c04`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d30ebd71cff00e52701b7628b7438f5eb05107462f3c16c488ae63115c29ce6`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5c9e8fddecf115ca8ef240cc97838dac301ebad813f0f4bb97fb4a2df8663223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd3d78ccc58da38f5c9784225881c8f8e808b08b3a013d1bcc82291d46b4027`

```dockerfile
```

-	Layers:
	-	`sha256:69756b18478f4cc81288a43dc2b274637ab0808892f69299c7a46ce2bc4f376b`  
		Last Modified: Wed, 20 May 2026 00:42:53 GMT  
		Size: 2.3 MB (2281822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4464ac2f2e453244abc0de5ed98d4a248c543e78699b999dd1652d669fdedf78`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3deeebb820fbfa4c392f5bf9a0698e6fe21c35187f8fd6543d4b665b3660a1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73112123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a45a7c8d6b7dab645bfc30843eb6f32797714e337f1844a353ab4b47e23bd4c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:36:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:36:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:39:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 00:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:39:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:39:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:39:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:39:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:39:20 GMT
CMD ["irb"]
# Wed, 20 May 2026 01:54:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 01:54:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 01:54:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 01:54:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 01:54:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 01:54:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 01:54:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 01:54:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 01:54:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 01:54:14 GMT
USER fluent
# Wed, 20 May 2026 01:54:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 01:54:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96895aa837a127026eac95d26c75abbb54babbb5e762050dadd64de4a4cdf26b`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 1.3 MB (1263760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab57a91c1b877ddd64d9568132be395821962d3f9abd509d21b78fbb37d4ce59`  
		Last Modified: Wed, 20 May 2026 00:39:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7c7a49c9a601347b5bc7885069679efc572a7d07d471b0d729f46f3f26606`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 37.9 MB (37924207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae01ed4844d48ccad3e6e0c04da1c92633f098629f45d62660416eba51d518d`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435e0feeac4798a35e86ed15b1039dcbd7564a9d1463c1d272f71afdf4b5a6c7`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 6.0 MB (5967895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a88cbf410a462245cdf6c313f99016571ca1333a989f427d18cc0d8af13d1d`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a511f40be0082bccf64ada0f042b0817dce09d595da6ea8ffac8ba4a47af61`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b4d5734bead9accdc01648bf81a931cdab381f24a53c405d69d26d7740f4e4`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4fbbf16de9fd37b8ad02ffc8ff711f6fb23db4db59ca30ef6b7a479d63be9911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac22b6680d7de4ef960a8ba1f903176de9f4d275f4307e36b4508e8e2c78785`

```dockerfile
```

-	Layers:
	-	`sha256:ffc4528a925dfb651506aa4af4d84b57e259458e081ff07bc63d3fac108efda9`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 2.3 MB (2284793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69f5031a63ffa26d07f230fc90c0cd130909dd2454f15aad4f5becee518760d4`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:17b4125ec36408635ec7cfa349a5ed826017e2bf7e5c44206a2a69682ba3f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70960827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eba3e25015f42e83adbf7a505edf08f56ea185dd7d2275e1d653fc44da17273`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:12:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:15:11 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 01:15:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:15:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:15:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:15:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:15:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:15:11 GMT
CMD ["irb"]
# Wed, 20 May 2026 02:18:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 02:18:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 02:18:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 02:18:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 02:18:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 02:18:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 02:18:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 02:18:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 02:18:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 02:18:51 GMT
USER fluent
# Wed, 20 May 2026 02:18:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 02:18:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0e18f2eb3a8e56bd5a9ae9ab99db08dcf4799a8c083e10a4634e7b53fd7f2`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 1.2 MB (1237685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99435c1ef4eea2241c80a26de27a40623cbd18ae90074a36770ba95dd49ee2e`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4f726d4647f840eb32e17ab3eac6cd69521f1b0ea37a25100585f11ab43f2c`  
		Last Modified: Wed, 20 May 2026 01:15:20 GMT  
		Size: 37.8 MB (37781022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418179391d555c02f2342c5b411ca11f3df309ba00f80724924c50cd1369500`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015697a1eccf89e0b031fe60053f9a706b1a2b8b2f06ae62e7ce9959fbfd1e8f`  
		Last Modified: Wed, 20 May 2026 02:19:00 GMT  
		Size: 5.7 MB (5733897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bc52d940d104b1c67a9254a4647201fc4de5287bc08f7f67a7fedc3d96d161`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641b991a2723adf71945a9dca05376e4908849b4846c28b4b082949bdee94ce0`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd085d4f1bd88ed9d7df2521f8dc417ec111dd4d70c32a5cd07f33a0aa13ad1a`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b3aa02b23374c872acce7d6637246def14b74cfa03be1e25e51ab9603936b181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc08142d2f496ae5d62f9e06db6eacac4419377aecaae6e62ba38141a6ab582`

```dockerfile
```

-	Layers:
	-	`sha256:ccd7c8b017d42e010b1e7b8b4e8efb4664779c34f51ec4d43129fc5b42c63e19`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 2.3 MB (2283234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a949fdba9ae187c7a9ff9ac9d419614042df451a2343917d40cc425ffefb7692`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:ce3631f5ca630ab6347a9df8f96824c814e7f49fb24e536cbfa5c302face8cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79544961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c70ed8618efb22b7953c7f3b73edc4e61129698e809006b4a660a229e1e7b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:59:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:01:38 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 00:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:01:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:01:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:01:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:01:38 GMT
CMD ["irb"]
# Wed, 20 May 2026 00:45:26 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 00:45:26 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 00:45:26 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 00:45:26 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 00:45:26 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 00:45:26 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 00:45:26 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 00:45:26 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 00:45:26 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 00:45:26 GMT
USER fluent
# Wed, 20 May 2026 00:45:26 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 00:45:26 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0598190532e5fd5fa7f406a5f319138ca25758feb0a64da1b3449f88ee3521`  
		Last Modified: Wed, 20 May 2026 00:01:47 GMT  
		Size: 1.3 MB (1262002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15451c3fcbf117446c70cfdc658a97fef17103b8aac67f9d0f6802d157bd9b46`  
		Last Modified: Wed, 20 May 2026 00:01:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f64a0da9b1063193969c2698804e6a46b382e111eaf1458b40462d9cfe9d2f6`  
		Last Modified: Wed, 20 May 2026 00:01:48 GMT  
		Size: 42.1 MB (42078709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b2a3b4652676c008170445be657c4eb9ad8e3438b155e354ce5530a206af77`  
		Last Modified: Wed, 20 May 2026 00:01:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c468e08f650d3fff69045c6c8375b0a6c8a16d598528d7615fd37b3b57ec048`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 6.1 MB (6059940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e6ef0caacaf679fbbbd825fa41b30bd764a7d8245761de4517c992ae005bb`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04afc7675db41ded07504e36e5275da1bbcafcb0c24b8ae92c8cecaa8e7dd842`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc75834da573e2d5e8b320011cc488ea14c4991de83d8301f3d53e1c75c7b358`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1ab31f62a213d35770ef2044e29445ac0521d04ed3dd854d1f1378ddf3109e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d3b20a204acc80741a498fb9d4108366013dac8043dd87c9ccbcf9f5f2692`

```dockerfile
```

-	Layers:
	-	`sha256:5c7f3e39d6f5e68a0e9b8bf80c02dab50eac63bf0943af51de24ea1d34099e4a`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 2.3 MB (2282086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0f0cc04971ca7d3fa62832f8578b0f4e5c0d3098839dda7bf0c54caa537224`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:c410b212e6cdfc4092aacc1cce7dc5e1bbb7019fd56b8bc46cef136714c77934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76286643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66240acb7cefc429d068f7e294fbcc57cc4e40359a5c6e7e230bfaabd864ff76`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:50:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 19 May 2026 23:53:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:20 GMT
CMD ["irb"]
# Wed, 20 May 2026 03:02:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 03:02:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 03:02:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 03:02:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 03:02:10 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 03:02:10 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 03:02:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 03:02:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 03:02:10 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 03:02:10 GMT
USER fluent
# Wed, 20 May 2026 03:02:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 03:02:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af0b86f8e074f8013394c8982e198a1696c4342a8a353df1261a9436c962fc9`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 1.3 MB (1287842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b478f5fd5d558d3bc5b16b7358ad81ffe9e90dd8bc53036a1e39466601cef7`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04ada0bbc123da7765a41ed03bd4930b19f6d3d5b7e7a44c1387ac2fcadd1d6`  
		Last Modified: Tue, 19 May 2026 23:53:29 GMT  
		Size: 37.7 MB (37661953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55408ceb22509be948980234f637e5a5ae7adf6e80d24588739f6d90684f6216`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931a4801406d68f7b0827fd601ff8d85c52ab40f6ec0eb8c93e5a2f68fd850d0`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 6.0 MB (6039122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e24965accd62ef1ba63bcda357831f008d5a4a8e3617dddb25eaa65a024729`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2599cc634f1448c59392feca518e7674b2ddb84e80dd929c0d148c72e379ca16`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5002f177266084489472144ecab94c108374732a7e59372ba5a8b2b7246c1d59`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:cb0ae3f7faf6ea5bde3c605d94ebacdca656cc30d5a2ea84e185038d80ce97e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2322a8ffe133a3f97e021d2664428ee0363fbdd607c2d35fc5fe47861d5146d0`

```dockerfile
```

-	Layers:
	-	`sha256:4151cea6497c446e934bc121c3af58b3da29964f63ecd3edbb446fa9278fcadd`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 2.3 MB (2279010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4745c54e86bea1ab62463a9b51c5d5fb518733e07ae2e73070c9f3947738854d`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:2bd708cb0638677b5220c6d97aa100b65010de3ca9c61de375812de9b67f1408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81035751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5698ff2c3b2ac57e01a62d67a3db55da973d6c6dcf598c2408460267f3b11cbd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:19:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 05:19:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 05:30:44 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 05:30:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 05:30:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 05:30:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 05:30:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:30:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 05:30:44 GMT
CMD ["irb"]
# Wed, 20 May 2026 08:50:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 08:50:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 08:50:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 08:50:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 08:50:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 08:50:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 08:50:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 08:50:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 08:50:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 08:50:04 GMT
USER fluent
# Wed, 20 May 2026 08:50:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 08:50:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f690f4ce037264685118208392ba68615b070bc6f389b1e1885a1093b000b1f0`  
		Last Modified: Wed, 20 May 2026 05:23:51 GMT  
		Size: 1.3 MB (1310365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4e33c6b3845011d63383976c646a4dcd0c10a4713aba30ef20741a1896eb7f`  
		Last Modified: Wed, 20 May 2026 05:23:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe6678da6048b1e50dc773fe29b467aa363454d05597952dd57edad830c5353`  
		Last Modified: Wed, 20 May 2026 05:31:05 GMT  
		Size: 39.5 MB (39532615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5bff98a4e0df97e1384614181c51b83eebf65b689cf70c36d9a1b26734d75`  
		Last Modified: Wed, 20 May 2026 05:31:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb20c3317469b094fe8180f90d46e40dba015565bd05b35ce3c89be027a1668`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 6.6 MB (6589922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59651207e6bbd9adae5168f59e1bc2063370398010c50456fbf0c931ae89ce2d`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4713f74fa0ffb3c0b2142c3e03c518a022ecc9e6b4b6b3a5bb14439814f5b8e3`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbcb96a0ff2c8ac18fd477ba11a8541a44a668cc75d8ce01dcac496a1638bbc`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:014402d5443a94f2c18d0e9ff317f9fb8fbc35b46dc3192b23c3b3369239df17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567ebb2fc729ff8c19eb36b4e429500ccfb8dfba9937e61a8d68b10f55b96393`

```dockerfile
```

-	Layers:
	-	`sha256:410daf5971803e3d0c439a4e0604f8a3d8f6e9e6acdc6d3bfffbe70f3e7a7b8c`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 2.3 MB (2285357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9061b52197119010fb6dd03ae9101d03db1c8f48b7212b371d00f507bffc0a13`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:8dd53004a497bfad0ccc505119653b4cb98957304ad0e09434abd4e05d759ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb565636cec41efec7fdd058360af949ea1b207261427e2a1d5201545852a94`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:31:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:36:54 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 01:36:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:36:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:36:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:36:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:36:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:36:54 GMT
CMD ["irb"]
# Wed, 20 May 2026 02:49:46 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 02:49:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 02:49:46 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 02:49:46 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 02:49:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 02:49:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 02:49:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 02:49:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 02:49:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 02:49:46 GMT
USER fluent
# Wed, 20 May 2026 02:49:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 02:49:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affe7ff5a6816636d316cab96ab4ec627f6e94e4d270f3c01c842db6eea57b6f`  
		Last Modified: Wed, 20 May 2026 01:33:59 GMT  
		Size: 1.3 MB (1294927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4902876f154cc5231cbb8f09b165c7a1d8b9724ac03ed3fca0b398366de5fa`  
		Last Modified: Wed, 20 May 2026 01:33:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310d4b6bd5ac5f0cc164b6ab59e2ae6eb73067560ccb6b6e520297cdef1a983a`  
		Last Modified: Wed, 20 May 2026 01:37:08 GMT  
		Size: 39.2 MB (39207831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd386c7dfc77967e8045d8c6a68f53eaa51530b4b2963b25db4e5046a2f6e0c`  
		Last Modified: Wed, 20 May 2026 01:37:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5322372e9b5d777948aabd3791612864ff0a519e266990e6a3c615ad7ca8421f`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 6.4 MB (6447242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0183570fe8eaac934be4d9bb87824272f14093a8281235578299a8aa534a09`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964711b1e73271d5128a6436d93cd01ec2d45e5fd97c54978edf0741024109a6`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaad4409f71b88d7c936f76fe42a9c95ef1cb34a7a9384a6d72afc6cc725283`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f5ef1068109c2e5e591362f5c238613e323d69f1d89b663a5d69ceda33a2188a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f203037d1ff5db53c4b41c69a9ac02bc565f4db06969b818a8ecbd9308d33969`

```dockerfile
```

-	Layers:
	-	`sha256:414057adf61949a138d296a9d8eedbcbfac679cfb4771026fa1f193e555e69b2`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 2.3 MB (2283267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d337cd30077e00434f231a07bee455acd6b4368b4e67760acc304e9401a7b292`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.2-debian-1.0`

```console
$ docker pull fluentd@sha256:a8afee19237b7c269e0ad943f4d7b66cf290d1aecf856fe7f6f480d5ad577b87
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
$ docker pull fluentd@sha256:00f76d25091b25cf42af10b5b8b0e184ef46c37da9654754581f727063be9856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79255022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62910f165807c3441ceadffa6ecaaa96fd0df004c645b721b1bcde139249569`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:51:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:51:21 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:34 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 19 May 2026 23:53:34 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 19 May 2026 23:53:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:34 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:34 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:34 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:34 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:34 GMT
CMD ["irb"]
# Wed, 20 May 2026 00:42:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 00:42:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 00:42:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 00:42:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 00:42:42 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 00:42:42 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 00:42:42 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 00:42:42 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 00:42:42 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 00:42:42 GMT
USER fluent
# Wed, 20 May 2026 00:42:42 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 00:42:42 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae509a998d8cc25f86fa4f526ccfd3705bd9f1cdca6b1b3e5dde600c5503c8f8`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 1.3 MB (1279968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74962092651f83b43187b825e403ac93d24a5181f9ce1560f2048cb675a93a3`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3262473bfa79eafa8c9058c39e428100724eeb68ce81266365aa60667dffafe`  
		Last Modified: Tue, 19 May 2026 23:53:43 GMT  
		Size: 42.1 MB (42127140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba9eca8660ca68e09841c5da2d4e95a207217797f889c661969cd56adadb63d`  
		Last Modified: Tue, 19 May 2026 23:53:42 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a9eb26a7e329dced11d3949926d121f7c796c796b1fc11f7b12985503d850`  
		Last Modified: Wed, 20 May 2026 00:42:53 GMT  
		Size: 6.1 MB (6065591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ae1d65594255316e8b520c558272744cf5de02d0e70e88fd27cca5472022c9`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff9be9611b0755a0d7c799c2b31f819f7441dd1bd513d3ed78f20070a5e8c04`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d30ebd71cff00e52701b7628b7438f5eb05107462f3c16c488ae63115c29ce6`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5c9e8fddecf115ca8ef240cc97838dac301ebad813f0f4bb97fb4a2df8663223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cd3d78ccc58da38f5c9784225881c8f8e808b08b3a013d1bcc82291d46b4027`

```dockerfile
```

-	Layers:
	-	`sha256:69756b18478f4cc81288a43dc2b274637ab0808892f69299c7a46ce2bc4f376b`  
		Last Modified: Wed, 20 May 2026 00:42:53 GMT  
		Size: 2.3 MB (2281822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4464ac2f2e453244abc0de5ed98d4a248c543e78699b999dd1652d669fdedf78`  
		Last Modified: Wed, 20 May 2026 00:42:52 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:3deeebb820fbfa4c392f5bf9a0698e6fe21c35187f8fd6543d4b665b3660a1d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73112123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a45a7c8d6b7dab645bfc30843eb6f32797714e337f1844a353ab4b47e23bd4c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:36:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:36:15 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:39:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 00:39:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 00:39:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:39:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:39:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:39:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:39:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:39:20 GMT
CMD ["irb"]
# Wed, 20 May 2026 01:54:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 01:54:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 01:54:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 01:54:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 01:54:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 01:54:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 01:54:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 01:54:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 01:54:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 01:54:14 GMT
USER fluent
# Wed, 20 May 2026 01:54:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 01:54:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96895aa837a127026eac95d26c75abbb54babbb5e762050dadd64de4a4cdf26b`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 1.3 MB (1263760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab57a91c1b877ddd64d9568132be395821962d3f9abd509d21b78fbb37d4ce59`  
		Last Modified: Wed, 20 May 2026 00:39:29 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b7c7a49c9a601347b5bc7885069679efc572a7d07d471b0d729f46f3f26606`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 37.9 MB (37924207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae01ed4844d48ccad3e6e0c04da1c92633f098629f45d62660416eba51d518d`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435e0feeac4798a35e86ed15b1039dcbd7564a9d1463c1d272f71afdf4b5a6c7`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 6.0 MB (5967895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a88cbf410a462245cdf6c313f99016571ca1333a989f427d18cc0d8af13d1d`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a511f40be0082bccf64ada0f042b0817dce09d595da6ea8ffac8ba4a47af61`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b4d5734bead9accdc01648bf81a931cdab381f24a53c405d69d26d7740f4e4`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4fbbf16de9fd37b8ad02ffc8ff711f6fb23db4db59ca30ef6b7a479d63be9911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac22b6680d7de4ef960a8ba1f903176de9f4d275f4307e36b4508e8e2c78785`

```dockerfile
```

-	Layers:
	-	`sha256:ffc4528a925dfb651506aa4af4d84b57e259458e081ff07bc63d3fac108efda9`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 2.3 MB (2284793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69f5031a63ffa26d07f230fc90c0cd130909dd2454f15aad4f5becee518760d4`  
		Last Modified: Wed, 20 May 2026 01:54:22 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:17b4125ec36408635ec7cfa349a5ed826017e2bf7e5c44206a2a69682ba3f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70960827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eba3e25015f42e83adbf7a505edf08f56ea185dd7d2275e1d653fc44da17273`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:12:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:12:32 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:15:11 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 01:15:11 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 01:15:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:15:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:15:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:15:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:15:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:15:11 GMT
CMD ["irb"]
# Wed, 20 May 2026 02:18:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 02:18:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 02:18:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 02:18:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 02:18:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 02:18:51 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 02:18:51 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 02:18:51 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 02:18:51 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 02:18:51 GMT
USER fluent
# Wed, 20 May 2026 02:18:51 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 02:18:51 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0e18f2eb3a8e56bd5a9ae9ab99db08dcf4799a8c083e10a4634e7b53fd7f2`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 1.2 MB (1237685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99435c1ef4eea2241c80a26de27a40623cbd18ae90074a36770ba95dd49ee2e`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4f726d4647f840eb32e17ab3eac6cd69521f1b0ea37a25100585f11ab43f2c`  
		Last Modified: Wed, 20 May 2026 01:15:20 GMT  
		Size: 37.8 MB (37781022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b418179391d555c02f2342c5b411ca11f3df309ba00f80724924c50cd1369500`  
		Last Modified: Wed, 20 May 2026 01:15:19 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015697a1eccf89e0b031fe60053f9a706b1a2b8b2f06ae62e7ce9959fbfd1e8f`  
		Last Modified: Wed, 20 May 2026 02:19:00 GMT  
		Size: 5.7 MB (5733897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bc52d940d104b1c67a9254a4647201fc4de5287bc08f7f67a7fedc3d96d161`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641b991a2723adf71945a9dca05376e4908849b4846c28b4b082949bdee94ce0`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd085d4f1bd88ed9d7df2521f8dc417ec111dd4d70c32a5cd07f33a0aa13ad1a`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b3aa02b23374c872acce7d6637246def14b74cfa03be1e25e51ab9603936b181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc08142d2f496ae5d62f9e06db6eacac4419377aecaae6e62ba38141a6ab582`

```dockerfile
```

-	Layers:
	-	`sha256:ccd7c8b017d42e010b1e7b8b4e8efb4664779c34f51ec4d43129fc5b42c63e19`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 2.3 MB (2283234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a949fdba9ae187c7a9ff9ac9d419614042df451a2343917d40cc425ffefb7692`  
		Last Modified: Wed, 20 May 2026 02:18:59 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:ce3631f5ca630ab6347a9df8f96824c814e7f49fb24e536cbfa5c302face8cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79544961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c70ed8618efb22b7953c7f3b73edc4e61129698e809006b4a660a229e1e7b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:59:06 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 00:01:38 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 00:01:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 00:01:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 00:01:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 00:01:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 00:01:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 00:01:38 GMT
CMD ["irb"]
# Wed, 20 May 2026 00:45:26 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 00:45:26 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 00:45:26 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 00:45:26 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 00:45:26 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 00:45:26 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 00:45:26 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 00:45:26 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 00:45:26 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 00:45:26 GMT
USER fluent
# Wed, 20 May 2026 00:45:26 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 00:45:26 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0598190532e5fd5fa7f406a5f319138ca25758feb0a64da1b3449f88ee3521`  
		Last Modified: Wed, 20 May 2026 00:01:47 GMT  
		Size: 1.3 MB (1262002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15451c3fcbf117446c70cfdc658a97fef17103b8aac67f9d0f6802d157bd9b46`  
		Last Modified: Wed, 20 May 2026 00:01:46 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f64a0da9b1063193969c2698804e6a46b382e111eaf1458b40462d9cfe9d2f6`  
		Last Modified: Wed, 20 May 2026 00:01:48 GMT  
		Size: 42.1 MB (42078709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b2a3b4652676c008170445be657c4eb9ad8e3438b155e354ce5530a206af77`  
		Last Modified: Wed, 20 May 2026 00:01:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c468e08f650d3fff69045c6c8375b0a6c8a16d598528d7615fd37b3b57ec048`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 6.1 MB (6059940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e6ef0caacaf679fbbbd825fa41b30bd764a7d8245761de4517c992ae005bb`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04afc7675db41ded07504e36e5275da1bbcafcb0c24b8ae92c8cecaa8e7dd842`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc75834da573e2d5e8b320011cc488ea14c4991de83d8301f3d53e1c75c7b358`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:1ab31f62a213d35770ef2044e29445ac0521d04ed3dd854d1f1378ddf3109e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24d3b20a204acc80741a498fb9d4108366013dac8043dd87c9ccbcf9f5f2692`

```dockerfile
```

-	Layers:
	-	`sha256:5c7f3e39d6f5e68a0e9b8bf80c02dab50eac63bf0943af51de24ea1d34099e4a`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 2.3 MB (2282086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0f0cc04971ca7d3fa62832f8578b0f4e5c0d3098839dda7bf0c54caa537224`  
		Last Modified: Wed, 20 May 2026 00:45:34 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:c410b212e6cdfc4092aacc1cce7dc5e1bbb7019fd56b8bc46cef136714c77934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76286643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66240acb7cefc429d068f7e294fbcc57cc4e40359a5c6e7e230bfaabd864ff76`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:50:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:50:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 19 May 2026 23:53:20 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_VERSION=3.4.9
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Tue, 19 May 2026 23:53:20 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Tue, 19 May 2026 23:53:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 19 May 2026 23:53:20 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 19 May 2026 23:53:20 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 19 May 2026 23:53:20 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:53:20 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 19 May 2026 23:53:20 GMT
CMD ["irb"]
# Wed, 20 May 2026 03:02:10 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 03:02:10 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 03:02:10 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 03:02:10 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 03:02:10 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 03:02:10 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 03:02:10 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 03:02:10 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 03:02:10 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 03:02:10 GMT
USER fluent
# Wed, 20 May 2026 03:02:10 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 03:02:10 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af0b86f8e074f8013394c8982e198a1696c4342a8a353df1261a9436c962fc9`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 1.3 MB (1287842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b478f5fd5d558d3bc5b16b7358ad81ffe9e90dd8bc53036a1e39466601cef7`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04ada0bbc123da7765a41ed03bd4930b19f6d3d5b7e7a44c1387ac2fcadd1d6`  
		Last Modified: Tue, 19 May 2026 23:53:29 GMT  
		Size: 37.7 MB (37661953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55408ceb22509be948980234f637e5a5ae7adf6e80d24588739f6d90684f6216`  
		Last Modified: Tue, 19 May 2026 23:53:28 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931a4801406d68f7b0827fd601ff8d85c52ab40f6ec0eb8c93e5a2f68fd850d0`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 6.0 MB (6039122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e24965accd62ef1ba63bcda357831f008d5a4a8e3617dddb25eaa65a024729`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2599cc634f1448c59392feca518e7674b2ddb84e80dd929c0d148c72e379ca16`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5002f177266084489472144ecab94c108374732a7e59372ba5a8b2b7246c1d59`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:cb0ae3f7faf6ea5bde3c605d94ebacdca656cc30d5a2ea84e185038d80ce97e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2300296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2322a8ffe133a3f97e021d2664428ee0363fbdd607c2d35fc5fe47861d5146d0`

```dockerfile
```

-	Layers:
	-	`sha256:4151cea6497c446e934bc121c3af58b3da29964f63ecd3edbb446fa9278fcadd`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 2.3 MB (2279010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4745c54e86bea1ab62463a9b51c5d5fb518733e07ae2e73070c9f3947738854d`  
		Last Modified: Wed, 20 May 2026 03:02:18 GMT  
		Size: 21.3 KB (21286 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:2bd708cb0638677b5220c6d97aa100b65010de3ca9c61de375812de9b67f1408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81035751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5698ff2c3b2ac57e01a62d67a3db55da973d6c6dcf598c2408460267f3b11cbd`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:19:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 05:19:45 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 05:30:44 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 05:30:44 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 05:30:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 05:30:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 05:30:44 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 05:30:44 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:30:44 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 05:30:44 GMT
CMD ["irb"]
# Wed, 20 May 2026 08:50:04 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 08:50:04 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 08:50:04 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 08:50:04 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 08:50:04 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 08:50:04 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 08:50:04 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 08:50:04 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 08:50:04 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 08:50:04 GMT
USER fluent
# Wed, 20 May 2026 08:50:04 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 08:50:04 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f690f4ce037264685118208392ba68615b070bc6f389b1e1885a1093b000b1f0`  
		Last Modified: Wed, 20 May 2026 05:23:51 GMT  
		Size: 1.3 MB (1310365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4e33c6b3845011d63383976c646a4dcd0c10a4713aba30ef20741a1896eb7f`  
		Last Modified: Wed, 20 May 2026 05:23:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe6678da6048b1e50dc773fe29b467aa363454d05597952dd57edad830c5353`  
		Last Modified: Wed, 20 May 2026 05:31:05 GMT  
		Size: 39.5 MB (39532615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5bff98a4e0df97e1384614181c51b83eebf65b689cf70c36d9a1b26734d75`  
		Last Modified: Wed, 20 May 2026 05:31:04 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb20c3317469b094fe8180f90d46e40dba015565bd05b35ce3c89be027a1668`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 6.6 MB (6589922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59651207e6bbd9adae5168f59e1bc2063370398010c50456fbf0c931ae89ce2d`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4713f74fa0ffb3c0b2142c3e03c518a022ecc9e6b4b6b3a5bb14439814f5b8e3`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbcb96a0ff2c8ac18fd477ba11a8541a44a668cc75d8ce01dcac496a1638bbc`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:014402d5443a94f2c18d0e9ff317f9fb8fbc35b46dc3192b23c3b3369239df17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567ebb2fc729ff8c19eb36b4e429500ccfb8dfba9937e61a8d68b10f55b96393`

```dockerfile
```

-	Layers:
	-	`sha256:410daf5971803e3d0c439a4e0604f8a3d8f6e9e6acdc6d3bfffbe70f3e7a7b8c`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 2.3 MB (2285357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9061b52197119010fb6dd03ae9101d03db1c8f48b7212b371d00f507bffc0a13`  
		Last Modified: Wed, 20 May 2026 08:50:20 GMT  
		Size: 21.4 KB (21378 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.2-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:8dd53004a497bfad0ccc505119653b4cb98957304ad0e09434abd4e05d759ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb565636cec41efec7fdd058360af949ea1b207261427e2a1d5201545852a94`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:31:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:31:00 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 20 May 2026 01:36:54 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_VERSION=3.4.9
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Wed, 20 May 2026 01:36:54 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Wed, 20 May 2026 01:36:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 20 May 2026 01:36:54 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 20 May 2026 01:36:54 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 20 May 2026 01:36:54 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:36:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 20 May 2026 01:36:54 GMT
CMD ["irb"]
# Wed, 20 May 2026 02:49:46 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 20 May 2026 02:49:46 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Wed, 20 May 2026 02:49:46 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 20 May 2026 02:49:46 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 20 May 2026 02:49:46 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 20 May 2026 02:49:46 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 20 May 2026 02:49:46 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 20 May 2026 02:49:46 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 20 May 2026 02:49:46 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 20 May 2026 02:49:46 GMT
USER fluent
# Wed, 20 May 2026 02:49:46 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 20 May 2026 02:49:46 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affe7ff5a6816636d316cab96ab4ec627f6e94e4d270f3c01c842db6eea57b6f`  
		Last Modified: Wed, 20 May 2026 01:33:59 GMT  
		Size: 1.3 MB (1294927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4902876f154cc5231cbb8f09b165c7a1d8b9724ac03ed3fca0b398366de5fa`  
		Last Modified: Wed, 20 May 2026 01:33:59 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310d4b6bd5ac5f0cc164b6ab59e2ae6eb73067560ccb6b6e520297cdef1a983a`  
		Last Modified: Wed, 20 May 2026 01:37:08 GMT  
		Size: 39.2 MB (39207831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd386c7dfc77967e8045d8c6a68f53eaa51530b4b2963b25db4e5046a2f6e0c`  
		Last Modified: Wed, 20 May 2026 01:37:07 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5322372e9b5d777948aabd3791612864ff0a519e266990e6a3c615ad7ca8421f`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 6.4 MB (6447242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0183570fe8eaac934be4d9bb87824272f14093a8281235578299a8aa534a09`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964711b1e73271d5128a6436d93cd01ec2d45e5fd97c54978edf0741024109a6`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfaad4409f71b88d7c936f76fe42a9c95ef1cb34a7a9384a6d72afc6cc725283`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.2-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f5ef1068109c2e5e591362f5c238613e323d69f1d89b663a5d69ceda33a2188a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f203037d1ff5db53c4b41c69a9ac02bc565f4db06969b818a8ecbd9308d33969`

```dockerfile
```

-	Layers:
	-	`sha256:414057adf61949a138d296a9d8eedbcbfac679cfb4771026fa1f193e555e69b2`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 2.3 MB (2283267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d337cd30077e00434f231a07bee455acd6b4368b4e67760acc304e9401a7b292`  
		Last Modified: Wed, 20 May 2026 02:50:00 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
