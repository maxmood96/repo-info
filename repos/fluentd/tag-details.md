<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fluentd`

-	[`fluentd:latest`](#fluentdlatest)
-	[`fluentd:v1.16-1`](#fluentdv116-1)
-	[`fluentd:v1.16-debian-1`](#fluentdv116-debian-1)
-	[`fluentd:v1.16.9-1.0`](#fluentdv1169-10)
-	[`fluentd:v1.16.9-debian-1.0`](#fluentdv1169-debian-10)
-	[`fluentd:v1.19-1`](#fluentdv119-1)
-	[`fluentd:v1.19-debian-1`](#fluentdv119-debian-1)
-	[`fluentd:v1.19.0-1.0`](#fluentdv1190-10)
-	[`fluentd:v1.19.0-debian-1.0`](#fluentdv1190-debian-10)

## `fluentd:latest`

```console
$ docker pull fluentd@sha256:9fbb4456191a5284d9d2084feb43915c2240e486a3bbdc4872af6013bb321515
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
$ docker pull fluentd@sha256:968450201f1633b5a796a19818797ba95ada90226e3e78d266de7cc447d702de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79258793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec6b9a837666fac5eef40dadfc3140928de04730d4dc0a2d94cb9d914d4a05f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac80cde22bfc7f1283ae07a881aea9b0ddb32e3c1bd62b6dd738c001461ae80c`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 1.3 MB (1279282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04bd217259e9a1adff42a11c482bc4ce95944a28541de67525db69fd74eb2a`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a793530ea8ee5034845d68f5cf20d39e0d069c36c9df258a0617f3a32fd4252`  
		Last Modified: Tue, 30 Sep 2025 00:46:10 GMT  
		Size: 42.2 MB (42153497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7503b4256904558e2f15b3cccab853eec67b0a9eb298954e71634e22152985c`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7718db5a4f479bb9efa051123d43769274727b3f793a5384e9b524fe083ab476`  
		Last Modified: Tue, 30 Sep 2025 03:38:08 GMT  
		Size: 6.0 MB (6045860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633fe0eec3f87f1fb588b5ca394da08edb16783f4f76ad896f53e96db77046d9`  
		Last Modified: Tue, 30 Sep 2025 03:38:07 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d605c050bdbc2cbe5986aacfb9b2cb699deefb8e96328a30c5955c8c203558`  
		Last Modified: Tue, 30 Sep 2025 03:38:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbe1a71e963aeda880faa4a8ee1c92f02aaa0f25c2c541d229938263151ae1`  
		Last Modified: Tue, 30 Sep 2025 03:38:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:5ab3b23006abd0a4505879bb744524f291c5fd3c47bcda59fe9580e6a52c9451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32239db467b7ac791c5e02a30b39a8e07d1676da3f72023c7a4e7a6e3b6dfdc1`

```dockerfile
```

-	Layers:
	-	`sha256:3c38f4673cb000c49365f7ac225ee6c8d1192d70f464591a2fe210e47b5e129d`  
		Last Modified: Wed, 01 Oct 2025 14:28:19 GMT  
		Size: 2.3 MB (2283480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63450ee822c0556494352d4e2d8a7f3d1aa722f4118a228a8de1dcc441a2d9d`  
		Last Modified: Wed, 01 Oct 2025 14:28:20 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:c0606950b9ddd0b3471e91868591e747d6794e0bf3559f55eba6ebf8ff0c562c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73145576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ab1bbad22e39a2ebc11e610006d2d8ec952c1a9f717f04ed3043c6c8ab584c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd187b5427463256098e233be4d4d03fccba4301a10c8bf73c1b1d07bfbc4305`  
		Last Modified: Tue, 30 Sep 2025 02:27:33 GMT  
		Size: 1.3 MB (1262736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba5754fd04e92aafff5cb6ad7abbb1e1defb4260642169bfbfe164ea4632f4b`  
		Last Modified: Tue, 30 Sep 2025 02:27:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77907aaee8949d54a9d51a6df6d5279b339b37d5e22e0c2146e66e347a21536e`  
		Last Modified: Tue, 30 Sep 2025 01:43:13 GMT  
		Size: 38.0 MB (37990588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec771643eef709f72f374b7d0f416502bb63707d40902ec5ccf83f1d49e6276`  
		Last Modified: Tue, 30 Sep 2025 01:43:05 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaaaef0ea7bb3e3e8bd4610b7207cdfe2b89b7b2f9c0f43a014f8718d67d119`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 5.9 MB (5943720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5f21615138e8a6acbd04d6781d94fc1eb303b8dd95cc6cba825a94f34991e3`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5798e98fbdd0d04752f2cef760bafad88e01c002715aa66cd861aab5d51ca13`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b2b12cd1a6435c07db2ac16401aee26e54c3330ecf16e3c055448ff8a6404b`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:c672b12deba689f1e313e24f8a284dc66eaffc97ab4a123901c87093c0f5f4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51235185b4bdc6bef6882a9b4db6f1b13ee1a239a15f817650b50cf2293fbf1`

```dockerfile
```

-	Layers:
	-	`sha256:48baca2e35bba316ac819ece9f88c363ec614e2a505a3ce38c95ef61bb768bad`  
		Last Modified: Tue, 30 Sep 2025 08:28:23 GMT  
		Size: 2.3 MB (2286451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a91c6bbf6731857abf09cffadbdc793585e066ea0e4ab2c605a118b48e1321`  
		Last Modified: Tue, 30 Sep 2025 08:28:23 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:fa5372efcc150d37b61d58d2fb4bc57e68336a0586673fb610000ac8fb894fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70999027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74be42a49de9e5de3bd1b91557e610d4c7ebf00984423c61309fd561c71a51b3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96565be4d07605304ab01ed88ddb2422c09d2c097a7a6bd9e908ecc538bc41b6`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 1.2 MB (1235933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89241ff1b55720625ba104e27a7ae55ed5d7f05f7cc70232c509ad4e8c98a25a`  
		Last Modified: Tue, 16 Sep 2025 17:54:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cfac0646ebc1380322334d36097689728babfc80127206b89b48da79bb9f1`  
		Last Modified: Tue, 16 Sep 2025 17:54:49 GMT  
		Size: 37.9 MB (37857621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2c1c0258f47c00e65e5e3ad5da5d3b1bcb59afa40ef39f4100c885d6657d9`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b56a2fffda99f1ab0d575d5e52c6b0f4c7b50264d9db5ee78ebcd53c86e30b`  
		Last Modified: Tue, 16 Sep 2025 17:58:46 GMT  
		Size: 5.7 MB (5695227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bc3ef11a838c2709f52197e9236fa80e8653bd776830a799d0b5b07d54113f`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a02e348d7bd7bdb8e5edfb92e9813de0ab15af3401b02704182796aa1fc3c3`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77df38f7b9cb8eb82b9ec2076c7a77d698dc0be9e5a99f3ef45ab20f6bd25630`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:8be90cff277f6e5259cb7dc07f78955407f6d16f7658d6d0f83c1222d2f26d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcaf75209bfa607e999300d674408dc1dddbd65addd06fe5cc43d1fe5bdff25`

```dockerfile
```

-	Layers:
	-	`sha256:5f6177053b838bc7b86b6c6f85b538ac8b390fa3ae1a2d945d7bbe551076dd61`  
		Last Modified: Tue, 16 Sep 2025 20:28:54 GMT  
		Size: 2.3 MB (2284892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53f76e5d6663876d3dcc1224bf2aeb3421fe3911d5cb12e04419ecaf3532b4e`  
		Last Modified: Tue, 16 Sep 2025 20:28:55 GMT  
		Size: 21.2 KB (21245 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:d2817f38ffa33d4de35a4b3797fc7db1eb930922ad165ea94ea514e07e6f855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79570070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b3937a22385f9d20cc74516f05ecebf7d5bc9f435f9112f55b9f6efeff9e23`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb29f9c6264e41391878cf99a87793deb9e28ca3db17c0bb34690c11297d7b5e`  
		Last Modified: Tue, 30 Sep 2025 00:47:23 GMT  
		Size: 1.3 MB (1260907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d195b9d4d6d03f5400fd32517a8bd8799024004cf083065521ce652d94c0d2b`  
		Last Modified: Tue, 30 Sep 2025 00:47:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f98c4e0b0b55d73bd847713bf4ee4962af2c7ffd0f980b4517f7ea00b7813a`  
		Last Modified: Tue, 30 Sep 2025 00:47:28 GMT  
		Size: 42.1 MB (42134245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2afd66200af4a0447310eb0c3f727edde8bc32240cf3343696ff2be5a577ad`  
		Last Modified: Tue, 30 Sep 2025 00:47:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a76ee738741e03869e456b0d29876ce0849f753da0c0375f6ce0b4b4cc46f0`  
		Last Modified: Tue, 30 Sep 2025 01:27:10 GMT  
		Size: 6.0 MB (6031686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0c6fa04b416ec7a8061ee5c017353b32ef8bace667d7d6aa062cd922dc5586`  
		Last Modified: Tue, 30 Sep 2025 01:27:10 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d6b5bab627da920964e3d12dd14eec3a2be4d11f72d4c500adb251443e35a2`  
		Last Modified: Tue, 30 Sep 2025 01:27:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b370b91e4389e4eac093d062fa8b43eef2d70af8311005e9b550556724dd6616`  
		Last Modified: Tue, 30 Sep 2025 01:27:11 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:42241076c4d8096f711808879d86e2c81c16de8af703c1e31708970ed4396eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3413fbfd0cf5a9ca3c27ceb81851854346a5523a7d1c3667eb561b1413d2d4d6`

```dockerfile
```

-	Layers:
	-	`sha256:889914816a72d49ec22c8ab729b9ee3cfc0c516d0d82ae1655738753152445d1`  
		Last Modified: Wed, 01 Oct 2025 11:35:05 GMT  
		Size: 2.3 MB (2283752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353fc631c01d1267fcf942cba3cd764d7f92535bebc5695105f881e9e0816b60`  
		Last Modified: Wed, 01 Oct 2025 11:35:05 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:5984bbd15c74879813e47b29f8446816454bc045e9f4044949d3868d80bb3aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76346556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb6144e08c32976421d484fc7e6afca57fc07a3fe6b3a7232d29b861868e92`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaebce22a6b2d6988a9332f9c7dc065d9e9f2a7a17e5c301d44f1fe019e9fc2`  
		Last Modified: Tue, 30 Sep 2025 00:45:29 GMT  
		Size: 1.3 MB (1286763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89469d8cb4eed711406676beb42abf83e21c53012c072fbaea75441a2f2a588`  
		Last Modified: Tue, 30 Sep 2025 00:45:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95001c5ad378e24b3da2da7276f7c559b8e94b7584eee54f3056825272023f6c`  
		Last Modified: Tue, 30 Sep 2025 00:45:32 GMT  
		Size: 37.7 MB (37742278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5746ce7240c97031bcab6d9c8dd307f00674605d79719f23ec9df231536ee0b`  
		Last Modified: Tue, 30 Sep 2025 00:45:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ce738fbe72cc62c38a36f7f8b6acfbb30990f17b7292a05225314e1d03befd`  
		Last Modified: Tue, 30 Sep 2025 01:26:07 GMT  
		Size: 6.0 MB (6020590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c7a12c38109dc888fe65b3be1e78ebfe10c75897e7e88a29a53f85c36eb1ac`  
		Last Modified: Tue, 30 Sep 2025 01:26:05 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782fd6568dcd50ab3250ba1420b126be663a698f9de571f283bbc43e98dcb80`  
		Last Modified: Tue, 30 Sep 2025 01:26:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8567c38864ddbfc250029b491f09c707abdae73f7b4ec08c1324c508eebf74ae`  
		Last Modified: Tue, 30 Sep 2025 01:26:06 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:fc73784634a0acce9f2232ffb9664bceb5962ffb158c3be7ad1dac17ab5b2073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd5606f84296eed8a6c30857eaa41ac7ebde5e9be715e562a6dede74c37f97b`

```dockerfile
```

-	Layers:
	-	`sha256:1aea84ac7962075608659f62303460c2d7c5fe97a9f63d87e188e19e1d29c731`  
		Last Modified: Wed, 01 Oct 2025 17:28:31 GMT  
		Size: 2.3 MB (2280668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590f9c6fec5755fe9a8da617ed8b62f9963ae37b75b6639c2cc5f04ada96c2d4`  
		Last Modified: Wed, 01 Oct 2025 17:28:32 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8b7c977482113b7d4c3379dbab8ea8bfed0e95e8088d98dd30cfb2aac2c9f2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81053367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4f08759596e3b9e5d7290dfbdfc8e075247f58227efbc547a1dc5030408742`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba702f0f51333fc2712ffc50d66684ef842dd2f30e7e612a7085b6264c7d0c0`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 1.3 MB (1309688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b9bcf1c68a9433fa734e7f77d0062d7271f532391ae56abbef8e2820cf828`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eeb6308e90b8bb2e276d4c0017af677089a878c4fc04021ec60abaf88b633b`  
		Last Modified: Tue, 16 Sep 2025 17:27:49 GMT  
		Size: 39.6 MB (39595821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa59464570e58df18efecb42c30257cdea420248e5b8999bbed0be72c06831`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6774045721abcc7f4299c08bc8dbeda3cb9f3fa72fec4b4eb19dd591a04d6813`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 6.6 MB (6551103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd934fc95d3b2adb5857e2f00983abe8c01018c4e84546953a5f77482d66992`  
		Last Modified: Tue, 16 Sep 2025 18:01:56 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc71cd1ca099ac43138c3be1a95632e82bc0144a52934fe849f86ad270b5a7a`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7fe823656da82cfb8ab46a01f99d1a4ca0687f122ae82a8d4e452e1b20fd9e`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:6c93025c0827bfd0d7b4e45dc24e2651898def62a33ed54347f89a5015af19d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03e92a175b411b28ac4407b23a620cb846b039a7656d72f9760a97da6dded42`

```dockerfile
```

-	Layers:
	-	`sha256:bd8a127995092ba84037010e07bf054f2fb51ccfb7c31d1b317e5e2aa323b274`  
		Last Modified: Tue, 16 Sep 2025 20:29:08 GMT  
		Size: 2.3 MB (2287015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99646e9dec58fd128ee6ae948247dfd018b470f6c449c9e956b352abbbab360c`  
		Last Modified: Tue, 16 Sep 2025 20:29:09 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:e1077d51cf425d916d172165c7e0adc158afdbfbcf5742ff7817babd8fec5cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76824627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323347be19501d30e21197bb58f1458e9a1aa28044755a9d28be61e0b8170168`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70370253f1ce091fe730c380a58bcad6c984318332f9815450f5cfaa70aa87f5`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 1.3 MB (1294292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ec12509a32b107309b0e8ad0dd5f247db0a2ca036489efbfcf07069855b56d`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95e9b1c0885cb28c05fa772e1873d7827da80a057035afb16216bb0e18774ea`  
		Last Modified: Tue, 16 Sep 2025 17:17:57 GMT  
		Size: 39.3 MB (39286986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160aaf92b9681375fe7aaa71ed89f2fa889c9ed589628572f762bc3bde9e15e7`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b20eb585bc1db6ed5ff9536e3f8f84a65a0a753ea5af95fde9d1cfffcea90e`  
		Last Modified: Tue, 16 Sep 2025 17:58:10 GMT  
		Size: 6.4 MB (6408044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a23e9fdec9bdc5545d5ce9e7c776cec3f3a8967d96ef8a15039b8e0c62b5089`  
		Last Modified: Tue, 16 Sep 2025 17:58:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05227e73144ce28d40dbc8ec6e46e37a0d636968a8968df0a54a6dec3c8a31fb`  
		Last Modified: Tue, 16 Sep 2025 17:58:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4096477949e4f1d7d4a4c2fdf49030b44fe4be6c2ca84f6d7300527798af25e`  
		Last Modified: Tue, 16 Sep 2025 17:58:10 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:7c98b5fe01dcee58e79906a8cda5ef48240d894adb6159e6890490f3548600d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd6db0e98cfcc6e85267280437a4963dbbc4a2e705f4b755a2baffcdc822b4a`

```dockerfile
```

-	Layers:
	-	`sha256:782a11d83d8a50fd862f7758dbb73b14c5932683d824bf14cd3b5844d177193d`  
		Last Modified: Tue, 16 Sep 2025 20:29:14 GMT  
		Size: 2.3 MB (2284925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796f5926fb2ed48c47aa5a5bd6ed0e0b3e417aadf0957f8e59270058399d4f92`  
		Last Modified: Tue, 16 Sep 2025 20:29:15 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-1`

```console
$ docker pull fluentd@sha256:9de84688a450e7f7140255bfb42faa98919c6a5b74b7844f5c0e2ef6b08a4d98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16-1` - linux; amd64

```console
$ docker pull fluentd@sha256:62b59793f4b04db4c6c55dc596c9b0f6f2f609ba3a5ca8a07a172ce4c4c94c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17364715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecdf9365b5088dc631ac62d36f5d484ca8b41403d0b0a72f4b722067edfda52`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-x86_64.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1747dece94917ce1b0256ecd60138ce4deaea1bd35dcb6b2e8afe697dd2f5b71`  
		Last Modified: Tue, 15 Jul 2025 18:59:51 GMT  
		Size: 3.4 MB (3415528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb31392c80bf139027b4fd99580f002640be382bc230598d0941fbc23840ef33`  
		Last Modified: Tue, 15 Jul 2025 19:30:51 GMT  
		Size: 13.9 MB (13947023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c2ab18679e720bc1b529d183c9e15a48bf8c51a44a96a5c88b1d30b63a2c5`  
		Last Modified: Tue, 15 Jul 2025 19:30:50 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ea010677b96e4da2f5996a87356528d7b83e6d8e7415e71b1a3fa88881560a`  
		Last Modified: Tue, 15 Jul 2025 19:30:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1c21fa85330ecf72a0795c2b88bf00f53608df1e52650afa9afe49db36bb50`  
		Last Modified: Tue, 15 Jul 2025 19:30:50 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:15f98fe183630cf6012aee43db490b5b7882c6fdcf38f22d2f8e2b95e3855079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.5 KB (983521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6ad4fbad3aad763dda59b0b642589920d6a1e88ea88f6b8aaf325e84b16899`

```dockerfile
```

-	Layers:
	-	`sha256:ac17ac913e35c4ba176d2d64ee52cdde0734638a314f5b8d613c95d9bc6741f0`  
		Last Modified: Tue, 15 Jul 2025 23:28:24 GMT  
		Size: 969.8 KB (969844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14dd3de9a6f820396ef937efd2c044817d9e6abd24d0eed9fbfc6b24c1875d1b`  
		Last Modified: Tue, 15 Jul 2025 23:28:25 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:351b12279af00d88a2f18a5cb8e919827c85d763c18ff31f79a381234941b0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16109845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf130dec1abbd0aa653924329e6c59a00675fea2f4c6e75df38ecdecedd5ffa`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-armhf.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0e31a7d1c448a18b75fd3ddf2a65dd820ec700316bcfa8710102fe2f00bf666d`  
		Last Modified: Tue, 15 Jul 2025 18:59:54 GMT  
		Size: 3.2 MB (3171284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4343a8d06e457dbc08b054339bb7f7be3c9c2c5757fc87ea56cf9dabdcc5d6`  
		Last Modified: Wed, 16 Jul 2025 03:31:09 GMT  
		Size: 12.9 MB (12936392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faa7724a34ca0aef3b0ace8626793bc73b0e9d6e07fc5b0802a13ba6147944a`  
		Last Modified: Wed, 16 Jul 2025 03:31:06 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184956266683be8c9f84a71faf719699d2f454733113a25ca9827fc3939d9c93`  
		Last Modified: Wed, 16 Jul 2025 03:31:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a932b6fa02679e51e14d11c560c02504b0d8c2a550bce03802de73690911242`  
		Last Modified: Wed, 16 Jul 2025 03:31:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:80cf01eb1c833e1bff5b8bdc8d9f290e69d4f6a97331a2bf5de3f4ea8bd19f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26c4cc20d3ce8522ca396d0c91859a7e01ecb4062649250087f770a95de0e33`

```dockerfile
```

-	Layers:
	-	`sha256:8c2a9a72c22295d5920c01a388d4107c49e60ae3cad8ce845b3161011e672e14`  
		Last Modified: Wed, 16 Jul 2025 05:28:30 GMT  
		Size: 13.5 KB (13534 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a26fafeea7e9dafc17c25197f75a0753de807961ffeb537a47cbf987c24762b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17346810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5f99a4238a53d779bb2e08e2dc478d6a2b34eb23b7c3c65a11546185b7036f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-aarch64.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:07e9a47f0c334cceba1b05e86ef0150c84564a9b9e9d4ae9dc9a5ebc85ef2b7c`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.4 MB (3353103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac6f34639e69d841f4495144c2925c0369698cb3a2cae79a9842c514901f627`  
		Last Modified: Wed, 16 Jul 2025 05:51:44 GMT  
		Size: 14.0 MB (13991540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a5dddf287fe6eebc80c2255f53f18794044f9da69e7623acead7b274569e71`  
		Last Modified: Wed, 16 Jul 2025 05:51:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ae2844be3a10be052663f438d979ba2f03ac6c89a841fe6c44d5bc43f9ef2`  
		Last Modified: Wed, 16 Jul 2025 05:51:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fd133ef2a740f7af3d063cfc0a9b2b09f56acc15218bb892a61b87f61d5009`  
		Last Modified: Wed, 16 Jul 2025 05:51:43 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:de4a4d3ee8b708e1ade04f7655238c9c98e3c302de6454df62cb7418c872231c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.7 KB (983744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6249690a5c15f0ddc47117703b20625dbd6b6766374531c80e1aa1011bd27151`

```dockerfile
```

-	Layers:
	-	`sha256:f63e498bb20dbf58b4a2452acd41ec4ccc42f816041d6c2866d3af691bdd9c61`  
		Last Modified: Wed, 16 Jul 2025 08:28:29 GMT  
		Size: 970.0 KB (969974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c92fef769075859e78e86eab6f06f019775338f1f17070f36b199227a263e8`  
		Last Modified: Wed, 16 Jul 2025 08:28:29 GMT  
		Size: 13.8 KB (13770 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; 386

```console
$ docker pull fluentd@sha256:9aece902e3a3c67c1c8f07a5af1580b708e81ecd7cc648650c939c91611d40f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16322333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cae686b1630babd15276674ab92d0a68b364bc88da5b6b541e25e921e95849`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-x86.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8505dab4c7114bf55a3da6a1e965a64c37604a0946b636bbc8606ab749093ccd`  
		Last Modified: Tue, 15 Jul 2025 19:05:03 GMT  
		Size: 3.3 MB (3250248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60783d300fa1186dce9b5c3eb11e36eeb62b943e964e71d994a199dd844061e`  
		Last Modified: Tue, 15 Jul 2025 19:25:25 GMT  
		Size: 13.1 MB (13069919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f44371e03cbf1bf428865c36018c43fdf75eb65bfc7ba651f46a84b7ce3ecb8`  
		Last Modified: Tue, 15 Jul 2025 19:25:25 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a6c9357c06ddb35d0559e0665e7d6dd592fb6505c0753f3cc1c5e5c9118ac5`  
		Last Modified: Tue, 15 Jul 2025 19:25:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93df47fb815f854253728dec79fa657e087eba34447ba0de9f51ff9591efda68`  
		Last Modified: Tue, 15 Jul 2025 19:25:25 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:a52d394b2d621b060b1d8308be8374fc09ae3b3821b249f0866cf065202e92c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.2 KB (980248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089a9b49170e879d8c95c2b64e66fc1a84a6f2a03ccba3c448ee09106e4bd231`

```dockerfile
```

-	Layers:
	-	`sha256:03414bf4b8575ff108fcbefa4c874acec592dcb6896c72866f14b88d848539e1`  
		Last Modified: Tue, 15 Jul 2025 20:28:41 GMT  
		Size: 966.6 KB (966595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1d28ac62dba6185ab4068ca0528498a5952903219b1bd4e33e785fb756033a`  
		Last Modified: Tue, 15 Jul 2025 20:28:42 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:4aeaebfa64236f2d8db0d5a40275bf6deb6f2dcec066527b64a1c21f37bd7c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16913295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a51f8c1e76a03a08b2a69fa65ba4a480734665505f15f26e9bb86646f4e9cf`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-ppc64le.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fad02e700aec982dd556a4276525680657ee6d1abbd1dd39a3e5709a60a75613`  
		Last Modified: Tue, 15 Jul 2025 19:01:18 GMT  
		Size: 3.4 MB (3362956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5d57847cb10b83ca39cc4849fdda1e8edf05460e6a52c83dc598ec2e945a2f`  
		Last Modified: Wed, 16 Jul 2025 01:17:41 GMT  
		Size: 13.5 MB (13548173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1127c667ffbc25946037843047f5ab11e8ca6a37dde4395320a26ae06d333d`  
		Last Modified: Wed, 16 Jul 2025 01:17:40 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4327b6146ba57f1fd1978f3014c06eb3fb8a5db0e24a14b10d7c74248b7952aa`  
		Last Modified: Wed, 16 Jul 2025 01:17:39 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cdb95f433df582af09b964a55b09ea777b751e7ef074155ee6d5979fa4e313`  
		Last Modified: Wed, 16 Jul 2025 01:17:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fa617bfb00ff80c808e63b3f9ac0f249a10b0870b4db6e3fedcc95d21ef95a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.1 KB (979078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677c3e30f08c6b32a44bf0e3eb3c25daa3dcc57878b6dbe7e9c6fd7a4f088eea`

```dockerfile
```

-	Layers:
	-	`sha256:dee0d912acf98283f9dd49f6106e0be3d1d551344dfc546eeeb0be4643fd801d`  
		Last Modified: Wed, 16 Jul 2025 02:28:33 GMT  
		Size: 965.4 KB (965367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e392f84bf352484fc6ba2d9ea94e671159f3593a26e10fe29b7fe699a8ddff3`  
		Last Modified: Wed, 16 Jul 2025 02:28:33 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-1` - linux; s390x

```console
$ docker pull fluentd@sha256:0230735e64f8c499a8822fd5921c882a6d21fc8065a6872e143e8d07db3d1888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16747299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b213617173eda7f4321012a955d2c166af985ca61f04deb7a99e1eb25fa1de4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-s390x.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:163224d0518e3abf0736ac8d226fdeefbf22e84c44de3b1a3b6c7c2beebd0942`  
		Last Modified: Tue, 15 Jul 2025 19:01:22 GMT  
		Size: 3.2 MB (3249001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd9c37afb374edc1a68dba4f5da69615429c45b07f7ccef55fd5ec9ad6c36c2`  
		Last Modified: Wed, 16 Jul 2025 04:57:53 GMT  
		Size: 13.5 MB (13496133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b895a58cefb82f036ccd42bfd305c06b6a42bdabe8ae47e6e8c1aa075b462f4d`  
		Last Modified: Wed, 16 Jul 2025 04:57:53 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e41aa6a1308c1b1acb531c12a5067a0903ddccca60e4ace040c07f6b261ec4`  
		Last Modified: Wed, 16 Jul 2025 04:57:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c7a0b685e1f3ae0425103b1f625d0be50d953f19bf5c28512420ed3c1d8ca9`  
		Last Modified: Wed, 16 Jul 2025 04:57:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0f6f12ef7be26befc1cc3823d3ebe0ece9f58d77d481ea4fc1a595f7b99a8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.4 KB (978434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f638219539f7263020b8ee67a597818fa1d5033e40d39cbb7b54898b57f7263`

```dockerfile
```

-	Layers:
	-	`sha256:1cd5461e768d2c51326c4d2783ebc6d4a9d026e60b9928132e3d24fcc1dda87b`  
		Last Modified: Wed, 16 Jul 2025 05:28:40 GMT  
		Size: 964.8 KB (964757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51c00df0ed05c9bb25a85a3331581d44e97dec65ef657ed0ce3339d002b7b79`  
		Last Modified: Wed, 16 Jul 2025 05:28:41 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:3d2550fa1be917e7dfcb301d6693d1aa6792dadb8a6938c8ae2d752610a3675b
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
$ docker pull fluentd@sha256:6ee4f4acacefb378f770c647c56eea2e4354596106132940d6e3795148ed8640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81975748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4792a4b2f463ace4bb6fde0596054efbe7569e8d48ed304c91ccf33618cb8c7d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd5cf0535143f813c81dc40977600297fc84dac6ad168c2f2760428b130f32b`  
		Last Modified: Tue, 30 Sep 2025 00:47:25 GMT  
		Size: 3.5 MB (3509642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0588fc42e3de39c565a8e08f901e22ada10040e44c8c294c00261755ae7594`  
		Last Modified: Tue, 30 Sep 2025 00:47:25 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae032e01cf18806f9211e435658f6b8acf767627808500b149779d6029a37b69`  
		Last Modified: Tue, 30 Sep 2025 00:47:28 GMT  
		Size: 36.0 MB (35963201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ae932d27bbb63612f4fb5fb512751b08bcc401af88225ead3de9e2f03d328f`  
		Last Modified: Tue, 30 Sep 2025 00:47:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1d537d64fcadf112b5d1c3fab00293199ebaed9a47f51628af214e50fae3d0`  
		Last Modified: Wed, 01 Oct 2025 09:41:35 GMT  
		Size: 14.3 MB (14272179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826aaffae4998cb9c3ec8e33b6a50228036524ca35a7d0e564e9ba49b60e27a8`  
		Last Modified: Tue, 30 Sep 2025 03:38:55 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed236373a948468c26a8f5aec5750c7d4792e2ab14ba0c0e404b33e9231633e`  
		Last Modified: Tue, 30 Sep 2025 03:38:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1be68973de91c8873042f4c6c8db0429e8d999b8d077df3c0defd28cac36c1`  
		Last Modified: Tue, 30 Sep 2025 03:39:02 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:de5edababd38b28b99dc35ae8af644e1b33878c7333a0f1e4c9e645247cca8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a11b35005fefc527ccd7eee05f7350fefae0aaa503e01f0cf3d808958c3540`

```dockerfile
```

-	Layers:
	-	`sha256:6999c90a90fdb165302d454f9abc4348489fc7f53adbf25f515c07ca05c84c4c`  
		Last Modified: Wed, 01 Oct 2025 14:28:28 GMT  
		Size: 2.7 MB (2668422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84937a2c41c762f957796ba60c18bfc6edf95dde39dcd9076a4eaf19e20a221e`  
		Last Modified: Wed, 01 Oct 2025 14:28:29 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:66ae7a4cb33d5257e84533632482c730267136184922951881649ee7841d9990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75419177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a817a073cc71e4d67c1670833984eb2dda781e9fc1b00cede4a20e6869e5d5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e1e8cf6a98b379fbf689c13a9736cd1289212f7d1817f7bef04f737d92c4359f`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 25.8 MB (25757437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7928f871bebd8c2fc35d896a5805704d5e891400d012f02566a89a93c9ecda20`  
		Last Modified: Tue, 30 Sep 2025 01:44:07 GMT  
		Size: 3.1 MB (3079747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6fdd13720cf19cd9bc49bf7088b8bfc257c2fa0971c343609f53a49a1285d4`  
		Last Modified: Tue, 30 Sep 2025 01:44:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dab461172145ceba29910b806bc000e3419504c99ccee67392781ee6ea37a20`  
		Last Modified: Tue, 30 Sep 2025 03:02:32 GMT  
		Size: 32.3 MB (32327029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7f364054c952d8cd0ff7cd0823ec7a05d5157193610f2f4dd9dc72e701432a`  
		Last Modified: Tue, 30 Sep 2025 01:58:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2cb131e0f23e2e89bf12dabc2c892c08857336eef5741460b3cb1a74b7e2d`  
		Last Modified: Tue, 30 Sep 2025 03:06:12 GMT  
		Size: 14.3 MB (14252576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ed329100ef85f50a8927e1c42bd4dfc4b527669980d6bb917b68003d79f360`  
		Last Modified: Tue, 30 Sep 2025 03:06:10 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e96acf9f6766243d02696eda8a8176bc779a5c123036146223b9a2016c0af0`  
		Last Modified: Tue, 30 Sep 2025 03:06:10 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8387f5129a4bece54734c5830b9d2f7e284483fe9885036f8fc063df53fbdbd0`  
		Last Modified: Tue, 30 Sep 2025 03:06:11 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7033428c702ac2aa0cabb7863b968e92cae0a04c13b569bd7d13ec05ee547ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69853da0c16f4a4bf4531e8ee29cca366d149997623a96abd545847e4c93d7ec`

```dockerfile
```

-	Layers:
	-	`sha256:ae786dfb7fff437bfc17b19b0aa46665e65310343316559ecbee7cd05b691ee2`  
		Last Modified: Tue, 30 Sep 2025 08:28:31 GMT  
		Size: 2.7 MB (2672217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9f82e87937f5c40b9ef6a2162ed8c95a67bfa6428a4346c59ee3c17d274c5a`  
		Last Modified: Tue, 30 Sep 2025 08:28:32 GMT  
		Size: 21.2 KB (21181 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:93050681f23eeaead5666294de38063c533906a29d6a5dedf42e5c4f0384e38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73182479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d4f1fbf5ffa8982ac800159fdb0124bb20288e3ea6a26cf565a3f18a9f4242`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4ce8dee9fef27a978e5996d8652a96aaf2074c2682c67960868be3f1a8e907`  
		Last Modified: Tue, 09 Sep 2025 01:45:08 GMT  
		Size: 2.9 MB (2912799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8f5d6b0c22a567f6582616a7d405b850499c3af2f9788d84cfcab5c2b2f645`  
		Last Modified: Tue, 09 Sep 2025 01:45:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c2df61321267472da1fdd3255ba0e599feeafff3656c58995e25d5acc48ce7`  
		Last Modified: Tue, 09 Sep 2025 06:29:38 GMT  
		Size: 32.2 MB (32161914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873f33a6ed8bfffca34bf2f5d22f672cfa175bc465f0d19b4ad2054ea11aa76e`  
		Last Modified: Tue, 09 Sep 2025 01:45:06 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690bb237c4e5e0f6d20259689c81525660eed7459c794268eea23148a6ca26ed`  
		Last Modified: Tue, 09 Sep 2025 07:10:43 GMT  
		Size: 14.2 MB (14171469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778273337874732fa8b06590eeb9afd39fd134e5e61daef9fe8457e4bc39cad0`  
		Last Modified: Tue, 09 Sep 2025 07:10:40 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff93d387bb8f22c19bcd1dc43043129626ace3e1b7c115502ca1ee7c3e1ae344`  
		Last Modified: Tue, 09 Sep 2025 07:10:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300fd1fd6cfc3f2c5f3e2ce3281bcf5174341f6ea40c9a8ddabbce93a14ee5ea`  
		Last Modified: Tue, 09 Sep 2025 07:10:33 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:74fef4145a74800f1a8a057b7d44e0c817150517bb8d9d70643bd89cd3568e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcdfec5cf7850fd1eda2575e31cf893e855f0afd5d466ce62987b60ed0c912e`

```dockerfile
```

-	Layers:
	-	`sha256:09d2f4d9d43700511e1bc42d0b87eb0e3061673c49050550b0eecd5507244ed9`  
		Last Modified: Tue, 09 Sep 2025 08:28:38 GMT  
		Size: 2.7 MB (2670648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7369731b1a0bd672cefa6e900d7d1b1c41c7ee89bc10579289df2d349e6ae19c`  
		Last Modified: Tue, 09 Sep 2025 08:28:39 GMT  
		Size: 21.2 KB (21180 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:87bd2cd4c67e94768b9035e7f81812be9af6ad4771e24913183eb169c195acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81625542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e6505d32bdd80497c17c4a68fb3bdfa4bc128a22436b7e8e140935adf4ff98`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1445bf21318ccbcd2d2ac318d6daca17bf8625cc188526c9bf3a628c06668071`  
		Last Modified: Tue, 30 Sep 2025 00:48:34 GMT  
		Size: 3.3 MB (3340600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4643ff5c706b7dea0e7b5bc08c60463e88fafaec16b10036a1d872ee33af5961`  
		Last Modified: Tue, 30 Sep 2025 00:48:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6838957d0ee261d891b43b86108567042c917e5d712e93afc8a47d9ffe0a3ade`  
		Last Modified: Tue, 30 Sep 2025 00:48:39 GMT  
		Size: 35.9 MB (35900507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a429faaf5f683caa611b556d6cd266d91b7e6e5622d0442d5da2e9543c32e124`  
		Last Modified: Tue, 30 Sep 2025 00:48:34 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06a05b6a2b0cd2e2c5481717e2f27171d10aa72501f786d5671654030eada67`  
		Last Modified: Tue, 30 Sep 2025 01:26:31 GMT  
		Size: 14.3 MB (14279904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734ea23d0c2c882d54cf3099c31768b9f7ee40f8218111fa656ec26f8980fe53`  
		Last Modified: Tue, 30 Sep 2025 01:26:30 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eb422984a20355451e1ebd0c5d61792d8d72c09a93c204cc566082db8b96a0`  
		Last Modified: Tue, 30 Sep 2025 01:26:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1bbd529546e05a1cf5f8876b01e75a310255f79638a0b0b67d47571407bcc`  
		Last Modified: Tue, 30 Sep 2025 01:26:30 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:2a762122992afe7ab6a312e8ee0fcd5e687462d9474e68f1ae722bdc56985b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd86414c7ffd69b89740a18a4a7f3c9cec33a569aab1879d2059b6aa07ddfca`

```dockerfile
```

-	Layers:
	-	`sha256:46fc0694c8873eeb7ffeb59a041362ad3b1e285a7b41942c556ac7263ff8cac2`  
		Last Modified: Wed, 01 Oct 2025 11:35:14 GMT  
		Size: 2.7 MB (2668662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebee3a6585aeb10d3f7662f99bd81c53fa2103862ed139f2403a513fa73c6f2`  
		Last Modified: Wed, 01 Oct 2025 11:35:15 GMT  
		Size: 21.2 KB (21199 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:6207bbd88341f628bee5a030e5020957137e2e4d597320d3a305a4d3eef1b4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78948791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4c7e9ce8fb3c722519113982b3a52b18d2f187d3b57e3dc9d6e94dda86db2e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9866f1e3ecc6d78a20307df8c713a20fae543c2fb2ee9ad903b4043a89e46a4`  
		Last Modified: Tue, 30 Sep 2025 00:47:18 GMT  
		Size: 3.5 MB (3510975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e30ccbbf512cc25963219cc7b180c2616ef7bf8587f8a123bf773b8a5ccbf8`  
		Last Modified: Tue, 30 Sep 2025 00:47:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0467c51c41b55e108743baf291095bf58d260774770a9e5334cce94249fa3303`  
		Last Modified: Tue, 30 Sep 2025 00:47:20 GMT  
		Size: 32.2 MB (32159943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28638e9f71e1c49797ad1bbee7e5ac328025927e3cbbebeb24d8a63f8739680`  
		Last Modified: Tue, 30 Sep 2025 00:47:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976b67074ae2aa3bde10c69d5f5631775325d5d36a2af49225bc720bcda8445e`  
		Last Modified: Tue, 30 Sep 2025 01:25:06 GMT  
		Size: 14.1 MB (14065856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce77b7edc8f0df8cabf1267214746abb296c8a70d3269d5790de91671593ade`  
		Last Modified: Tue, 30 Sep 2025 01:25:05 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74dc59d7a01df8898d09ed147533ed1daa5e5a0f2c39429412c94d5be66b0d4`  
		Last Modified: Tue, 30 Sep 2025 01:25:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cf065a1cfadcb686e969f76e2b16c11c95aae52c651a35bc842ff3ed0cb2d9`  
		Last Modified: Tue, 30 Sep 2025 01:25:05 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:4c25420f43d4d27b12898bb82ace50832c705257e407b1bff51d33df1082a99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c34d590cec2e6f7bbab2f808eb5d7af534330f4bb7df1082ab4aab16eb09250`

```dockerfile
```

-	Layers:
	-	`sha256:679ff5366c3efc942953d51cc2358164011d5fa8a5d8389fa43c603f9e4cb241`  
		Last Modified: Wed, 01 Oct 2025 18:04:08 GMT  
		Size: 2.7 MB (2665601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8392399ff128f18d9567f3c8d2027976d108142f363c235d1efaf6f8f3ddd961`  
		Last Modified: Wed, 01 Oct 2025 18:04:07 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:ebff0f353ca87f433c4ca1a79cb328b32d877add1a1a668d0e1522fc7f3a6768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84276348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ee54f28d6395578918ebf2c75f269ee5397f8a4920e65fda610245a64a53b3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032a57e3d5f8b2442867f60cad2c164df4838776060718078382e234a9a79b80`  
		Last Modified: Tue, 09 Sep 2025 08:56:23 GMT  
		Size: 3.7 MB (3709108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bf3ea547b16299a98bd6553b0327e55bf9d889bb7e9a34eeb3809f4739eb59`  
		Last Modified: Tue, 09 Sep 2025 08:56:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b187b3dc4744bcf2e5b0cd38aec07892ee2463dadf6590b7762d571cb7a88e`  
		Last Modified: Tue, 09 Sep 2025 08:37:43 GMT  
		Size: 33.8 MB (33832555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e376eda6962a88611b1fa354a1a54f6109538766affdf0edcc4ede606cf09d`  
		Last Modified: Tue, 09 Sep 2025 08:37:37 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fe8f745171af37a5e4aac61e1ca623d3e3bf8389aff95c8df25e7cd9cb9c58`  
		Last Modified: Tue, 09 Sep 2025 20:15:36 GMT  
		Size: 14.7 MB (14663528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba35e0103d3df86d2f50fb294ad76f6d623b42ec502a3ea645954c506bcd0e87`  
		Last Modified: Tue, 09 Sep 2025 20:15:35 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1df22aa521c9d365cf236d0384b0cc70a0a3d994e2b06ca56c8b8b96f5a604f`  
		Last Modified: Tue, 09 Sep 2025 20:15:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a272f17ba87b74583e3372768135687dd19721ff8fd46daa7209bbf7da576`  
		Last Modified: Tue, 09 Sep 2025 20:15:35 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3b208e7b67171a0efa5087be2f1752dda5bd67ca5bbf561396033c8bd24e8af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b94b8aeea9db413fc387af87caff8e7c6fdd8e852e7a1aee59b3548613195b`

```dockerfile
```

-	Layers:
	-	`sha256:dcf3f69a53852e6990dbba65114b563d71ab80acda7ea0723cbf0db6e5578430`  
		Last Modified: Tue, 09 Sep 2025 20:28:41 GMT  
		Size: 2.7 MB (2672839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39ef407a04c55f676d34a9f20d0f669a2a81a46ed395775d3643553f35f6028f`  
		Last Modified: Tue, 09 Sep 2025 20:28:42 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:266eb6a6ec8098e4ac50aec5be1aaebde50fb07111e898caa673c91856a72efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77557645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d40d54e3b4548da7825464b7774bc001c9ec927afac96aef53be41791fa57ca`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390e76980816039bea819b7c18b019a550bd1474594cd9c6932a1978f03e70ec`  
		Last Modified: Tue, 09 Sep 2025 04:57:51 GMT  
		Size: 3.2 MB (3170276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f820fbb71400175128c13402320f002b7f0eaaf6ea87fa677dfce1823d20eb3`  
		Last Modified: Tue, 09 Sep 2025 04:58:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d31be15fc6204597180b0b4c00b002eb1344fe12c053fbcda06f052a8bf61b`  
		Last Modified: Tue, 09 Sep 2025 09:17:46 GMT  
		Size: 33.1 MB (33098963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18c82b0958dcaf951ee6dae7be74137b1fc7634a5ec90193385b41c41c48d49`  
		Last Modified: Tue, 09 Sep 2025 05:23:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6702cf60d92e89cf8dae04643270aefe240ee9d7430b917d62d06fabd7f3329`  
		Last Modified: Tue, 09 Sep 2025 15:33:11 GMT  
		Size: 14.4 MB (14401708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d49b97c44a05f2058221ea9202180a934cb0d70cd06e7ea2c64119fff6ae94`  
		Last Modified: Tue, 09 Sep 2025 15:33:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd47ea13c5fbb38183f77b62a65442c3176805349efd97a200502fb6b4949ea1`  
		Last Modified: Tue, 09 Sep 2025 15:33:12 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30cfbd888301b2b5aab591ddf968b7d0dbc6b53408b9c8cc0f906013856ea7`  
		Last Modified: Tue, 09 Sep 2025 15:33:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d7ca13fffeeacf4276954f41b230827039736df37cebe5d5728d5686c0b59055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b796b6d1468d53dcbcc3121b953c181d3e4c4f188b03c227ffbdb268770bff`

```dockerfile
```

-	Layers:
	-	`sha256:cc89dcac709092c04fa6f0835e84d2f2a373f192f72acad94b1d7530c930c77b`  
		Last Modified: Tue, 09 Sep 2025 17:28:49 GMT  
		Size: 2.7 MB (2665247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e5bd3191bd38bc560c749cd5a19ca5bbbe88ee8c07cb901f89c64bb58dd3c9`  
		Last Modified: Tue, 09 Sep 2025 17:28:51 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.9-1.0`

```console
$ docker pull fluentd@sha256:9de84688a450e7f7140255bfb42faa98919c6a5b74b7844f5c0e2ef6b08a4d98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `fluentd:v1.16.9-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:62b59793f4b04db4c6c55dc596c9b0f6f2f609ba3a5ca8a07a172ce4c4c94c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17364715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecdf9365b5088dc631ac62d36f5d484ca8b41403d0b0a72f4b722067edfda52`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-x86_64.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:1747dece94917ce1b0256ecd60138ce4deaea1bd35dcb6b2e8afe697dd2f5b71`  
		Last Modified: Tue, 15 Jul 2025 18:59:51 GMT  
		Size: 3.4 MB (3415528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb31392c80bf139027b4fd99580f002640be382bc230598d0941fbc23840ef33`  
		Last Modified: Tue, 15 Jul 2025 19:30:51 GMT  
		Size: 13.9 MB (13947023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c2ab18679e720bc1b529d183c9e15a48bf8c51a44a96a5c88b1d30b63a2c5`  
		Last Modified: Tue, 15 Jul 2025 19:30:50 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ea010677b96e4da2f5996a87356528d7b83e6d8e7415e71b1a3fa88881560a`  
		Last Modified: Tue, 15 Jul 2025 19:30:50 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1c21fa85330ecf72a0795c2b88bf00f53608df1e52650afa9afe49db36bb50`  
		Last Modified: Tue, 15 Jul 2025 19:30:50 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:15f98fe183630cf6012aee43db490b5b7882c6fdcf38f22d2f8e2b95e3855079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.5 KB (983521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6ad4fbad3aad763dda59b0b642589920d6a1e88ea88f6b8aaf325e84b16899`

```dockerfile
```

-	Layers:
	-	`sha256:ac17ac913e35c4ba176d2d64ee52cdde0734638a314f5b8d613c95d9bc6741f0`  
		Last Modified: Tue, 15 Jul 2025 23:28:24 GMT  
		Size: 969.8 KB (969844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14dd3de9a6f820396ef937efd2c044817d9e6abd24d0eed9fbfc6b24c1875d1b`  
		Last Modified: Tue, 15 Jul 2025 23:28:25 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; arm variant v6

```console
$ docker pull fluentd@sha256:351b12279af00d88a2f18a5cb8e919827c85d763c18ff31f79a381234941b0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16109845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf130dec1abbd0aa653924329e6c59a00675fea2f4c6e75df38ecdecedd5ffa`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-armhf.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0e31a7d1c448a18b75fd3ddf2a65dd820ec700316bcfa8710102fe2f00bf666d`  
		Last Modified: Tue, 15 Jul 2025 18:59:54 GMT  
		Size: 3.2 MB (3171284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4343a8d06e457dbc08b054339bb7f7be3c9c2c5757fc87ea56cf9dabdcc5d6`  
		Last Modified: Wed, 16 Jul 2025 03:31:09 GMT  
		Size: 12.9 MB (12936392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faa7724a34ca0aef3b0ace8626793bc73b0e9d6e07fc5b0802a13ba6147944a`  
		Last Modified: Wed, 16 Jul 2025 03:31:06 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184956266683be8c9f84a71faf719699d2f454733113a25ca9827fc3939d9c93`  
		Last Modified: Wed, 16 Jul 2025 03:31:06 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a932b6fa02679e51e14d11c560c02504b0d8c2a550bce03802de73690911242`  
		Last Modified: Wed, 16 Jul 2025 03:31:06 GMT  
		Size: 457.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:80cf01eb1c833e1bff5b8bdc8d9f290e69d4f6a97331a2bf5de3f4ea8bd19f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 KB (13534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26c4cc20d3ce8522ca396d0c91859a7e01ecb4062649250087f770a95de0e33`

```dockerfile
```

-	Layers:
	-	`sha256:8c2a9a72c22295d5920c01a388d4107c49e60ae3cad8ce845b3161011e672e14`  
		Last Modified: Wed, 16 Jul 2025 05:28:30 GMT  
		Size: 13.5 KB (13534 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a26fafeea7e9dafc17c25197f75a0753de807961ffeb537a47cbf987c24762b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17346810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5f99a4238a53d779bb2e08e2dc478d6a2b34eb23b7c3c65a11546185b7036f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-aarch64.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:07e9a47f0c334cceba1b05e86ef0150c84564a9b9e9d4ae9dc9a5ebc85ef2b7c`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.4 MB (3353103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac6f34639e69d841f4495144c2925c0369698cb3a2cae79a9842c514901f627`  
		Last Modified: Wed, 16 Jul 2025 05:51:44 GMT  
		Size: 14.0 MB (13991540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a5dddf287fe6eebc80c2255f53f18794044f9da69e7623acead7b274569e71`  
		Last Modified: Wed, 16 Jul 2025 05:51:43 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ae2844be3a10be052663f438d979ba2f03ac6c89a841fe6c44d5bc43f9ef2`  
		Last Modified: Wed, 16 Jul 2025 05:51:43 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3fd133ef2a740f7af3d063cfc0a9b2b09f56acc15218bb892a61b87f61d5009`  
		Last Modified: Wed, 16 Jul 2025 05:51:43 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:de4a4d3ee8b708e1ade04f7655238c9c98e3c302de6454df62cb7418c872231c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.7 KB (983744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6249690a5c15f0ddc47117703b20625dbd6b6766374531c80e1aa1011bd27151`

```dockerfile
```

-	Layers:
	-	`sha256:f63e498bb20dbf58b4a2452acd41ec4ccc42f816041d6c2866d3af691bdd9c61`  
		Last Modified: Wed, 16 Jul 2025 08:28:29 GMT  
		Size: 970.0 KB (969974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c92fef769075859e78e86eab6f06f019775338f1f17070f36b199227a263e8`  
		Last Modified: Wed, 16 Jul 2025 08:28:29 GMT  
		Size: 13.8 KB (13770 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:9aece902e3a3c67c1c8f07a5af1580b708e81ecd7cc648650c939c91611d40f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16322333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cae686b1630babd15276674ab92d0a68b364bc88da5b6b541e25e921e95849`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-x86.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8505dab4c7114bf55a3da6a1e965a64c37604a0946b636bbc8606ab749093ccd`  
		Last Modified: Tue, 15 Jul 2025 19:05:03 GMT  
		Size: 3.3 MB (3250248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60783d300fa1186dce9b5c3eb11e36eeb62b943e964e71d994a199dd844061e`  
		Last Modified: Tue, 15 Jul 2025 19:25:25 GMT  
		Size: 13.1 MB (13069919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f44371e03cbf1bf428865c36018c43fdf75eb65bfc7ba651f46a84b7ce3ecb8`  
		Last Modified: Tue, 15 Jul 2025 19:25:25 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a6c9357c06ddb35d0559e0665e7d6dd592fb6505c0753f3cc1c5e5c9118ac5`  
		Last Modified: Tue, 15 Jul 2025 19:25:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93df47fb815f854253728dec79fa657e087eba34447ba0de9f51ff9591efda68`  
		Last Modified: Tue, 15 Jul 2025 19:25:25 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:a52d394b2d621b060b1d8308be8374fc09ae3b3821b249f0866cf065202e92c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **980.2 KB (980248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089a9b49170e879d8c95c2b64e66fc1a84a6f2a03ccba3c448ee09106e4bd231`

```dockerfile
```

-	Layers:
	-	`sha256:03414bf4b8575ff108fcbefa4c874acec592dcb6896c72866f14b88d848539e1`  
		Last Modified: Tue, 15 Jul 2025 20:28:41 GMT  
		Size: 966.6 KB (966595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe1d28ac62dba6185ab4068ca0528498a5952903219b1bd4e33e785fb756033a`  
		Last Modified: Tue, 15 Jul 2025 20:28:42 GMT  
		Size: 13.7 KB (13653 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:4aeaebfa64236f2d8db0d5a40275bf6deb6f2dcec066527b64a1c21f37bd7c16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16913295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a51f8c1e76a03a08b2a69fa65ba4a480734665505f15f26e9bb86646f4e9cf`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-ppc64le.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:fad02e700aec982dd556a4276525680657ee6d1abbd1dd39a3e5709a60a75613`  
		Last Modified: Tue, 15 Jul 2025 19:01:18 GMT  
		Size: 3.4 MB (3362956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5d57847cb10b83ca39cc4849fdda1e8edf05460e6a52c83dc598ec2e945a2f`  
		Last Modified: Wed, 16 Jul 2025 01:17:41 GMT  
		Size: 13.5 MB (13548173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1127c667ffbc25946037843047f5ab11e8ca6a37dde4395320a26ae06d333d`  
		Last Modified: Wed, 16 Jul 2025 01:17:40 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4327b6146ba57f1fd1978f3014c06eb3fb8a5db0e24a14b10d7c74248b7952aa`  
		Last Modified: Wed, 16 Jul 2025 01:17:39 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cdb95f433df582af09b964a55b09ea777b751e7ef074155ee6d5979fa4e313`  
		Last Modified: Wed, 16 Jul 2025 01:17:39 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fa617bfb00ff80c808e63b3f9ac0f249a10b0870b4db6e3fedcc95d21ef95a10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **979.1 KB (979078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677c3e30f08c6b32a44bf0e3eb3c25daa3dcc57878b6dbe7e9c6fd7a4f088eea`

```dockerfile
```

-	Layers:
	-	`sha256:dee0d912acf98283f9dd49f6106e0be3d1d551344dfc546eeeb0be4643fd801d`  
		Last Modified: Wed, 16 Jul 2025 02:28:33 GMT  
		Size: 965.4 KB (965367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e392f84bf352484fc6ba2d9ea94e671159f3593a26e10fe29b7fe699a8ddff3`  
		Last Modified: Wed, 16 Jul 2025 02:28:33 GMT  
		Size: 13.7 KB (13711 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:0230735e64f8c499a8822fd5921c882a6d21fc8065a6872e143e8d07db3d1888
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16747299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b213617173eda7f4321012a955d2c166af985ca61f04deb7a99e1eb25fa1de4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
ADD alpine-minirootfs-3.19.8-s390x.tar.gz / # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["/bin/sh"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
RUN apk update  && apk add --no-cache         ca-certificates         ruby ruby-irb ruby-etc ruby-webrick         tini  && apk add --no-cache --virtual .build-deps         build-base linux-headers         ruby-dev gnupg  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && gem install bigdecimal -v 1.4.4  && apk del .build-deps  && rm -rf /var/cache/apk/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN addgroup -S fluent && adduser -S -G fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:163224d0518e3abf0736ac8d226fdeefbf22e84c44de3b1a3b6c7c2beebd0942`  
		Last Modified: Tue, 15 Jul 2025 19:01:22 GMT  
		Size: 3.2 MB (3249001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd9c37afb374edc1a68dba4f5da69615429c45b07f7ccef55fd5ec9ad6c36c2`  
		Last Modified: Wed, 16 Jul 2025 04:57:53 GMT  
		Size: 13.5 MB (13496133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b895a58cefb82f036ccd42bfd305c06b6a42bdabe8ae47e6e8c1aa075b462f4d`  
		Last Modified: Wed, 16 Jul 2025 04:57:53 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e41aa6a1308c1b1acb531c12a5067a0903ddccca60e4ace040c07f6b261ec4`  
		Last Modified: Wed, 16 Jul 2025 04:57:52 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c7a0b685e1f3ae0425103b1f625d0be50d953f19bf5c28512420ed3c1d8ca9`  
		Last Modified: Wed, 16 Jul 2025 04:57:52 GMT  
		Size: 456.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0f6f12ef7be26befc1cc3823d3ebe0ece9f58d77d481ea4fc1a595f7b99a8c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **978.4 KB (978434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f638219539f7263020b8ee67a597818fa1d5033e40d39cbb7b54898b57f7263`

```dockerfile
```

-	Layers:
	-	`sha256:1cd5461e768d2c51326c4d2783ebc6d4a9d026e60b9928132e3d24fcc1dda87b`  
		Last Modified: Wed, 16 Jul 2025 05:28:40 GMT  
		Size: 964.8 KB (964757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c51c00df0ed05c9bb25a85a3331581d44e97dec65ef657ed0ce3339d002b7b79`  
		Last Modified: Wed, 16 Jul 2025 05:28:41 GMT  
		Size: 13.7 KB (13677 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.9-debian-1.0`

```console
$ docker pull fluentd@sha256:3d2550fa1be917e7dfcb301d6693d1aa6792dadb8a6938c8ae2d752610a3675b
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

### `fluentd:v1.16.9-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:6ee4f4acacefb378f770c647c56eea2e4354596106132940d6e3795148ed8640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81975748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4792a4b2f463ace4bb6fde0596054efbe7569e8d48ed304c91ccf33618cb8c7d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd5cf0535143f813c81dc40977600297fc84dac6ad168c2f2760428b130f32b`  
		Last Modified: Tue, 30 Sep 2025 00:47:25 GMT  
		Size: 3.5 MB (3509642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0588fc42e3de39c565a8e08f901e22ada10040e44c8c294c00261755ae7594`  
		Last Modified: Tue, 30 Sep 2025 00:47:25 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae032e01cf18806f9211e435658f6b8acf767627808500b149779d6029a37b69`  
		Last Modified: Tue, 30 Sep 2025 00:47:28 GMT  
		Size: 36.0 MB (35963201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ae932d27bbb63612f4fb5fb512751b08bcc401af88225ead3de9e2f03d328f`  
		Last Modified: Tue, 30 Sep 2025 00:47:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1d537d64fcadf112b5d1c3fab00293199ebaed9a47f51628af214e50fae3d0`  
		Last Modified: Wed, 01 Oct 2025 09:41:35 GMT  
		Size: 14.3 MB (14272179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826aaffae4998cb9c3ec8e33b6a50228036524ca35a7d0e564e9ba49b60e27a8`  
		Last Modified: Tue, 30 Sep 2025 03:38:55 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed236373a948468c26a8f5aec5750c7d4792e2ab14ba0c0e404b33e9231633e`  
		Last Modified: Tue, 30 Sep 2025 03:38:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1be68973de91c8873042f4c6c8db0429e8d999b8d077df3c0defd28cac36c1`  
		Last Modified: Tue, 30 Sep 2025 03:39:02 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:de5edababd38b28b99dc35ae8af644e1b33878c7333a0f1e4c9e645247cca8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a11b35005fefc527ccd7eee05f7350fefae0aaa503e01f0cf3d808958c3540`

```dockerfile
```

-	Layers:
	-	`sha256:6999c90a90fdb165302d454f9abc4348489fc7f53adbf25f515c07ca05c84c4c`  
		Last Modified: Wed, 01 Oct 2025 14:28:28 GMT  
		Size: 2.7 MB (2668422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84937a2c41c762f957796ba60c18bfc6edf95dde39dcd9076a4eaf19e20a221e`  
		Last Modified: Wed, 01 Oct 2025 14:28:29 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:66ae7a4cb33d5257e84533632482c730267136184922951881649ee7841d9990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75419177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a817a073cc71e4d67c1670833984eb2dda781e9fc1b00cede4a20e6869e5d5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e1e8cf6a98b379fbf689c13a9736cd1289212f7d1817f7bef04f737d92c4359f`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 25.8 MB (25757437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7928f871bebd8c2fc35d896a5805704d5e891400d012f02566a89a93c9ecda20`  
		Last Modified: Tue, 30 Sep 2025 01:44:07 GMT  
		Size: 3.1 MB (3079747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6fdd13720cf19cd9bc49bf7088b8bfc257c2fa0971c343609f53a49a1285d4`  
		Last Modified: Tue, 30 Sep 2025 01:44:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dab461172145ceba29910b806bc000e3419504c99ccee67392781ee6ea37a20`  
		Last Modified: Tue, 30 Sep 2025 03:02:32 GMT  
		Size: 32.3 MB (32327029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7f364054c952d8cd0ff7cd0823ec7a05d5157193610f2f4dd9dc72e701432a`  
		Last Modified: Tue, 30 Sep 2025 01:58:34 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc2cb131e0f23e2e89bf12dabc2c892c08857336eef5741460b3cb1a74b7e2d`  
		Last Modified: Tue, 30 Sep 2025 03:06:12 GMT  
		Size: 14.3 MB (14252576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ed329100ef85f50a8927e1c42bd4dfc4b527669980d6bb917b68003d79f360`  
		Last Modified: Tue, 30 Sep 2025 03:06:10 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e96acf9f6766243d02696eda8a8176bc779a5c123036146223b9a2016c0af0`  
		Last Modified: Tue, 30 Sep 2025 03:06:10 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8387f5129a4bece54734c5830b9d2f7e284483fe9885036f8fc063df53fbdbd0`  
		Last Modified: Tue, 30 Sep 2025 03:06:11 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7033428c702ac2aa0cabb7863b968e92cae0a04c13b569bd7d13ec05ee547ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69853da0c16f4a4bf4531e8ee29cca366d149997623a96abd545847e4c93d7ec`

```dockerfile
```

-	Layers:
	-	`sha256:ae786dfb7fff437bfc17b19b0aa46665e65310343316559ecbee7cd05b691ee2`  
		Last Modified: Tue, 30 Sep 2025 08:28:31 GMT  
		Size: 2.7 MB (2672217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9f82e87937f5c40b9ef6a2162ed8c95a67bfa6428a4346c59ee3c17d274c5a`  
		Last Modified: Tue, 30 Sep 2025 08:28:32 GMT  
		Size: 21.2 KB (21181 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:93050681f23eeaead5666294de38063c533906a29d6a5dedf42e5c4f0384e38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73182479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09d4f1fbf5ffa8982ac800159fdb0124bb20288e3ea6a26cf565a3f18a9f4242`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e747f8ef7f1d9a41c99bfb53889f7b8de3504300740a326627fc7522904708cc`  
		Last Modified: Mon, 08 Sep 2025 21:14:21 GMT  
		Size: 23.9 MB (23933904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4ce8dee9fef27a978e5996d8652a96aaf2074c2682c67960868be3f1a8e907`  
		Last Modified: Tue, 09 Sep 2025 01:45:08 GMT  
		Size: 2.9 MB (2912799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8f5d6b0c22a567f6582616a7d405b850499c3af2f9788d84cfcab5c2b2f645`  
		Last Modified: Tue, 09 Sep 2025 01:45:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c2df61321267472da1fdd3255ba0e599feeafff3656c58995e25d5acc48ce7`  
		Last Modified: Tue, 09 Sep 2025 06:29:38 GMT  
		Size: 32.2 MB (32161914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873f33a6ed8bfffca34bf2f5d22f672cfa175bc465f0d19b4ad2054ea11aa76e`  
		Last Modified: Tue, 09 Sep 2025 01:45:06 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690bb237c4e5e0f6d20259689c81525660eed7459c794268eea23148a6ca26ed`  
		Last Modified: Tue, 09 Sep 2025 07:10:43 GMT  
		Size: 14.2 MB (14171469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778273337874732fa8b06590eeb9afd39fd134e5e61daef9fe8457e4bc39cad0`  
		Last Modified: Tue, 09 Sep 2025 07:10:40 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff93d387bb8f22c19bcd1dc43043129626ace3e1b7c115502ca1ee7c3e1ae344`  
		Last Modified: Tue, 09 Sep 2025 07:10:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300fd1fd6cfc3f2c5f3e2ce3281bcf5174341f6ea40c9a8ddabbce93a14ee5ea`  
		Last Modified: Tue, 09 Sep 2025 07:10:33 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:74fef4145a74800f1a8a057b7d44e0c817150517bb8d9d70643bd89cd3568e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bcdfec5cf7850fd1eda2575e31cf893e855f0afd5d466ce62987b60ed0c912e`

```dockerfile
```

-	Layers:
	-	`sha256:09d2f4d9d43700511e1bc42d0b87eb0e3061673c49050550b0eecd5507244ed9`  
		Last Modified: Tue, 09 Sep 2025 08:28:38 GMT  
		Size: 2.7 MB (2670648 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7369731b1a0bd672cefa6e900d7d1b1c41c7ee89bc10579289df2d349e6ae19c`  
		Last Modified: Tue, 09 Sep 2025 08:28:39 GMT  
		Size: 21.2 KB (21180 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:87bd2cd4c67e94768b9035e7f81812be9af6ad4771e24913183eb169c195acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81625542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e6505d32bdd80497c17c4a68fb3bdfa4bc128a22436b7e8e140935adf4ff98`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1445bf21318ccbcd2d2ac318d6daca17bf8625cc188526c9bf3a628c06668071`  
		Last Modified: Tue, 30 Sep 2025 00:48:34 GMT  
		Size: 3.3 MB (3340600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4643ff5c706b7dea0e7b5bc08c60463e88fafaec16b10036a1d872ee33af5961`  
		Last Modified: Tue, 30 Sep 2025 00:48:34 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6838957d0ee261d891b43b86108567042c917e5d712e93afc8a47d9ffe0a3ade`  
		Last Modified: Tue, 30 Sep 2025 00:48:39 GMT  
		Size: 35.9 MB (35900507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a429faaf5f683caa611b556d6cd266d91b7e6e5622d0442d5da2e9543c32e124`  
		Last Modified: Tue, 30 Sep 2025 00:48:34 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06a05b6a2b0cd2e2c5481717e2f27171d10aa72501f786d5671654030eada67`  
		Last Modified: Tue, 30 Sep 2025 01:26:31 GMT  
		Size: 14.3 MB (14279904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734ea23d0c2c882d54cf3099c31768b9f7ee40f8218111fa656ec26f8980fe53`  
		Last Modified: Tue, 30 Sep 2025 01:26:30 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27eb422984a20355451e1ebd0c5d61792d8d72c09a93c204cc566082db8b96a0`  
		Last Modified: Tue, 30 Sep 2025 01:26:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc1bbd529546e05a1cf5f8876b01e75a310255f79638a0b0b67d47571407bcc`  
		Last Modified: Tue, 30 Sep 2025 01:26:30 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:2a762122992afe7ab6a312e8ee0fcd5e687462d9474e68f1ae722bdc56985b65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd86414c7ffd69b89740a18a4a7f3c9cec33a569aab1879d2059b6aa07ddfca`

```dockerfile
```

-	Layers:
	-	`sha256:46fc0694c8873eeb7ffeb59a041362ad3b1e285a7b41942c556ac7263ff8cac2`  
		Last Modified: Wed, 01 Oct 2025 11:35:14 GMT  
		Size: 2.7 MB (2668662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bebee3a6585aeb10d3f7662f99bd81c53fa2103862ed139f2403a513fa73c6f2`  
		Last Modified: Wed, 01 Oct 2025 11:35:15 GMT  
		Size: 21.2 KB (21199 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:6207bbd88341f628bee5a030e5020957137e2e4d597320d3a305a4d3eef1b4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78948791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4c7e9ce8fb3c722519113982b3a52b18d2f187d3b57e3dc9d6e94dda86db2e`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:5a19917fb037e6569ceef43a0b0faa5c3f8554f4d9b154320d254dea136b463a`  
		Last Modified: Mon, 29 Sep 2025 23:35:20 GMT  
		Size: 29.2 MB (29209630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9866f1e3ecc6d78a20307df8c713a20fae543c2fb2ee9ad903b4043a89e46a4`  
		Last Modified: Tue, 30 Sep 2025 00:47:18 GMT  
		Size: 3.5 MB (3510975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e30ccbbf512cc25963219cc7b180c2616ef7bf8587f8a123bf773b8a5ccbf8`  
		Last Modified: Tue, 30 Sep 2025 00:47:18 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0467c51c41b55e108743baf291095bf58d260774770a9e5334cce94249fa3303`  
		Last Modified: Tue, 30 Sep 2025 00:47:20 GMT  
		Size: 32.2 MB (32159943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28638e9f71e1c49797ad1bbee7e5ac328025927e3cbbebeb24d8a63f8739680`  
		Last Modified: Tue, 30 Sep 2025 00:47:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976b67074ae2aa3bde10c69d5f5631775325d5d36a2af49225bc720bcda8445e`  
		Last Modified: Tue, 30 Sep 2025 01:25:06 GMT  
		Size: 14.1 MB (14065856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce77b7edc8f0df8cabf1267214746abb296c8a70d3269d5790de91671593ade`  
		Last Modified: Tue, 30 Sep 2025 01:25:05 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74dc59d7a01df8898d09ed147533ed1daa5e5a0f2c39429412c94d5be66b0d4`  
		Last Modified: Tue, 30 Sep 2025 01:25:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cf065a1cfadcb686e969f76e2b16c11c95aae52c651a35bc842ff3ed0cb2d9`  
		Last Modified: Tue, 30 Sep 2025 01:25:05 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:4c25420f43d4d27b12898bb82ace50832c705257e407b1bff51d33df1082a99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c34d590cec2e6f7bbab2f808eb5d7af534330f4bb7df1082ab4aab16eb09250`

```dockerfile
```

-	Layers:
	-	`sha256:679ff5366c3efc942953d51cc2358164011d5fa8a5d8389fa43c603f9e4cb241`  
		Last Modified: Wed, 01 Oct 2025 18:04:08 GMT  
		Size: 2.7 MB (2665601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8392399ff128f18d9567f3c8d2027976d108142f363c235d1efaf6f8f3ddd961`  
		Last Modified: Wed, 01 Oct 2025 18:04:07 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:ebff0f353ca87f433c4ca1a79cb328b32d877add1a1a668d0e1522fc7f3a6768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84276348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ee54f28d6395578918ebf2c75f269ee5397f8a4920e65fda610245a64a53b3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032a57e3d5f8b2442867f60cad2c164df4838776060718078382e234a9a79b80`  
		Last Modified: Tue, 09 Sep 2025 08:56:23 GMT  
		Size: 3.7 MB (3709108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bf3ea547b16299a98bd6553b0327e55bf9d889bb7e9a34eeb3809f4739eb59`  
		Last Modified: Tue, 09 Sep 2025 08:56:22 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b187b3dc4744bcf2e5b0cd38aec07892ee2463dadf6590b7762d571cb7a88e`  
		Last Modified: Tue, 09 Sep 2025 08:37:43 GMT  
		Size: 33.8 MB (33832555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e376eda6962a88611b1fa354a1a54f6109538766affdf0edcc4ede606cf09d`  
		Last Modified: Tue, 09 Sep 2025 08:37:37 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fe8f745171af37a5e4aac61e1ca623d3e3bf8389aff95c8df25e7cd9cb9c58`  
		Last Modified: Tue, 09 Sep 2025 20:15:36 GMT  
		Size: 14.7 MB (14663528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba35e0103d3df86d2f50fb294ad76f6d623b42ec502a3ea645954c506bcd0e87`  
		Last Modified: Tue, 09 Sep 2025 20:15:35 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1df22aa521c9d365cf236d0384b0cc70a0a3d994e2b06ca56c8b8b96f5a604f`  
		Last Modified: Tue, 09 Sep 2025 20:15:35 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288a272f17ba87b74583e3372768135687dd19721ff8fd46daa7209bbf7da576`  
		Last Modified: Tue, 09 Sep 2025 20:15:35 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3b208e7b67171a0efa5087be2f1752dda5bd67ca5bbf561396033c8bd24e8af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b94b8aeea9db413fc387af87caff8e7c6fdd8e852e7a1aee59b3548613195b`

```dockerfile
```

-	Layers:
	-	`sha256:dcf3f69a53852e6990dbba65114b563d71ab80acda7ea0723cbf0db6e5578430`  
		Last Modified: Tue, 09 Sep 2025 20:28:41 GMT  
		Size: 2.7 MB (2672839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39ef407a04c55f676d34a9f20d0f669a2a81a46ed395775d3643553f35f6028f`  
		Last Modified: Tue, 09 Sep 2025 20:28:42 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:266eb6a6ec8098e4ac50aec5be1aaebde50fb07111e898caa673c91856a72efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77557645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d40d54e3b4548da7825464b7774bc001c9ec927afac96aef53be41791fa57ca`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV LANG=C.UTF-8
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_VERSION=3.2.9
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Fri, 23 May 2025 01:51:58 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Fri, 23 May 2025 01:51:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 May 2025 01:51:58 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Fri, 23 May 2025 01:51:58 GMT
CMD ["irb"]
# Fri, 23 May 2025 01:51:58 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Fri, 23 May 2025 01:51:58 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.9
# Fri, 23 May 2025 01:51:58 GMT
ENV TINI_VERSION=0.18.0
# Fri, 23 May 2025 01:51:58 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.0  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.9  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Fri, 23 May 2025 01:51:58 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
COPY entrypoint.sh /bin/ # buildkit
# Fri, 23 May 2025 01:51:58 GMT
ENV FLUENTD_CONF=fluent.conf
# Fri, 23 May 2025 01:51:58 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Fri, 23 May 2025 01:51:58 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Fri, 23 May 2025 01:51:58 GMT
USER fluent
# Fri, 23 May 2025 01:51:58 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Fri, 23 May 2025 01:51:58 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390e76980816039bea819b7c18b019a550bd1474594cd9c6932a1978f03e70ec`  
		Last Modified: Tue, 09 Sep 2025 04:57:51 GMT  
		Size: 3.2 MB (3170276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f820fbb71400175128c13402320f002b7f0eaaf6ea87fa677dfce1823d20eb3`  
		Last Modified: Tue, 09 Sep 2025 04:58:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d31be15fc6204597180b0b4c00b002eb1344fe12c053fbcda06f052a8bf61b`  
		Last Modified: Tue, 09 Sep 2025 09:17:46 GMT  
		Size: 33.1 MB (33098963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18c82b0958dcaf951ee6dae7be74137b1fc7634a5ec90193385b41c41c48d49`  
		Last Modified: Tue, 09 Sep 2025 05:23:11 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6702cf60d92e89cf8dae04643270aefe240ee9d7430b917d62d06fabd7f3329`  
		Last Modified: Tue, 09 Sep 2025 15:33:11 GMT  
		Size: 14.4 MB (14401708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d49b97c44a05f2058221ea9202180a934cb0d70cd06e7ea2c64119fff6ae94`  
		Last Modified: Tue, 09 Sep 2025 15:33:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd47ea13c5fbb38183f77b62a65442c3176805349efd97a200502fb6b4949ea1`  
		Last Modified: Tue, 09 Sep 2025 15:33:12 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af30cfbd888301b2b5aab591ddf968b7d0dbc6b53408b9c8cc0f906013856ea7`  
		Last Modified: Tue, 09 Sep 2025 15:33:13 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:d7ca13fffeeacf4276954f41b230827039736df37cebe5d5728d5686c0b59055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b796b6d1468d53dcbcc3121b953c181d3e4c4f188b03c227ffbdb268770bff`

```dockerfile
```

-	Layers:
	-	`sha256:cc89dcac709092c04fa6f0835e84d2f2a373f192f72acad94b1d7530c930c77b`  
		Last Modified: Tue, 09 Sep 2025 17:28:49 GMT  
		Size: 2.7 MB (2665247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e5bd3191bd38bc560c749cd5a19ca5bbbe88ee8c07cb901f89c64bb58dd3c9`  
		Last Modified: Tue, 09 Sep 2025 17:28:51 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:8f6b1cf9675279a4472112886e8ecbafaaffcbef27919879b83bca67aa156475
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
$ docker pull fluentd@sha256:968450201f1633b5a796a19818797ba95ada90226e3e78d266de7cc447d702de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79258793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec6b9a837666fac5eef40dadfc3140928de04730d4dc0a2d94cb9d914d4a05f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac80cde22bfc7f1283ae07a881aea9b0ddb32e3c1bd62b6dd738c001461ae80c`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 1.3 MB (1279282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04bd217259e9a1adff42a11c482bc4ce95944a28541de67525db69fd74eb2a`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a793530ea8ee5034845d68f5cf20d39e0d069c36c9df258a0617f3a32fd4252`  
		Last Modified: Tue, 30 Sep 2025 00:46:10 GMT  
		Size: 42.2 MB (42153497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7503b4256904558e2f15b3cccab853eec67b0a9eb298954e71634e22152985c`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7718db5a4f479bb9efa051123d43769274727b3f793a5384e9b524fe083ab476`  
		Last Modified: Tue, 30 Sep 2025 03:38:08 GMT  
		Size: 6.0 MB (6045860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633fe0eec3f87f1fb588b5ca394da08edb16783f4f76ad896f53e96db77046d9`  
		Last Modified: Tue, 30 Sep 2025 03:38:07 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d605c050bdbc2cbe5986aacfb9b2cb699deefb8e96328a30c5955c8c203558`  
		Last Modified: Tue, 30 Sep 2025 03:38:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbe1a71e963aeda880faa4a8ee1c92f02aaa0f25c2c541d229938263151ae1`  
		Last Modified: Tue, 30 Sep 2025 03:38:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5ab3b23006abd0a4505879bb744524f291c5fd3c47bcda59fe9580e6a52c9451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32239db467b7ac791c5e02a30b39a8e07d1676da3f72023c7a4e7a6e3b6dfdc1`

```dockerfile
```

-	Layers:
	-	`sha256:3c38f4673cb000c49365f7ac225ee6c8d1192d70f464591a2fe210e47b5e129d`  
		Last Modified: Wed, 01 Oct 2025 14:28:19 GMT  
		Size: 2.3 MB (2283480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63450ee822c0556494352d4e2d8a7f3d1aa722f4118a228a8de1dcc441a2d9d`  
		Last Modified: Wed, 01 Oct 2025 14:28:20 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:c0606950b9ddd0b3471e91868591e747d6794e0bf3559f55eba6ebf8ff0c562c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73145576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ab1bbad22e39a2ebc11e610006d2d8ec952c1a9f717f04ed3043c6c8ab584c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd187b5427463256098e233be4d4d03fccba4301a10c8bf73c1b1d07bfbc4305`  
		Last Modified: Tue, 30 Sep 2025 02:27:33 GMT  
		Size: 1.3 MB (1262736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba5754fd04e92aafff5cb6ad7abbb1e1defb4260642169bfbfe164ea4632f4b`  
		Last Modified: Tue, 30 Sep 2025 02:27:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77907aaee8949d54a9d51a6df6d5279b339b37d5e22e0c2146e66e347a21536e`  
		Last Modified: Tue, 30 Sep 2025 01:43:13 GMT  
		Size: 38.0 MB (37990588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec771643eef709f72f374b7d0f416502bb63707d40902ec5ccf83f1d49e6276`  
		Last Modified: Tue, 30 Sep 2025 01:43:05 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaaaef0ea7bb3e3e8bd4610b7207cdfe2b89b7b2f9c0f43a014f8718d67d119`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 5.9 MB (5943720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5f21615138e8a6acbd04d6781d94fc1eb303b8dd95cc6cba825a94f34991e3`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5798e98fbdd0d04752f2cef760bafad88e01c002715aa66cd861aab5d51ca13`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b2b12cd1a6435c07db2ac16401aee26e54c3330ecf16e3c055448ff8a6404b`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c672b12deba689f1e313e24f8a284dc66eaffc97ab4a123901c87093c0f5f4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51235185b4bdc6bef6882a9b4db6f1b13ee1a239a15f817650b50cf2293fbf1`

```dockerfile
```

-	Layers:
	-	`sha256:48baca2e35bba316ac819ece9f88c363ec614e2a505a3ce38c95ef61bb768bad`  
		Last Modified: Tue, 30 Sep 2025 08:28:23 GMT  
		Size: 2.3 MB (2286451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a91c6bbf6731857abf09cffadbdc793585e066ea0e4ab2c605a118b48e1321`  
		Last Modified: Tue, 30 Sep 2025 08:28:23 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:fa5372efcc150d37b61d58d2fb4bc57e68336a0586673fb610000ac8fb894fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70999027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74be42a49de9e5de3bd1b91557e610d4c7ebf00984423c61309fd561c71a51b3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96565be4d07605304ab01ed88ddb2422c09d2c097a7a6bd9e908ecc538bc41b6`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 1.2 MB (1235933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89241ff1b55720625ba104e27a7ae55ed5d7f05f7cc70232c509ad4e8c98a25a`  
		Last Modified: Tue, 16 Sep 2025 17:54:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cfac0646ebc1380322334d36097689728babfc80127206b89b48da79bb9f1`  
		Last Modified: Tue, 16 Sep 2025 17:54:49 GMT  
		Size: 37.9 MB (37857621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2c1c0258f47c00e65e5e3ad5da5d3b1bcb59afa40ef39f4100c885d6657d9`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b56a2fffda99f1ab0d575d5e52c6b0f4c7b50264d9db5ee78ebcd53c86e30b`  
		Last Modified: Tue, 16 Sep 2025 17:58:46 GMT  
		Size: 5.7 MB (5695227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bc3ef11a838c2709f52197e9236fa80e8653bd776830a799d0b5b07d54113f`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a02e348d7bd7bdb8e5edfb92e9813de0ab15af3401b02704182796aa1fc3c3`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77df38f7b9cb8eb82b9ec2076c7a77d698dc0be9e5a99f3ef45ab20f6bd25630`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8be90cff277f6e5259cb7dc07f78955407f6d16f7658d6d0f83c1222d2f26d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcaf75209bfa607e999300d674408dc1dddbd65addd06fe5cc43d1fe5bdff25`

```dockerfile
```

-	Layers:
	-	`sha256:5f6177053b838bc7b86b6c6f85b538ac8b390fa3ae1a2d945d7bbe551076dd61`  
		Last Modified: Tue, 16 Sep 2025 20:28:54 GMT  
		Size: 2.3 MB (2284892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53f76e5d6663876d3dcc1224bf2aeb3421fe3911d5cb12e04419ecaf3532b4e`  
		Last Modified: Tue, 16 Sep 2025 20:28:55 GMT  
		Size: 21.2 KB (21245 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:e95c431a2714327e438149883e695922d8cf022d97ade75c147f570ff8c2c982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79554959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3086967e9567172bf55d2fd1929a0d7a447524ba83996f9cea9ff3702e875eb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34425e9a9c6e82827dc5ccbdc05696ab59c93c6a3f9037bb6cbe805a7f5abde`  
		Last Modified: Tue, 16 Sep 2025 17:07:41 GMT  
		Size: 1.3 MB (1260872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390acc4c37285a6ee478f4264f2ed3d9213800b2014c5e93735666031c27f238`  
		Last Modified: Tue, 16 Sep 2025 17:07:35 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fd0f854246fa6759c30ec6ea097df9bd3949fbdecd97382a03be0640882a4d`  
		Last Modified: Tue, 16 Sep 2025 17:07:40 GMT  
		Size: 42.1 MB (42133523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3945d4c7194481fe1acfb2b5afb156034f860a15810a9f917eeaa6e2d5b0fb`  
		Last Modified: Tue, 16 Sep 2025 17:07:35 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4467e7da74767a8542cd6e78214b46c99561ee2b84ab8babf9d848a29bbe3f49`  
		Last Modified: Tue, 16 Sep 2025 18:00:37 GMT  
		Size: 6.0 MB (6021535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf947b2204e030030adda1718d88f4ce3539cede2b511f6735a9254a0f80f25c`  
		Last Modified: Tue, 16 Sep 2025 18:00:37 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162f8509accfb25aaaa8bfca84a5c9277097f2061f8329ea496e9bc575acade7`  
		Last Modified: Tue, 16 Sep 2025 18:00:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4b74a51b6bcb45b0323031a0b2a1fb36fff506153c9079d9a6f119e561028c`  
		Last Modified: Tue, 16 Sep 2025 18:00:37 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:047f614544522c14535a00ef87467f6886d450ce7243be39b1e62977628ca5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c217d7902a37080ef9dd6e1d8f40018fe99b73a8899d64e32c89a774bda8b64`

```dockerfile
```

-	Layers:
	-	`sha256:d4f551271a41c602eaa7735e6d6d63c8f5286130fed81965bbc8066eef371b82`  
		Last Modified: Tue, 16 Sep 2025 20:28:58 GMT  
		Size: 2.3 MB (2283752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b82f6182d04a9a497cc7d2f862904cc50b8635656e4b5092deba1ffc05a4d6`  
		Last Modified: Tue, 16 Sep 2025 20:28:59 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:5984bbd15c74879813e47b29f8446816454bc045e9f4044949d3868d80bb3aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76346556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb6144e08c32976421d484fc7e6afca57fc07a3fe6b3a7232d29b861868e92`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaebce22a6b2d6988a9332f9c7dc065d9e9f2a7a17e5c301d44f1fe019e9fc2`  
		Last Modified: Tue, 30 Sep 2025 00:45:29 GMT  
		Size: 1.3 MB (1286763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89469d8cb4eed711406676beb42abf83e21c53012c072fbaea75441a2f2a588`  
		Last Modified: Tue, 30 Sep 2025 00:45:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95001c5ad378e24b3da2da7276f7c559b8e94b7584eee54f3056825272023f6c`  
		Last Modified: Tue, 30 Sep 2025 00:45:32 GMT  
		Size: 37.7 MB (37742278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5746ce7240c97031bcab6d9c8dd307f00674605d79719f23ec9df231536ee0b`  
		Last Modified: Tue, 30 Sep 2025 00:45:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ce738fbe72cc62c38a36f7f8b6acfbb30990f17b7292a05225314e1d03befd`  
		Last Modified: Tue, 30 Sep 2025 01:26:07 GMT  
		Size: 6.0 MB (6020590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c7a12c38109dc888fe65b3be1e78ebfe10c75897e7e88a29a53f85c36eb1ac`  
		Last Modified: Tue, 30 Sep 2025 01:26:05 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782fd6568dcd50ab3250ba1420b126be663a698f9de571f283bbc43e98dcb80`  
		Last Modified: Tue, 30 Sep 2025 01:26:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8567c38864ddbfc250029b491f09c707abdae73f7b4ec08c1324c508eebf74ae`  
		Last Modified: Tue, 30 Sep 2025 01:26:06 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fc73784634a0acce9f2232ffb9664bceb5962ffb158c3be7ad1dac17ab5b2073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd5606f84296eed8a6c30857eaa41ac7ebde5e9be715e562a6dede74c37f97b`

```dockerfile
```

-	Layers:
	-	`sha256:1aea84ac7962075608659f62303460c2d7c5fe97a9f63d87e188e19e1d29c731`  
		Last Modified: Wed, 01 Oct 2025 17:28:31 GMT  
		Size: 2.3 MB (2280668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590f9c6fec5755fe9a8da617ed8b62f9963ae37b75b6639c2cc5f04ada96c2d4`  
		Last Modified: Wed, 01 Oct 2025 17:28:32 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8b7c977482113b7d4c3379dbab8ea8bfed0e95e8088d98dd30cfb2aac2c9f2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81053367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4f08759596e3b9e5d7290dfbdfc8e075247f58227efbc547a1dc5030408742`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba702f0f51333fc2712ffc50d66684ef842dd2f30e7e612a7085b6264c7d0c0`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 1.3 MB (1309688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b9bcf1c68a9433fa734e7f77d0062d7271f532391ae56abbef8e2820cf828`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eeb6308e90b8bb2e276d4c0017af677089a878c4fc04021ec60abaf88b633b`  
		Last Modified: Tue, 16 Sep 2025 17:27:49 GMT  
		Size: 39.6 MB (39595821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa59464570e58df18efecb42c30257cdea420248e5b8999bbed0be72c06831`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6774045721abcc7f4299c08bc8dbeda3cb9f3fa72fec4b4eb19dd591a04d6813`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 6.6 MB (6551103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd934fc95d3b2adb5857e2f00983abe8c01018c4e84546953a5f77482d66992`  
		Last Modified: Tue, 16 Sep 2025 18:01:56 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc71cd1ca099ac43138c3be1a95632e82bc0144a52934fe849f86ad270b5a7a`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7fe823656da82cfb8ab46a01f99d1a4ca0687f122ae82a8d4e452e1b20fd9e`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6c93025c0827bfd0d7b4e45dc24e2651898def62a33ed54347f89a5015af19d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03e92a175b411b28ac4407b23a620cb846b039a7656d72f9760a97da6dded42`

```dockerfile
```

-	Layers:
	-	`sha256:bd8a127995092ba84037010e07bf054f2fb51ccfb7c31d1b317e5e2aa323b274`  
		Last Modified: Tue, 16 Sep 2025 20:29:08 GMT  
		Size: 2.3 MB (2287015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99646e9dec58fd128ee6ae948247dfd018b470f6c449c9e956b352abbbab360c`  
		Last Modified: Tue, 16 Sep 2025 20:29:09 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; s390x

```console
$ docker pull fluentd@sha256:e1077d51cf425d916d172165c7e0adc158afdbfbcf5742ff7817babd8fec5cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76824627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323347be19501d30e21197bb58f1458e9a1aa28044755a9d28be61e0b8170168`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70370253f1ce091fe730c380a58bcad6c984318332f9815450f5cfaa70aa87f5`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 1.3 MB (1294292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ec12509a32b107309b0e8ad0dd5f247db0a2ca036489efbfcf07069855b56d`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95e9b1c0885cb28c05fa772e1873d7827da80a057035afb16216bb0e18774ea`  
		Last Modified: Tue, 16 Sep 2025 17:17:57 GMT  
		Size: 39.3 MB (39286986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160aaf92b9681375fe7aaa71ed89f2fa889c9ed589628572f762bc3bde9e15e7`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b20eb585bc1db6ed5ff9536e3f8f84a65a0a753ea5af95fde9d1cfffcea90e`  
		Last Modified: Tue, 16 Sep 2025 17:58:10 GMT  
		Size: 6.4 MB (6408044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a23e9fdec9bdc5545d5ce9e7c776cec3f3a8967d96ef8a15039b8e0c62b5089`  
		Last Modified: Tue, 16 Sep 2025 17:58:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05227e73144ce28d40dbc8ec6e46e37a0d636968a8968df0a54a6dec3c8a31fb`  
		Last Modified: Tue, 16 Sep 2025 17:58:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4096477949e4f1d7d4a4c2fdf49030b44fe4be6c2ca84f6d7300527798af25e`  
		Last Modified: Tue, 16 Sep 2025 17:58:10 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7c98b5fe01dcee58e79906a8cda5ef48240d894adb6159e6890490f3548600d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd6db0e98cfcc6e85267280437a4963dbbc4a2e705f4b755a2baffcdc822b4a`

```dockerfile
```

-	Layers:
	-	`sha256:782a11d83d8a50fd862f7758dbb73b14c5932683d824bf14cd3b5844d177193d`  
		Last Modified: Tue, 16 Sep 2025 20:29:14 GMT  
		Size: 2.3 MB (2284925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796f5926fb2ed48c47aa5a5bd6ed0e0b3e417aadf0957f8e59270058399d4f92`  
		Last Modified: Tue, 16 Sep 2025 20:29:15 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:9fbb4456191a5284d9d2084feb43915c2240e486a3bbdc4872af6013bb321515
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
$ docker pull fluentd@sha256:968450201f1633b5a796a19818797ba95ada90226e3e78d266de7cc447d702de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79258793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec6b9a837666fac5eef40dadfc3140928de04730d4dc0a2d94cb9d914d4a05f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac80cde22bfc7f1283ae07a881aea9b0ddb32e3c1bd62b6dd738c001461ae80c`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 1.3 MB (1279282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04bd217259e9a1adff42a11c482bc4ce95944a28541de67525db69fd74eb2a`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a793530ea8ee5034845d68f5cf20d39e0d069c36c9df258a0617f3a32fd4252`  
		Last Modified: Tue, 30 Sep 2025 00:46:10 GMT  
		Size: 42.2 MB (42153497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7503b4256904558e2f15b3cccab853eec67b0a9eb298954e71634e22152985c`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7718db5a4f479bb9efa051123d43769274727b3f793a5384e9b524fe083ab476`  
		Last Modified: Tue, 30 Sep 2025 03:38:08 GMT  
		Size: 6.0 MB (6045860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633fe0eec3f87f1fb588b5ca394da08edb16783f4f76ad896f53e96db77046d9`  
		Last Modified: Tue, 30 Sep 2025 03:38:07 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d605c050bdbc2cbe5986aacfb9b2cb699deefb8e96328a30c5955c8c203558`  
		Last Modified: Tue, 30 Sep 2025 03:38:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbe1a71e963aeda880faa4a8ee1c92f02aaa0f25c2c541d229938263151ae1`  
		Last Modified: Tue, 30 Sep 2025 03:38:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5ab3b23006abd0a4505879bb744524f291c5fd3c47bcda59fe9580e6a52c9451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32239db467b7ac791c5e02a30b39a8e07d1676da3f72023c7a4e7a6e3b6dfdc1`

```dockerfile
```

-	Layers:
	-	`sha256:3c38f4673cb000c49365f7ac225ee6c8d1192d70f464591a2fe210e47b5e129d`  
		Last Modified: Wed, 01 Oct 2025 14:28:19 GMT  
		Size: 2.3 MB (2283480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63450ee822c0556494352d4e2d8a7f3d1aa722f4118a228a8de1dcc441a2d9d`  
		Last Modified: Wed, 01 Oct 2025 14:28:20 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:c0606950b9ddd0b3471e91868591e747d6794e0bf3559f55eba6ebf8ff0c562c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73145576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ab1bbad22e39a2ebc11e610006d2d8ec952c1a9f717f04ed3043c6c8ab584c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd187b5427463256098e233be4d4d03fccba4301a10c8bf73c1b1d07bfbc4305`  
		Last Modified: Tue, 30 Sep 2025 02:27:33 GMT  
		Size: 1.3 MB (1262736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba5754fd04e92aafff5cb6ad7abbb1e1defb4260642169bfbfe164ea4632f4b`  
		Last Modified: Tue, 30 Sep 2025 02:27:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77907aaee8949d54a9d51a6df6d5279b339b37d5e22e0c2146e66e347a21536e`  
		Last Modified: Tue, 30 Sep 2025 01:43:13 GMT  
		Size: 38.0 MB (37990588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec771643eef709f72f374b7d0f416502bb63707d40902ec5ccf83f1d49e6276`  
		Last Modified: Tue, 30 Sep 2025 01:43:05 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaaaef0ea7bb3e3e8bd4610b7207cdfe2b89b7b2f9c0f43a014f8718d67d119`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 5.9 MB (5943720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5f21615138e8a6acbd04d6781d94fc1eb303b8dd95cc6cba825a94f34991e3`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5798e98fbdd0d04752f2cef760bafad88e01c002715aa66cd861aab5d51ca13`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b2b12cd1a6435c07db2ac16401aee26e54c3330ecf16e3c055448ff8a6404b`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c672b12deba689f1e313e24f8a284dc66eaffc97ab4a123901c87093c0f5f4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51235185b4bdc6bef6882a9b4db6f1b13ee1a239a15f817650b50cf2293fbf1`

```dockerfile
```

-	Layers:
	-	`sha256:48baca2e35bba316ac819ece9f88c363ec614e2a505a3ce38c95ef61bb768bad`  
		Last Modified: Tue, 30 Sep 2025 08:28:23 GMT  
		Size: 2.3 MB (2286451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a91c6bbf6731857abf09cffadbdc793585e066ea0e4ab2c605a118b48e1321`  
		Last Modified: Tue, 30 Sep 2025 08:28:23 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:fa5372efcc150d37b61d58d2fb4bc57e68336a0586673fb610000ac8fb894fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70999027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74be42a49de9e5de3bd1b91557e610d4c7ebf00984423c61309fd561c71a51b3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96565be4d07605304ab01ed88ddb2422c09d2c097a7a6bd9e908ecc538bc41b6`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 1.2 MB (1235933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89241ff1b55720625ba104e27a7ae55ed5d7f05f7cc70232c509ad4e8c98a25a`  
		Last Modified: Tue, 16 Sep 2025 17:54:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cfac0646ebc1380322334d36097689728babfc80127206b89b48da79bb9f1`  
		Last Modified: Tue, 16 Sep 2025 17:54:49 GMT  
		Size: 37.9 MB (37857621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2c1c0258f47c00e65e5e3ad5da5d3b1bcb59afa40ef39f4100c885d6657d9`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b56a2fffda99f1ab0d575d5e52c6b0f4c7b50264d9db5ee78ebcd53c86e30b`  
		Last Modified: Tue, 16 Sep 2025 17:58:46 GMT  
		Size: 5.7 MB (5695227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bc3ef11a838c2709f52197e9236fa80e8653bd776830a799d0b5b07d54113f`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a02e348d7bd7bdb8e5edfb92e9813de0ab15af3401b02704182796aa1fc3c3`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77df38f7b9cb8eb82b9ec2076c7a77d698dc0be9e5a99f3ef45ab20f6bd25630`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:8be90cff277f6e5259cb7dc07f78955407f6d16f7658d6d0f83c1222d2f26d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcaf75209bfa607e999300d674408dc1dddbd65addd06fe5cc43d1fe5bdff25`

```dockerfile
```

-	Layers:
	-	`sha256:5f6177053b838bc7b86b6c6f85b538ac8b390fa3ae1a2d945d7bbe551076dd61`  
		Last Modified: Tue, 16 Sep 2025 20:28:54 GMT  
		Size: 2.3 MB (2284892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53f76e5d6663876d3dcc1224bf2aeb3421fe3911d5cb12e04419ecaf3532b4e`  
		Last Modified: Tue, 16 Sep 2025 20:28:55 GMT  
		Size: 21.2 KB (21245 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:d2817f38ffa33d4de35a4b3797fc7db1eb930922ad165ea94ea514e07e6f855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79570070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b3937a22385f9d20cc74516f05ecebf7d5bc9f435f9112f55b9f6efeff9e23`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb29f9c6264e41391878cf99a87793deb9e28ca3db17c0bb34690c11297d7b5e`  
		Last Modified: Tue, 30 Sep 2025 00:47:23 GMT  
		Size: 1.3 MB (1260907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d195b9d4d6d03f5400fd32517a8bd8799024004cf083065521ce652d94c0d2b`  
		Last Modified: Tue, 30 Sep 2025 00:47:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f98c4e0b0b55d73bd847713bf4ee4962af2c7ffd0f980b4517f7ea00b7813a`  
		Last Modified: Tue, 30 Sep 2025 00:47:28 GMT  
		Size: 42.1 MB (42134245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2afd66200af4a0447310eb0c3f727edde8bc32240cf3343696ff2be5a577ad`  
		Last Modified: Tue, 30 Sep 2025 00:47:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a76ee738741e03869e456b0d29876ce0849f753da0c0375f6ce0b4b4cc46f0`  
		Last Modified: Tue, 30 Sep 2025 01:27:10 GMT  
		Size: 6.0 MB (6031686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0c6fa04b416ec7a8061ee5c017353b32ef8bace667d7d6aa062cd922dc5586`  
		Last Modified: Tue, 30 Sep 2025 01:27:10 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d6b5bab627da920964e3d12dd14eec3a2be4d11f72d4c500adb251443e35a2`  
		Last Modified: Tue, 30 Sep 2025 01:27:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b370b91e4389e4eac093d062fa8b43eef2d70af8311005e9b550556724dd6616`  
		Last Modified: Tue, 30 Sep 2025 01:27:11 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:42241076c4d8096f711808879d86e2c81c16de8af703c1e31708970ed4396eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3413fbfd0cf5a9ca3c27ceb81851854346a5523a7d1c3667eb561b1413d2d4d6`

```dockerfile
```

-	Layers:
	-	`sha256:889914816a72d49ec22c8ab729b9ee3cfc0c516d0d82ae1655738753152445d1`  
		Last Modified: Wed, 01 Oct 2025 11:35:05 GMT  
		Size: 2.3 MB (2283752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353fc631c01d1267fcf942cba3cd764d7f92535bebc5695105f881e9e0816b60`  
		Last Modified: Wed, 01 Oct 2025 11:35:05 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:5984bbd15c74879813e47b29f8446816454bc045e9f4044949d3868d80bb3aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76346556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb6144e08c32976421d484fc7e6afca57fc07a3fe6b3a7232d29b861868e92`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaebce22a6b2d6988a9332f9c7dc065d9e9f2a7a17e5c301d44f1fe019e9fc2`  
		Last Modified: Tue, 30 Sep 2025 00:45:29 GMT  
		Size: 1.3 MB (1286763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89469d8cb4eed711406676beb42abf83e21c53012c072fbaea75441a2f2a588`  
		Last Modified: Tue, 30 Sep 2025 00:45:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95001c5ad378e24b3da2da7276f7c559b8e94b7584eee54f3056825272023f6c`  
		Last Modified: Tue, 30 Sep 2025 00:45:32 GMT  
		Size: 37.7 MB (37742278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5746ce7240c97031bcab6d9c8dd307f00674605d79719f23ec9df231536ee0b`  
		Last Modified: Tue, 30 Sep 2025 00:45:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ce738fbe72cc62c38a36f7f8b6acfbb30990f17b7292a05225314e1d03befd`  
		Last Modified: Tue, 30 Sep 2025 01:26:07 GMT  
		Size: 6.0 MB (6020590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c7a12c38109dc888fe65b3be1e78ebfe10c75897e7e88a29a53f85c36eb1ac`  
		Last Modified: Tue, 30 Sep 2025 01:26:05 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782fd6568dcd50ab3250ba1420b126be663a698f9de571f283bbc43e98dcb80`  
		Last Modified: Tue, 30 Sep 2025 01:26:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8567c38864ddbfc250029b491f09c707abdae73f7b4ec08c1324c508eebf74ae`  
		Last Modified: Tue, 30 Sep 2025 01:26:06 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:fc73784634a0acce9f2232ffb9664bceb5962ffb158c3be7ad1dac17ab5b2073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd5606f84296eed8a6c30857eaa41ac7ebde5e9be715e562a6dede74c37f97b`

```dockerfile
```

-	Layers:
	-	`sha256:1aea84ac7962075608659f62303460c2d7c5fe97a9f63d87e188e19e1d29c731`  
		Last Modified: Wed, 01 Oct 2025 17:28:31 GMT  
		Size: 2.3 MB (2280668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590f9c6fec5755fe9a8da617ed8b62f9963ae37b75b6639c2cc5f04ada96c2d4`  
		Last Modified: Wed, 01 Oct 2025 17:28:32 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8b7c977482113b7d4c3379dbab8ea8bfed0e95e8088d98dd30cfb2aac2c9f2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81053367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4f08759596e3b9e5d7290dfbdfc8e075247f58227efbc547a1dc5030408742`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba702f0f51333fc2712ffc50d66684ef842dd2f30e7e612a7085b6264c7d0c0`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 1.3 MB (1309688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b9bcf1c68a9433fa734e7f77d0062d7271f532391ae56abbef8e2820cf828`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eeb6308e90b8bb2e276d4c0017af677089a878c4fc04021ec60abaf88b633b`  
		Last Modified: Tue, 16 Sep 2025 17:27:49 GMT  
		Size: 39.6 MB (39595821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa59464570e58df18efecb42c30257cdea420248e5b8999bbed0be72c06831`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6774045721abcc7f4299c08bc8dbeda3cb9f3fa72fec4b4eb19dd591a04d6813`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 6.6 MB (6551103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd934fc95d3b2adb5857e2f00983abe8c01018c4e84546953a5f77482d66992`  
		Last Modified: Tue, 16 Sep 2025 18:01:56 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc71cd1ca099ac43138c3be1a95632e82bc0144a52934fe849f86ad270b5a7a`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7fe823656da82cfb8ab46a01f99d1a4ca0687f122ae82a8d4e452e1b20fd9e`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:6c93025c0827bfd0d7b4e45dc24e2651898def62a33ed54347f89a5015af19d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03e92a175b411b28ac4407b23a620cb846b039a7656d72f9760a97da6dded42`

```dockerfile
```

-	Layers:
	-	`sha256:bd8a127995092ba84037010e07bf054f2fb51ccfb7c31d1b317e5e2aa323b274`  
		Last Modified: Tue, 16 Sep 2025 20:29:08 GMT  
		Size: 2.3 MB (2287015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99646e9dec58fd128ee6ae948247dfd018b470f6c449c9e956b352abbbab360c`  
		Last Modified: Tue, 16 Sep 2025 20:29:09 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:e1077d51cf425d916d172165c7e0adc158afdbfbcf5742ff7817babd8fec5cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76824627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323347be19501d30e21197bb58f1458e9a1aa28044755a9d28be61e0b8170168`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70370253f1ce091fe730c380a58bcad6c984318332f9815450f5cfaa70aa87f5`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 1.3 MB (1294292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ec12509a32b107309b0e8ad0dd5f247db0a2ca036489efbfcf07069855b56d`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95e9b1c0885cb28c05fa772e1873d7827da80a057035afb16216bb0e18774ea`  
		Last Modified: Tue, 16 Sep 2025 17:17:57 GMT  
		Size: 39.3 MB (39286986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160aaf92b9681375fe7aaa71ed89f2fa889c9ed589628572f762bc3bde9e15e7`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b20eb585bc1db6ed5ff9536e3f8f84a65a0a753ea5af95fde9d1cfffcea90e`  
		Last Modified: Tue, 16 Sep 2025 17:58:10 GMT  
		Size: 6.4 MB (6408044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a23e9fdec9bdc5545d5ce9e7c776cec3f3a8967d96ef8a15039b8e0c62b5089`  
		Last Modified: Tue, 16 Sep 2025 17:58:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05227e73144ce28d40dbc8ec6e46e37a0d636968a8968df0a54a6dec3c8a31fb`  
		Last Modified: Tue, 16 Sep 2025 17:58:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4096477949e4f1d7d4a4c2fdf49030b44fe4be6c2ca84f6d7300527798af25e`  
		Last Modified: Tue, 16 Sep 2025 17:58:10 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7c98b5fe01dcee58e79906a8cda5ef48240d894adb6159e6890490f3548600d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd6db0e98cfcc6e85267280437a4963dbbc4a2e705f4b755a2baffcdc822b4a`

```dockerfile
```

-	Layers:
	-	`sha256:782a11d83d8a50fd862f7758dbb73b14c5932683d824bf14cd3b5844d177193d`  
		Last Modified: Tue, 16 Sep 2025 20:29:14 GMT  
		Size: 2.3 MB (2284925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796f5926fb2ed48c47aa5a5bd6ed0e0b3e417aadf0957f8e59270058399d4f92`  
		Last Modified: Tue, 16 Sep 2025 20:29:15 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.0-1.0`

```console
$ docker pull fluentd@sha256:8f6b1cf9675279a4472112886e8ecbafaaffcbef27919879b83bca67aa156475
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
$ docker pull fluentd@sha256:968450201f1633b5a796a19818797ba95ada90226e3e78d266de7cc447d702de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79258793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec6b9a837666fac5eef40dadfc3140928de04730d4dc0a2d94cb9d914d4a05f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac80cde22bfc7f1283ae07a881aea9b0ddb32e3c1bd62b6dd738c001461ae80c`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 1.3 MB (1279282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04bd217259e9a1adff42a11c482bc4ce95944a28541de67525db69fd74eb2a`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a793530ea8ee5034845d68f5cf20d39e0d069c36c9df258a0617f3a32fd4252`  
		Last Modified: Tue, 30 Sep 2025 00:46:10 GMT  
		Size: 42.2 MB (42153497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7503b4256904558e2f15b3cccab853eec67b0a9eb298954e71634e22152985c`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7718db5a4f479bb9efa051123d43769274727b3f793a5384e9b524fe083ab476`  
		Last Modified: Tue, 30 Sep 2025 03:38:08 GMT  
		Size: 6.0 MB (6045860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633fe0eec3f87f1fb588b5ca394da08edb16783f4f76ad896f53e96db77046d9`  
		Last Modified: Tue, 30 Sep 2025 03:38:07 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d605c050bdbc2cbe5986aacfb9b2cb699deefb8e96328a30c5955c8c203558`  
		Last Modified: Tue, 30 Sep 2025 03:38:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbe1a71e963aeda880faa4a8ee1c92f02aaa0f25c2c541d229938263151ae1`  
		Last Modified: Tue, 30 Sep 2025 03:38:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5ab3b23006abd0a4505879bb744524f291c5fd3c47bcda59fe9580e6a52c9451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32239db467b7ac791c5e02a30b39a8e07d1676da3f72023c7a4e7a6e3b6dfdc1`

```dockerfile
```

-	Layers:
	-	`sha256:3c38f4673cb000c49365f7ac225ee6c8d1192d70f464591a2fe210e47b5e129d`  
		Last Modified: Wed, 01 Oct 2025 14:28:19 GMT  
		Size: 2.3 MB (2283480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63450ee822c0556494352d4e2d8a7f3d1aa722f4118a228a8de1dcc441a2d9d`  
		Last Modified: Wed, 01 Oct 2025 14:28:20 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:c0606950b9ddd0b3471e91868591e747d6794e0bf3559f55eba6ebf8ff0c562c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73145576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ab1bbad22e39a2ebc11e610006d2d8ec952c1a9f717f04ed3043c6c8ab584c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd187b5427463256098e233be4d4d03fccba4301a10c8bf73c1b1d07bfbc4305`  
		Last Modified: Tue, 30 Sep 2025 02:27:33 GMT  
		Size: 1.3 MB (1262736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba5754fd04e92aafff5cb6ad7abbb1e1defb4260642169bfbfe164ea4632f4b`  
		Last Modified: Tue, 30 Sep 2025 02:27:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77907aaee8949d54a9d51a6df6d5279b339b37d5e22e0c2146e66e347a21536e`  
		Last Modified: Tue, 30 Sep 2025 01:43:13 GMT  
		Size: 38.0 MB (37990588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec771643eef709f72f374b7d0f416502bb63707d40902ec5ccf83f1d49e6276`  
		Last Modified: Tue, 30 Sep 2025 01:43:05 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaaaef0ea7bb3e3e8bd4610b7207cdfe2b89b7b2f9c0f43a014f8718d67d119`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 5.9 MB (5943720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5f21615138e8a6acbd04d6781d94fc1eb303b8dd95cc6cba825a94f34991e3`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5798e98fbdd0d04752f2cef760bafad88e01c002715aa66cd861aab5d51ca13`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b2b12cd1a6435c07db2ac16401aee26e54c3330ecf16e3c055448ff8a6404b`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c672b12deba689f1e313e24f8a284dc66eaffc97ab4a123901c87093c0f5f4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51235185b4bdc6bef6882a9b4db6f1b13ee1a239a15f817650b50cf2293fbf1`

```dockerfile
```

-	Layers:
	-	`sha256:48baca2e35bba316ac819ece9f88c363ec614e2a505a3ce38c95ef61bb768bad`  
		Last Modified: Tue, 30 Sep 2025 08:28:23 GMT  
		Size: 2.3 MB (2286451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a91c6bbf6731857abf09cffadbdc793585e066ea0e4ab2c605a118b48e1321`  
		Last Modified: Tue, 30 Sep 2025 08:28:23 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:fa5372efcc150d37b61d58d2fb4bc57e68336a0586673fb610000ac8fb894fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70999027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74be42a49de9e5de3bd1b91557e610d4c7ebf00984423c61309fd561c71a51b3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96565be4d07605304ab01ed88ddb2422c09d2c097a7a6bd9e908ecc538bc41b6`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 1.2 MB (1235933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89241ff1b55720625ba104e27a7ae55ed5d7f05f7cc70232c509ad4e8c98a25a`  
		Last Modified: Tue, 16 Sep 2025 17:54:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cfac0646ebc1380322334d36097689728babfc80127206b89b48da79bb9f1`  
		Last Modified: Tue, 16 Sep 2025 17:54:49 GMT  
		Size: 37.9 MB (37857621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2c1c0258f47c00e65e5e3ad5da5d3b1bcb59afa40ef39f4100c885d6657d9`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b56a2fffda99f1ab0d575d5e52c6b0f4c7b50264d9db5ee78ebcd53c86e30b`  
		Last Modified: Tue, 16 Sep 2025 17:58:46 GMT  
		Size: 5.7 MB (5695227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bc3ef11a838c2709f52197e9236fa80e8653bd776830a799d0b5b07d54113f`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a02e348d7bd7bdb8e5edfb92e9813de0ab15af3401b02704182796aa1fc3c3`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77df38f7b9cb8eb82b9ec2076c7a77d698dc0be9e5a99f3ef45ab20f6bd25630`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8be90cff277f6e5259cb7dc07f78955407f6d16f7658d6d0f83c1222d2f26d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcaf75209bfa607e999300d674408dc1dddbd65addd06fe5cc43d1fe5bdff25`

```dockerfile
```

-	Layers:
	-	`sha256:5f6177053b838bc7b86b6c6f85b538ac8b390fa3ae1a2d945d7bbe551076dd61`  
		Last Modified: Tue, 16 Sep 2025 20:28:54 GMT  
		Size: 2.3 MB (2284892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53f76e5d6663876d3dcc1224bf2aeb3421fe3911d5cb12e04419ecaf3532b4e`  
		Last Modified: Tue, 16 Sep 2025 20:28:55 GMT  
		Size: 21.2 KB (21245 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:e95c431a2714327e438149883e695922d8cf022d97ade75c147f570ff8c2c982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79554959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3086967e9567172bf55d2fd1929a0d7a447524ba83996f9cea9ff3702e875eb`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34425e9a9c6e82827dc5ccbdc05696ab59c93c6a3f9037bb6cbe805a7f5abde`  
		Last Modified: Tue, 16 Sep 2025 17:07:41 GMT  
		Size: 1.3 MB (1260872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390acc4c37285a6ee478f4264f2ed3d9213800b2014c5e93735666031c27f238`  
		Last Modified: Tue, 16 Sep 2025 17:07:35 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fd0f854246fa6759c30ec6ea097df9bd3949fbdecd97382a03be0640882a4d`  
		Last Modified: Tue, 16 Sep 2025 17:07:40 GMT  
		Size: 42.1 MB (42133523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3945d4c7194481fe1acfb2b5afb156034f860a15810a9f917eeaa6e2d5b0fb`  
		Last Modified: Tue, 16 Sep 2025 17:07:35 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4467e7da74767a8542cd6e78214b46c99561ee2b84ab8babf9d848a29bbe3f49`  
		Last Modified: Tue, 16 Sep 2025 18:00:37 GMT  
		Size: 6.0 MB (6021535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf947b2204e030030adda1718d88f4ce3539cede2b511f6735a9254a0f80f25c`  
		Last Modified: Tue, 16 Sep 2025 18:00:37 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162f8509accfb25aaaa8bfca84a5c9277097f2061f8329ea496e9bc575acade7`  
		Last Modified: Tue, 16 Sep 2025 18:00:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db4b74a51b6bcb45b0323031a0b2a1fb36fff506153c9079d9a6f119e561028c`  
		Last Modified: Tue, 16 Sep 2025 18:00:37 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:047f614544522c14535a00ef87467f6886d450ce7243be39b1e62977628ca5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c217d7902a37080ef9dd6e1d8f40018fe99b73a8899d64e32c89a774bda8b64`

```dockerfile
```

-	Layers:
	-	`sha256:d4f551271a41c602eaa7735e6d6d63c8f5286130fed81965bbc8066eef371b82`  
		Last Modified: Tue, 16 Sep 2025 20:28:58 GMT  
		Size: 2.3 MB (2283752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b82f6182d04a9a497cc7d2f862904cc50b8635656e4b5092deba1ffc05a4d6`  
		Last Modified: Tue, 16 Sep 2025 20:28:59 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:5984bbd15c74879813e47b29f8446816454bc045e9f4044949d3868d80bb3aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76346556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb6144e08c32976421d484fc7e6afca57fc07a3fe6b3a7232d29b861868e92`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaebce22a6b2d6988a9332f9c7dc065d9e9f2a7a17e5c301d44f1fe019e9fc2`  
		Last Modified: Tue, 30 Sep 2025 00:45:29 GMT  
		Size: 1.3 MB (1286763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89469d8cb4eed711406676beb42abf83e21c53012c072fbaea75441a2f2a588`  
		Last Modified: Tue, 30 Sep 2025 00:45:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95001c5ad378e24b3da2da7276f7c559b8e94b7584eee54f3056825272023f6c`  
		Last Modified: Tue, 30 Sep 2025 00:45:32 GMT  
		Size: 37.7 MB (37742278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5746ce7240c97031bcab6d9c8dd307f00674605d79719f23ec9df231536ee0b`  
		Last Modified: Tue, 30 Sep 2025 00:45:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ce738fbe72cc62c38a36f7f8b6acfbb30990f17b7292a05225314e1d03befd`  
		Last Modified: Tue, 30 Sep 2025 01:26:07 GMT  
		Size: 6.0 MB (6020590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c7a12c38109dc888fe65b3be1e78ebfe10c75897e7e88a29a53f85c36eb1ac`  
		Last Modified: Tue, 30 Sep 2025 01:26:05 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782fd6568dcd50ab3250ba1420b126be663a698f9de571f283bbc43e98dcb80`  
		Last Modified: Tue, 30 Sep 2025 01:26:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8567c38864ddbfc250029b491f09c707abdae73f7b4ec08c1324c508eebf74ae`  
		Last Modified: Tue, 30 Sep 2025 01:26:06 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fc73784634a0acce9f2232ffb9664bceb5962ffb158c3be7ad1dac17ab5b2073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd5606f84296eed8a6c30857eaa41ac7ebde5e9be715e562a6dede74c37f97b`

```dockerfile
```

-	Layers:
	-	`sha256:1aea84ac7962075608659f62303460c2d7c5fe97a9f63d87e188e19e1d29c731`  
		Last Modified: Wed, 01 Oct 2025 17:28:31 GMT  
		Size: 2.3 MB (2280668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590f9c6fec5755fe9a8da617ed8b62f9963ae37b75b6639c2cc5f04ada96c2d4`  
		Last Modified: Wed, 01 Oct 2025 17:28:32 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8b7c977482113b7d4c3379dbab8ea8bfed0e95e8088d98dd30cfb2aac2c9f2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81053367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4f08759596e3b9e5d7290dfbdfc8e075247f58227efbc547a1dc5030408742`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba702f0f51333fc2712ffc50d66684ef842dd2f30e7e612a7085b6264c7d0c0`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 1.3 MB (1309688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b9bcf1c68a9433fa734e7f77d0062d7271f532391ae56abbef8e2820cf828`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eeb6308e90b8bb2e276d4c0017af677089a878c4fc04021ec60abaf88b633b`  
		Last Modified: Tue, 16 Sep 2025 17:27:49 GMT  
		Size: 39.6 MB (39595821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa59464570e58df18efecb42c30257cdea420248e5b8999bbed0be72c06831`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6774045721abcc7f4299c08bc8dbeda3cb9f3fa72fec4b4eb19dd591a04d6813`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 6.6 MB (6551103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd934fc95d3b2adb5857e2f00983abe8c01018c4e84546953a5f77482d66992`  
		Last Modified: Tue, 16 Sep 2025 18:01:56 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc71cd1ca099ac43138c3be1a95632e82bc0144a52934fe849f86ad270b5a7a`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7fe823656da82cfb8ab46a01f99d1a4ca0687f122ae82a8d4e452e1b20fd9e`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6c93025c0827bfd0d7b4e45dc24e2651898def62a33ed54347f89a5015af19d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03e92a175b411b28ac4407b23a620cb846b039a7656d72f9760a97da6dded42`

```dockerfile
```

-	Layers:
	-	`sha256:bd8a127995092ba84037010e07bf054f2fb51ccfb7c31d1b317e5e2aa323b274`  
		Last Modified: Tue, 16 Sep 2025 20:29:08 GMT  
		Size: 2.3 MB (2287015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99646e9dec58fd128ee6ae948247dfd018b470f6c449c9e956b352abbbab360c`  
		Last Modified: Tue, 16 Sep 2025 20:29:09 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:e1077d51cf425d916d172165c7e0adc158afdbfbcf5742ff7817babd8fec5cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76824627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323347be19501d30e21197bb58f1458e9a1aa28044755a9d28be61e0b8170168`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70370253f1ce091fe730c380a58bcad6c984318332f9815450f5cfaa70aa87f5`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 1.3 MB (1294292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ec12509a32b107309b0e8ad0dd5f247db0a2ca036489efbfcf07069855b56d`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95e9b1c0885cb28c05fa772e1873d7827da80a057035afb16216bb0e18774ea`  
		Last Modified: Tue, 16 Sep 2025 17:17:57 GMT  
		Size: 39.3 MB (39286986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160aaf92b9681375fe7aaa71ed89f2fa889c9ed589628572f762bc3bde9e15e7`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b20eb585bc1db6ed5ff9536e3f8f84a65a0a753ea5af95fde9d1cfffcea90e`  
		Last Modified: Tue, 16 Sep 2025 17:58:10 GMT  
		Size: 6.4 MB (6408044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a23e9fdec9bdc5545d5ce9e7c776cec3f3a8967d96ef8a15039b8e0c62b5089`  
		Last Modified: Tue, 16 Sep 2025 17:58:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05227e73144ce28d40dbc8ec6e46e37a0d636968a8968df0a54a6dec3c8a31fb`  
		Last Modified: Tue, 16 Sep 2025 17:58:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4096477949e4f1d7d4a4c2fdf49030b44fe4be6c2ca84f6d7300527798af25e`  
		Last Modified: Tue, 16 Sep 2025 17:58:10 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7c98b5fe01dcee58e79906a8cda5ef48240d894adb6159e6890490f3548600d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd6db0e98cfcc6e85267280437a4963dbbc4a2e705f4b755a2baffcdc822b4a`

```dockerfile
```

-	Layers:
	-	`sha256:782a11d83d8a50fd862f7758dbb73b14c5932683d824bf14cd3b5844d177193d`  
		Last Modified: Tue, 16 Sep 2025 20:29:14 GMT  
		Size: 2.3 MB (2284925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796f5926fb2ed48c47aa5a5bd6ed0e0b3e417aadf0957f8e59270058399d4f92`  
		Last Modified: Tue, 16 Sep 2025 20:29:15 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.0-debian-1.0`

```console
$ docker pull fluentd@sha256:9fbb4456191a5284d9d2084feb43915c2240e486a3bbdc4872af6013bb321515
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

### `fluentd:v1.19.0-debian-1.0` - linux; amd64

```console
$ docker pull fluentd@sha256:968450201f1633b5a796a19818797ba95ada90226e3e78d266de7cc447d702de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.3 MB (79258793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec6b9a837666fac5eef40dadfc3140928de04730d4dc0a2d94cb9d914d4a05f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac80cde22bfc7f1283ae07a881aea9b0ddb32e3c1bd62b6dd738c001461ae80c`  
		Last Modified: Tue, 30 Sep 2025 00:46:08 GMT  
		Size: 1.3 MB (1279282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf04bd217259e9a1adff42a11c482bc4ce95944a28541de67525db69fd74eb2a`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a793530ea8ee5034845d68f5cf20d39e0d069c36c9df258a0617f3a32fd4252`  
		Last Modified: Tue, 30 Sep 2025 00:46:10 GMT  
		Size: 42.2 MB (42153497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7503b4256904558e2f15b3cccab853eec67b0a9eb298954e71634e22152985c`  
		Last Modified: Tue, 30 Sep 2025 00:46:07 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7718db5a4f479bb9efa051123d43769274727b3f793a5384e9b524fe083ab476`  
		Last Modified: Tue, 30 Sep 2025 03:38:08 GMT  
		Size: 6.0 MB (6045860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633fe0eec3f87f1fb588b5ca394da08edb16783f4f76ad896f53e96db77046d9`  
		Last Modified: Tue, 30 Sep 2025 03:38:07 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d605c050bdbc2cbe5986aacfb9b2cb699deefb8e96328a30c5955c8c203558`  
		Last Modified: Tue, 30 Sep 2025 03:38:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cbe1a71e963aeda880faa4a8ee1c92f02aaa0f25c2c541d229938263151ae1`  
		Last Modified: Tue, 30 Sep 2025 03:38:08 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5ab3b23006abd0a4505879bb744524f291c5fd3c47bcda59fe9580e6a52c9451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32239db467b7ac791c5e02a30b39a8e07d1676da3f72023c7a4e7a6e3b6dfdc1`

```dockerfile
```

-	Layers:
	-	`sha256:3c38f4673cb000c49365f7ac225ee6c8d1192d70f464591a2fe210e47b5e129d`  
		Last Modified: Wed, 01 Oct 2025 14:28:19 GMT  
		Size: 2.3 MB (2283480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e63450ee822c0556494352d4e2d8a7f3d1aa722f4118a228a8de1dcc441a2d9d`  
		Last Modified: Wed, 01 Oct 2025 14:28:20 GMT  
		Size: 21.1 KB (21144 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:c0606950b9ddd0b3471e91868591e747d6794e0bf3559f55eba6ebf8ff0c562c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73145576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ab1bbad22e39a2ebc11e610006d2d8ec952c1a9f717f04ed3043c6c8ab584c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d2a243ecf382412941b4d6772dba911a8093cf3703c933872fbb7ecc21e27e20`  
		Last Modified: Mon, 29 Sep 2025 23:34:24 GMT  
		Size: 27.9 MB (27946145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd187b5427463256098e233be4d4d03fccba4301a10c8bf73c1b1d07bfbc4305`  
		Last Modified: Tue, 30 Sep 2025 02:27:33 GMT  
		Size: 1.3 MB (1262736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba5754fd04e92aafff5cb6ad7abbb1e1defb4260642169bfbfe164ea4632f4b`  
		Last Modified: Tue, 30 Sep 2025 02:27:32 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77907aaee8949d54a9d51a6df6d5279b339b37d5e22e0c2146e66e347a21536e`  
		Last Modified: Tue, 30 Sep 2025 01:43:13 GMT  
		Size: 38.0 MB (37990588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec771643eef709f72f374b7d0f416502bb63707d40902ec5ccf83f1d49e6276`  
		Last Modified: Tue, 30 Sep 2025 01:43:05 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaaaef0ea7bb3e3e8bd4610b7207cdfe2b89b7b2f9c0f43a014f8718d67d119`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 5.9 MB (5943720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5f21615138e8a6acbd04d6781d94fc1eb303b8dd95cc6cba825a94f34991e3`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5798e98fbdd0d04752f2cef760bafad88e01c002715aa66cd861aab5d51ca13`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b2b12cd1a6435c07db2ac16401aee26e54c3330ecf16e3c055448ff8a6404b`  
		Last Modified: Tue, 30 Sep 2025 03:07:03 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c672b12deba689f1e313e24f8a284dc66eaffc97ab4a123901c87093c0f5f4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51235185b4bdc6bef6882a9b4db6f1b13ee1a239a15f817650b50cf2293fbf1`

```dockerfile
```

-	Layers:
	-	`sha256:48baca2e35bba316ac819ece9f88c363ec614e2a505a3ce38c95ef61bb768bad`  
		Last Modified: Tue, 30 Sep 2025 08:28:23 GMT  
		Size: 2.3 MB (2286451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a91c6bbf6731857abf09cffadbdc793585e066ea0e4ab2c605a118b48e1321`  
		Last Modified: Tue, 30 Sep 2025 08:28:23 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:fa5372efcc150d37b61d58d2fb4bc57e68336a0586673fb610000ac8fb894fc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70999027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74be42a49de9e5de3bd1b91557e610d4c7ebf00984423c61309fd561c71a51b3`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96565be4d07605304ab01ed88ddb2422c09d2c097a7a6bd9e908ecc538bc41b6`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 1.2 MB (1235933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89241ff1b55720625ba104e27a7ae55ed5d7f05f7cc70232c509ad4e8c98a25a`  
		Last Modified: Tue, 16 Sep 2025 17:54:45 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16cfac0646ebc1380322334d36097689728babfc80127206b89b48da79bb9f1`  
		Last Modified: Tue, 16 Sep 2025 17:54:49 GMT  
		Size: 37.9 MB (37857621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f2c1c0258f47c00e65e5e3ad5da5d3b1bcb59afa40ef39f4100c885d6657d9`  
		Last Modified: Tue, 16 Sep 2025 17:54:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b56a2fffda99f1ab0d575d5e52c6b0f4c7b50264d9db5ee78ebcd53c86e30b`  
		Last Modified: Tue, 16 Sep 2025 17:58:46 GMT  
		Size: 5.7 MB (5695227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bc3ef11a838c2709f52197e9236fa80e8653bd776830a799d0b5b07d54113f`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a02e348d7bd7bdb8e5edfb92e9813de0ab15af3401b02704182796aa1fc3c3`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77df38f7b9cb8eb82b9ec2076c7a77d698dc0be9e5a99f3ef45ab20f6bd25630`  
		Last Modified: Tue, 16 Sep 2025 17:58:45 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:8be90cff277f6e5259cb7dc07f78955407f6d16f7658d6d0f83c1222d2f26d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcaf75209bfa607e999300d674408dc1dddbd65addd06fe5cc43d1fe5bdff25`

```dockerfile
```

-	Layers:
	-	`sha256:5f6177053b838bc7b86b6c6f85b538ac8b390fa3ae1a2d945d7bbe551076dd61`  
		Last Modified: Tue, 16 Sep 2025 20:28:54 GMT  
		Size: 2.3 MB (2284892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a53f76e5d6663876d3dcc1224bf2aeb3421fe3911d5cb12e04419ecaf3532b4e`  
		Last Modified: Tue, 16 Sep 2025 20:28:55 GMT  
		Size: 21.2 KB (21245 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:d2817f38ffa33d4de35a4b3797fc7db1eb930922ad165ea94ea514e07e6f855a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79570070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b3937a22385f9d20cc74516f05ecebf7d5bc9f435f9112f55b9f6efeff9e23`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb29f9c6264e41391878cf99a87793deb9e28ca3db17c0bb34690c11297d7b5e`  
		Last Modified: Tue, 30 Sep 2025 00:47:23 GMT  
		Size: 1.3 MB (1260907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d195b9d4d6d03f5400fd32517a8bd8799024004cf083065521ce652d94c0d2b`  
		Last Modified: Tue, 30 Sep 2025 00:47:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f98c4e0b0b55d73bd847713bf4ee4962af2c7ffd0f980b4517f7ea00b7813a`  
		Last Modified: Tue, 30 Sep 2025 00:47:28 GMT  
		Size: 42.1 MB (42134245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2afd66200af4a0447310eb0c3f727edde8bc32240cf3343696ff2be5a577ad`  
		Last Modified: Tue, 30 Sep 2025 00:47:25 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a76ee738741e03869e456b0d29876ce0849f753da0c0375f6ce0b4b4cc46f0`  
		Last Modified: Tue, 30 Sep 2025 01:27:10 GMT  
		Size: 6.0 MB (6031686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0c6fa04b416ec7a8061ee5c017353b32ef8bace667d7d6aa062cd922dc5586`  
		Last Modified: Tue, 30 Sep 2025 01:27:10 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d6b5bab627da920964e3d12dd14eec3a2be4d11f72d4c500adb251443e35a2`  
		Last Modified: Tue, 30 Sep 2025 01:27:11 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b370b91e4389e4eac093d062fa8b43eef2d70af8311005e9b550556724dd6616`  
		Last Modified: Tue, 30 Sep 2025 01:27:11 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:42241076c4d8096f711808879d86e2c81c16de8af703c1e31708970ed4396eac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3413fbfd0cf5a9ca3c27ceb81851854346a5523a7d1c3667eb561b1413d2d4d6`

```dockerfile
```

-	Layers:
	-	`sha256:889914816a72d49ec22c8ab729b9ee3cfc0c516d0d82ae1655738753152445d1`  
		Last Modified: Wed, 01 Oct 2025 11:35:05 GMT  
		Size: 2.3 MB (2283752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:353fc631c01d1267fcf942cba3cd764d7f92535bebc5695105f881e9e0816b60`  
		Last Modified: Wed, 01 Oct 2025 11:35:05 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:5984bbd15c74879813e47b29f8446816454bc045e9f4044949d3868d80bb3aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76346556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb6144e08c32976421d484fc7e6afca57fc07a3fe6b3a7232d29b861868e92`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ab4c7760f4a4bda4b0797f3f0b56bd90b9778b76fc8351f2e1bd7c332b9dcc92`  
		Last Modified: Mon, 29 Sep 2025 23:35:33 GMT  
		Size: 31.3 MB (31294536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaebce22a6b2d6988a9332f9c7dc065d9e9f2a7a17e5c301d44f1fe019e9fc2`  
		Last Modified: Tue, 30 Sep 2025 00:45:29 GMT  
		Size: 1.3 MB (1286763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89469d8cb4eed711406676beb42abf83e21c53012c072fbaea75441a2f2a588`  
		Last Modified: Tue, 30 Sep 2025 00:45:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95001c5ad378e24b3da2da7276f7c559b8e94b7584eee54f3056825272023f6c`  
		Last Modified: Tue, 30 Sep 2025 00:45:32 GMT  
		Size: 37.7 MB (37742278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5746ce7240c97031bcab6d9c8dd307f00674605d79719f23ec9df231536ee0b`  
		Last Modified: Tue, 30 Sep 2025 00:45:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ce738fbe72cc62c38a36f7f8b6acfbb30990f17b7292a05225314e1d03befd`  
		Last Modified: Tue, 30 Sep 2025 01:26:07 GMT  
		Size: 6.0 MB (6020590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c7a12c38109dc888fe65b3be1e78ebfe10c75897e7e88a29a53f85c36eb1ac`  
		Last Modified: Tue, 30 Sep 2025 01:26:05 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e782fd6568dcd50ab3250ba1420b126be663a698f9de571f283bbc43e98dcb80`  
		Last Modified: Tue, 30 Sep 2025 01:26:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8567c38864ddbfc250029b491f09c707abdae73f7b4ec08c1324c508eebf74ae`  
		Last Modified: Tue, 30 Sep 2025 01:26:06 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:fc73784634a0acce9f2232ffb9664bceb5962ffb158c3be7ad1dac17ab5b2073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fd5606f84296eed8a6c30857eaa41ac7ebde5e9be715e562a6dede74c37f97b`

```dockerfile
```

-	Layers:
	-	`sha256:1aea84ac7962075608659f62303460c2d7c5fe97a9f63d87e188e19e1d29c731`  
		Last Modified: Wed, 01 Oct 2025 17:28:31 GMT  
		Size: 2.3 MB (2280668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590f9c6fec5755fe9a8da617ed8b62f9963ae37b75b6639c2cc5f04ada96c2d4`  
		Last Modified: Wed, 01 Oct 2025 17:28:32 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:8b7c977482113b7d4c3379dbab8ea8bfed0e95e8088d98dd30cfb2aac2c9f2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81053367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4f08759596e3b9e5d7290dfbdfc8e075247f58227efbc547a1dc5030408742`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba702f0f51333fc2712ffc50d66684ef842dd2f30e7e612a7085b6264c7d0c0`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 1.3 MB (1309688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902b9bcf1c68a9433fa734e7f77d0062d7271f532391ae56abbef8e2820cf828`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00eeb6308e90b8bb2e276d4c0017af677089a878c4fc04021ec60abaf88b633b`  
		Last Modified: Tue, 16 Sep 2025 17:27:49 GMT  
		Size: 39.6 MB (39595821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aa59464570e58df18efecb42c30257cdea420248e5b8999bbed0be72c06831`  
		Last Modified: Tue, 16 Sep 2025 17:27:46 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6774045721abcc7f4299c08bc8dbeda3cb9f3fa72fec4b4eb19dd591a04d6813`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 6.6 MB (6551103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd934fc95d3b2adb5857e2f00983abe8c01018c4e84546953a5f77482d66992`  
		Last Modified: Tue, 16 Sep 2025 18:01:56 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc71cd1ca099ac43138c3be1a95632e82bc0144a52934fe849f86ad270b5a7a`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7fe823656da82cfb8ab46a01f99d1a4ca0687f122ae82a8d4e452e1b20fd9e`  
		Last Modified: Tue, 16 Sep 2025 18:01:57 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:6c93025c0827bfd0d7b4e45dc24e2651898def62a33ed54347f89a5015af19d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03e92a175b411b28ac4407b23a620cb846b039a7656d72f9760a97da6dded42`

```dockerfile
```

-	Layers:
	-	`sha256:bd8a127995092ba84037010e07bf054f2fb51ccfb7c31d1b317e5e2aa323b274`  
		Last Modified: Tue, 16 Sep 2025 20:29:08 GMT  
		Size: 2.3 MB (2287015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99646e9dec58fd128ee6ae948247dfd018b470f6c449c9e956b352abbbab360c`  
		Last Modified: Tue, 16 Sep 2025 20:29:09 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:e1077d51cf425d916d172165c7e0adc158afdbfbcf5742ff7817babd8fec5cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76824627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323347be19501d30e21197bb58f1458e9a1aa28044755a9d28be61e0b8170168`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.6
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.6.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=804995bc22938aa475127000d3103cb133409ad3955edfc0e7412be66a4859b8
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV GEM_HOME=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Thu, 31 Jul 2025 04:35:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["irb"]
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 31 Jul 2025 04:35:05 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.0
# Thu, 31 Jul 2025 04:35:05 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.1  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.0  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 31 Jul 2025 04:35:05 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 31 Jul 2025 04:35:05 GMT
USER fluent
# Thu, 31 Jul 2025 04:35:05 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 31 Jul 2025 04:35:05 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70370253f1ce091fe730c380a58bcad6c984318332f9815450f5cfaa70aa87f5`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 1.3 MB (1294292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ec12509a32b107309b0e8ad0dd5f247db0a2ca036489efbfcf07069855b56d`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95e9b1c0885cb28c05fa772e1873d7827da80a057035afb16216bb0e18774ea`  
		Last Modified: Tue, 16 Sep 2025 17:17:57 GMT  
		Size: 39.3 MB (39286986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160aaf92b9681375fe7aaa71ed89f2fa889c9ed589628572f762bc3bde9e15e7`  
		Last Modified: Tue, 16 Sep 2025 17:17:49 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b20eb585bc1db6ed5ff9536e3f8f84a65a0a753ea5af95fde9d1cfffcea90e`  
		Last Modified: Tue, 16 Sep 2025 17:58:10 GMT  
		Size: 6.4 MB (6408044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a23e9fdec9bdc5545d5ce9e7c776cec3f3a8967d96ef8a15039b8e0c62b5089`  
		Last Modified: Tue, 16 Sep 2025 17:58:09 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05227e73144ce28d40dbc8ec6e46e37a0d636968a8968df0a54a6dec3c8a31fb`  
		Last Modified: Tue, 16 Sep 2025 17:58:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4096477949e4f1d7d4a4c2fdf49030b44fe4be6c2ca84f6d7300527798af25e`  
		Last Modified: Tue, 16 Sep 2025 17:58:10 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7c98b5fe01dcee58e79906a8cda5ef48240d894adb6159e6890490f3548600d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd6db0e98cfcc6e85267280437a4963dbbc4a2e705f4b755a2baffcdc822b4a`

```dockerfile
```

-	Layers:
	-	`sha256:782a11d83d8a50fd862f7758dbb73b14c5932683d824bf14cd3b5844d177193d`  
		Last Modified: Tue, 16 Sep 2025 20:29:14 GMT  
		Size: 2.3 MB (2284925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796f5926fb2ed48c47aa5a5bd6ed0e0b3e417aadf0957f8e59270058399d4f92`  
		Last Modified: Tue, 16 Sep 2025 20:29:15 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json
