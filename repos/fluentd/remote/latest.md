## `fluentd:latest`

```console
$ docker pull fluentd@sha256:73eb7609fb22d00485b5f8f40b1c925ca8c27746cc52759557013a11b5d78174
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
$ docker pull fluentd@sha256:0bd954ecf4f913f45922ac57d7703c95228b955458e2b032097d006b81bd22e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79264893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd83f702792d704d74f33e1d0357ca5b52f2aabbbbc33c09e2734dea18a31087`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:11:07 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:13:35 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:13:35 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 01:13:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 01:13:35 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 01:13:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:13:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:13:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:13:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:13:35 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 02:41:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 02:41:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 02:41:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 02:41:52 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 02:41:52 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 02:41:52 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 02:41:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 02:41:52 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 02:41:52 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 02:41:52 GMT
USER fluent
# Thu, 11 Jun 2026 02:41:52 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 02:41:52 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec728fe7c5388bc586dcb9a3646e289e16841c311529b356a6b4b26be1f0ed9`  
		Last Modified: Thu, 11 Jun 2026 01:13:45 GMT  
		Size: 1.3 MB (1279952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e3767d48de1ba9866346d00550a4a4e82c2200d937844109d7039e10225788`  
		Last Modified: Thu, 11 Jun 2026 01:13:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481aefa75286a6aa4cbaea96391ef6bdf066ad400ba719f79227feeae4bd5fff`  
		Last Modified: Thu, 11 Jun 2026 01:13:46 GMT  
		Size: 42.1 MB (42127408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69a7b52177e01dac722dc5074b6b718c138ce718deb0fd5fab4c6526152f746`  
		Last Modified: Thu, 11 Jun 2026 01:13:45 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ff1261d0cb9765f8e2e49652ed26ffd9940559f0d92323636023abae93edc2`  
		Last Modified: Thu, 11 Jun 2026 02:42:00 GMT  
		Size: 6.1 MB (6069726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e65fd3d66f13282e42606352f2cfac303eab4ee9b90cd9b5850272db007bee1`  
		Last Modified: Thu, 11 Jun 2026 02:41:59 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f731151c688fb833a897e129b97693bf1f53a8f3b886ae83ebacef41aeef0c`  
		Last Modified: Thu, 11 Jun 2026 02:41:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0be945eb44d97915c3eb494a121ded56b7d8ee4190657a0c2ee82e3d7580154`  
		Last Modified: Thu, 11 Jun 2026 02:41:59 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:dc9ff2658e6b6de534631ec195fbe99cfa72eac69c1a90d2185d640c0a9d15c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa46f0f466498b6d2ca14b08b1f94c00f4499a8f1ed3c3a1999d96da9bec8f6`

```dockerfile
```

-	Layers:
	-	`sha256:ba9318c9813986751c08334c13bdc845c7d4b2898591810292864289043a0006`  
		Last Modified: Thu, 11 Jun 2026 02:42:00 GMT  
		Size: 2.3 MB (2281853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54d9d38d1d7feacf2f74cf00a7644c0ff29f5386c1efc2dfb077146fae621281`  
		Last Modified: Thu, 11 Jun 2026 02:41:59 GMT  
		Size: 21.3 KB (21325 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:b179a66ee4dc5aeaf0402e4671a51e28f7c89976a3cabeca5c7670c89a6b8a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73119600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb261f09174e64899f9d0e504e1f8929d41d8ed8de945334a1e69adce4ac7b5b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:01:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:01:12 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 02:07:38 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:07:38 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 02:07:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 02:07:38 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 02:07:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 02:07:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 02:07:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 02:07:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:07:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 02:07:38 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 03:05:39 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 03:05:39 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 03:05:39 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 03:05:39 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 03:05:39 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 03:05:39 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 03:05:39 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 03:05:39 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 03:05:39 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 03:05:39 GMT
USER fluent
# Thu, 11 Jun 2026 03:05:39 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 03:05:39 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e3cfccb6310683199a018dc5db96c3df1f54031f2d969548c4bee2dd27702d`  
		Last Modified: Thu, 11 Jun 2026 02:04:26 GMT  
		Size: 1.3 MB (1263762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:412792fac1cad0c217a72615d451d3c835fbb24474bc4daedebe95726ccf15ab`  
		Last Modified: Thu, 11 Jun 2026 02:04:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e54c74c7e0779c455b62afbc13dda3c4428174796d5e74ebdf169a07cd9f0c`  
		Last Modified: Thu, 11 Jun 2026 02:07:48 GMT  
		Size: 37.9 MB (37924178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb32077f316f39309642b4db366395c339629f8f6682a25d7c8f75b20ec8dc1`  
		Last Modified: Thu, 11 Jun 2026 02:07:47 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852acd821c3680db9d969c1bfb3536a1a26460a96bb50f0e2eac126f97ab1396`  
		Last Modified: Thu, 11 Jun 2026 03:05:47 GMT  
		Size: 6.0 MB (5970073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd17f978d12dc3a6dc6f3cf633e9a91bae5d54a516c4d0530deb2a4cb88e5d3c`  
		Last Modified: Thu, 11 Jun 2026 03:05:47 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1d11ea98cc74975cda0e78e1bb348bd6c03c8d036115953bcdc93825d18e20`  
		Last Modified: Thu, 11 Jun 2026 03:05:47 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff12561929cf2923916f449270b852db34a84aaaa0159774e615c3b42a8603d8`  
		Last Modified: Thu, 11 Jun 2026 03:05:47 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:1369f096a26a20abd94e7870e3fbcdd97e0465590890a382500c545f490585bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3213775a5a89a4ce3c71758378e8b8902aa1f87084405bcb17e9d3160fbadc96`

```dockerfile
```

-	Layers:
	-	`sha256:8ea4d4d2ab9c5cb4e68f656fc50df3de9627febabf68aece212784917440ae45`  
		Last Modified: Thu, 11 Jun 2026 03:05:47 GMT  
		Size: 2.3 MB (2284824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4612e80d85283875f25406043e399ceb96cce37b401be055a7690c17d60b3eef`  
		Last Modified: Thu, 11 Jun 2026 03:05:47 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:88a4689e69d8fa250767e665835206fd8979278ddf715109953f3d76883228ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70968409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8853b69d18b475625354ed0dee5f442a2601cacf7171a0f297b0e973fdc9e683`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:35:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:35:52 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 02:38:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:38:37 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 02:38:37 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 02:38:37 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 02:38:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 02:38:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 02:38:37 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 02:38:37 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:38:37 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 02:38:37 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 03:24:28 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 03:24:28 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 03:24:28 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 03:24:28 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 03:24:28 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 03:24:29 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 03:24:29 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 03:24:29 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 03:24:29 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 03:24:29 GMT
USER fluent
# Thu, 11 Jun 2026 03:24:29 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 03:24:29 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7045ba38aaa974d7ba574b1801f2b1517e72f10e3a413efdde5c1a9c3dd36e`  
		Last Modified: Thu, 11 Jun 2026 02:38:46 GMT  
		Size: 1.2 MB (1237620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c691db1f2bcc7484f4db9de9ecb9f43e4cba43b4bd385132308d3f4d9c89cd`  
		Last Modified: Thu, 11 Jun 2026 02:38:46 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ef16d9bcb29faaf3909e9dc0954b7a0befebb8b4662b8b94b492ce1a79983c8`  
		Last Modified: Thu, 11 Jun 2026 02:38:47 GMT  
		Size: 37.8 MB (37781499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f703ee4a6f3a1577d773c87ad72573268321bcb6fe239054973ebdd6773cab`  
		Last Modified: Thu, 11 Jun 2026 02:38:46 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb34cba7aae51643828af2bcb9e99c585e057805a9bab089c9ded57ff0249f5d`  
		Last Modified: Thu, 11 Jun 2026 03:24:36 GMT  
		Size: 5.7 MB (5735894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209beb520691249199a9772f93e1898a32b9950d9372a07b8112d3c7a4d20224`  
		Last Modified: Thu, 11 Jun 2026 03:24:36 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d272cbc5286e0d6f5b80f99b04f79af06e8823454c1e5674f617a5845aa1c4df`  
		Last Modified: Thu, 11 Jun 2026 03:24:37 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6eee6b63e4ae0dfbdf54e722251b1409f15a68930eebd379e5cdd8572cddec`  
		Last Modified: Thu, 11 Jun 2026 03:24:36 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:46ee6551d2ba4a47ead1f90c4b86218d7f1dc14bcfc81c4f22cb03ba70cf72ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821f2f421a6c537eef686d56cae6307ce6a763558fb5a3b7917576e0de6b2700`

```dockerfile
```

-	Layers:
	-	`sha256:951bb877e4fab879f03e0de48b2b54b456a84ae090a3e5195b7149596e4c1da9`  
		Last Modified: Thu, 11 Jun 2026 03:24:36 GMT  
		Size: 2.3 MB (2283265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4fbace4aff0b0196427ce90483cc4a865a7991966c7b9a0209154f03acdfbb`  
		Last Modified: Thu, 11 Jun 2026 03:24:36 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:58272ee2b5b38fd676b31cfc8d6f80bc8e6c5da0c3b9296501f43cadf5101bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79555212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb547e75521875ea2bd7bf7f06177d004b62a99ebe496ad924af63c8a386b210`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:16:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:16:03 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 11 Jun 2026 01:18:35 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:18:35 GMT
ENV RUBY_VERSION=3.4.9
# Thu, 11 Jun 2026 01:18:35 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.9.tar.xz
# Thu, 11 Jun 2026 01:18:35 GMT
ENV RUBY_DOWNLOAD_SHA256=4231c54072601a171faed1699f105985e9971c94cd382b78feb4eb44eec2dd1a
# Thu, 11 Jun 2026 01:18:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 11 Jun 2026 01:18:35 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 11 Jun 2026 01:18:35 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 11 Jun 2026 01:18:35 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:35 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 11 Jun 2026 01:18:35 GMT
CMD ["irb"]
# Thu, 11 Jun 2026 02:42:50 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 11 Jun 2026 02:42:50 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.2
# Thu, 11 Jun 2026 02:42:50 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.2  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 11 Jun 2026 02:42:50 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 11 Jun 2026 02:42:50 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 11 Jun 2026 02:42:50 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 11 Jun 2026 02:42:50 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 11 Jun 2026 02:42:50 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 11 Jun 2026 02:42:50 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 11 Jun 2026 02:42:50 GMT
USER fluent
# Thu, 11 Jun 2026 02:42:50 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 11 Jun 2026 02:42:50 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e98699ce0114d65cbc3c73ede5f62287cfbd9866205e8ce8be51adf89e74add`  
		Last Modified: Thu, 11 Jun 2026 01:18:44 GMT  
		Size: 1.3 MB (1261957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdd6ecd8606638bbcbe93663caf1af54258fc41d7ccb9a731d700cc130dd402`  
		Last Modified: Thu, 11 Jun 2026 01:18:43 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c06de89f3cd4fcc042ed04fa9705995ad5f75ab502621a3190b72c086fd3306`  
		Last Modified: Thu, 11 Jun 2026 01:18:45 GMT  
		Size: 42.1 MB (42079153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1ead663c512810ee369f05cc9f522f948aeb54161471d3dd195a8b4349d4ef`  
		Last Modified: Thu, 11 Jun 2026 01:18:44 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac05611a8cae5cb8d4beb1589afb0baff46b03bf78848fbc49703628c70afbd2`  
		Last Modified: Thu, 11 Jun 2026 02:42:58 GMT  
		Size: 6.1 MB (6063184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8c6407a2c91cf1af638cddf636b440a556fe8bc61e99a2398f9b87e8c4a1b9`  
		Last Modified: Thu, 11 Jun 2026 02:42:58 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69a7a8d2a1c24e7f8f39c37130935f8a97272014bd1cc7e219236dac7ead7a1`  
		Last Modified: Thu, 11 Jun 2026 02:42:58 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4726cea7500430db37b3ae4f80bdc42536794f9edae9ada46cfd17e2c2c5b`  
		Last Modified: Thu, 11 Jun 2026 02:42:58 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:399b5178eff965a20c48b93b5cd5e9a756b7a1286c229308a8be6cb7c6ee969a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1079b3bbea8e43c57a55340896bd1f0bf479ab94e8dafed32d7f762579a340f6`

```dockerfile
```

-	Layers:
	-	`sha256:474efab0152521eee39332f399d3677a1b3ddea1e0e985cf983e135e7a5a4e2e`  
		Last Modified: Thu, 11 Jun 2026 02:42:58 GMT  
		Size: 2.3 MB (2282117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e97578581fa054413b0a43fbe0f8fb17849e880efdb31a1b342c446568b154ff`  
		Last Modified: Thu, 11 Jun 2026 02:42:58 GMT  
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
