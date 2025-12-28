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
$ docker pull fluentd@sha256:8c44f4b95a232eeb20682fd642f2262a04e3e0b5045f318cb707e0ce2ed03bea
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
$ docker pull fluentd@sha256:2e281a4d2bfd7389c89d191a4aa38a63211e08e4bab3372985c8829dd44552df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73016020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9132ce316ff971ffcd2aa7a5c5bd64785657f898d88dfd917a3438ccaf5b702c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:01:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:13:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:13:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:13:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:13:55 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:13:55 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:13:55 GMT
USER fluent
# Wed, 17 Dec 2025 20:13:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:13:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c694792a75e7d76b490ae53980be6c2ce4fc998b1abd1475632aff8287efc`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 1.3 MB (1263015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6f6bf8da6225045c47fd91b956dedced5d22858a41d4abd24faf97bf3a73b1`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce54dc660a317ab44a20bbca82fcf472e5460a5d00afcef3157a0d661358c4`  
		Last Modified: Wed, 17 Dec 2025 20:05:49 GMT  
		Size: 37.9 MB (37906221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a63170ee86c30b036e6a19e4b2d3d7ece095f2f01bd32210c30d85fb115c84`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a81dcfbd2a86e33e6f2983a02b97705257c256b6c8d59a82f6a1c1870c1d5f`  
		Last Modified: Wed, 17 Dec 2025 20:14:16 GMT  
		Size: 5.9 MB (5900202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928044fa3186dc09088e6022988048179ee0956fa6539e4e7e777079c95941b`  
		Last Modified: Wed, 17 Dec 2025 20:14:15 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad673d7a54829730a1d99e1f482693639c90181e8dba554c614f17ae9391eb10`  
		Last Modified: Wed, 17 Dec 2025 20:14:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f53e6794061ca3f128990137a16356b70a815fc1281616fee26354fad9cf238`  
		Last Modified: Wed, 17 Dec 2025 20:14:14 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:5822791d2c146c240a6db34cf3091234b74db0c763a30cfc4a2b91f098bd76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38999837f8a8c8ec535dbe53874b8e6b31181ce2795aa6a5917d527f1415791e`

```dockerfile
```

-	Layers:
	-	`sha256:ee6f93f01dc397e5a393ec3833092a9d10645e0946184ea1e02102d2618742e5`  
		Last Modified: Wed, 17 Dec 2025 21:28:39 GMT  
		Size: 2.3 MB (2283076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db50f75d562b56c401d9d075cb4616765c5c60a312532db20c8647447a6f8f0`  
		Last Modified: Wed, 17 Dec 2025 21:28:40 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:52386d9fbca5e4b5cc088352526c0e3c4cf51be51e0f26b3603a3e07641dfd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70882759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220a27933802ea4c11ac8beef173d524db5fc07324dcb4a439b26f9e68a93de`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:07:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:07:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:10:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:10:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:10:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:10:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:13:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 21:13:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 21:13:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 21:13:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 21:13:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 21:13:20 GMT
USER fluent
# Wed, 17 Dec 2025 21:13:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 21:13:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af25235a6de2f73e167fe9d88cdb35738f38330c0c1adb0a191c1fc872a9a364`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 1.2 MB (1236507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1bb323f42cea80e196b1c113bbf05dc2ffc74c425a95add0955e6d63de14d8`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179e797e543eb082ba216f703bd38c73f866328fa552cbcf520c594c28d80306`  
		Last Modified: Wed, 17 Dec 2025 20:10:35 GMT  
		Size: 37.8 MB (37766875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c92a6a12306fa8638515dcae5b2813033ff5ffb720ea29cd55a4c2a33e8efa`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7f61ef88bae3b047c2cfc4a457c18c71c6811f2684cc81717061d6354ac9b`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 5.7 MB (5666971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea2617a74be904e505d34f84800b1264f38db650537a2e9f0e91a8270bdf71`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d71df345b8a5d1f1a637ac1bfc24f1f25d50bbece4d887a3f3aafc5bfe9971`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333971b0001af4916c9dde13bf2ae6b47f0abc68a5520106bdf314d5fdff0024`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:dbcd5fb56afa1e0e644dd7830aa1f96e9511a441854f1db4d8a8dbcc76edf221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95c721314f5ce0fa6462b3644eb511bed426d68bacc782ae9b81452b7fe36ff`

```dockerfile
```

-	Layers:
	-	`sha256:a20ad8df9e4981fb7f1004b28b0319ea519b5572f91ca2c71c18e906c4cff0eb`  
		Last Modified: Thu, 18 Dec 2025 00:28:54 GMT  
		Size: 2.3 MB (2281517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ef7f8dd08cef21651402ee0ac9d1340826bbce65c398a8da68760f7876588a`  
		Last Modified: Thu, 18 Dec 2025 00:28:55 GMT  
		Size: 21.4 KB (21426 bytes)  
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
$ docker pull fluentd@sha256:73be61587891d374d3c979debd8a69f833a0f85de1eb94114b1f047bc27b7927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76212297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351f56953b1c30bd87baf457bfe140e4c16e8f8a40754ec76384ff82d6c33077`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:03:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:54 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:11:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:11:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:11:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:11:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:11:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:11:20 GMT
USER fluent
# Wed, 17 Dec 2025 20:11:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:11:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf1defef1ae1276b0248a3c76741c1891939a1305af2224f030f0be43e9db41`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 1.3 MB (1287235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cce8366db0dd679385b27b26e792754efc6013e1eda6246ee7ca02f922319a`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b00e55c71100d0de4f564dfcb1fc8490be93fe4f8103e8d52dfa969a36734`  
		Last Modified: Wed, 17 Dec 2025 20:06:12 GMT  
		Size: 37.7 MB (37660989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fc4a019eaaef42d87bc0513d35218ffa99b699068a12455d4242dcdaf38d72`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb78718a1133db063b1ce75239c860b6f2f0f6122eb5dfc1991f9641b2be050`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 6.0 MB (5968610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781fd9850d76b1d666d28ef26adb2d39c4c05eb608589dbed770ee0547e69a26`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2df57eb74f0355cd0eb5f946b505243377a86644076d239e11995bbec6d39f`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6872d4ffa7a906ea417de17f24dead0e2ef3a08572e1b8efac674ede0da3b9`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:08cfd12ad67134dcd23de31a90ae0862508c0ab3701f98bcfd15b299f48541f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aec5ba6d2aa7c291a1d4723fc3b3b42e6fa9a831d491b806449a2e2370e6a76`

```dockerfile
```

-	Layers:
	-	`sha256:3f503c9d2868e3e13b005f645397720ccdc305fd4000a78a1fe573585211f18d`  
		Last Modified: Wed, 17 Dec 2025 21:28:53 GMT  
		Size: 2.3 MB (2277293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d22ded427958d01913dcfdd1170d7f316e3dce1f47b36b13dbcb6365337bc42`  
		Last Modified: Wed, 17 Dec 2025 21:28:54 GMT  
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
$ docker pull fluentd@sha256:df866d45e9c42990004664ebbbc84a5da8226c60a6812f38e4b35c72f4427a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76710384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173e4062a59954573ad08ea80deac1a44ee4999e1b9be3718d12f03ecd9cb272`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:20:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:16 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:17 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:12:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:12:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:12:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:12:34 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:12:34 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:12:34 GMT
USER fluent
# Wed, 17 Dec 2025 20:12:34 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:12:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662846f86a973652ecbddd619140820b878a10b24d506301b3ff40bc977f649e`  
		Last Modified: Tue, 09 Dec 2025 01:23:20 GMT  
		Size: 1.3 MB (1294298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2be1d5814f3adfc26d3329bfeb07a0dbe2c41e30e37cdde13ed72d5f1998a3`  
		Last Modified: Tue, 09 Dec 2025 01:23:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04baeba94b0b05b3cf0c2e16ea2c3ac0481ca6c567133c5ca75d2542df991405`  
		Last Modified: Wed, 17 Dec 2025 20:05:43 GMT  
		Size: 39.2 MB (39205556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f033f95cdad94e516803e0f39534b1a9074ec1415305ce0c686e9285abed1d60`  
		Last Modified: Wed, 17 Dec 2025 20:05:37 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cdc8fab2b07dd1273cac69e76b0defaf389454ffd9bc8dccc4190b27d8406`  
		Last Modified: Wed, 17 Dec 2025 20:12:52 GMT  
		Size: 6.4 MB (6373737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbf8ce3f8a45fc259f69c3379222b09ffe7156593fd4b2eeec78322ec41170a`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b391fd190f6e8a6eb073e8ce5c63d71b77532e3a1cb00b9ba54cca6d4159df`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767a525eb440c984de5ff08e89df817785fb9ab54ef788bfae5d00f2cd0ee644`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:b2aef20825bca4e726f8ca8ddf40961cf371e014e7a786e5005100af0b3a6636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6700b757d6ba83e04526bcd96d2f5c5ab3b3c057fef86aba3c1b971ab881158`

```dockerfile
```

-	Layers:
	-	`sha256:df7914f5a0a1b027ccec3f33313de14f71942676edacc8fb99c60c58a6a6a7e2`  
		Last Modified: Wed, 17 Dec 2025 21:29:01 GMT  
		Size: 2.3 MB (2281550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4dd252f3d08c04e4907e55e076b0eca323f1f974c5fb38d38191ab3a58c75`  
		Last Modified: Wed, 17 Dec 2025 21:29:02 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16-debian-1`

```console
$ docker pull fluentd@sha256:845f06514e582e17742f173c13decf37172c11b8e072753a30218330c518cee7
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
$ docker pull fluentd@sha256:8a39ab4e78305c7b663ceca216fbc17991adbb817927ddac83d7a54faa820df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82039546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e15a6053367d0baacdfe07c6fc24441ff3a06cac6ead89fcb0011d41fac898`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 19:59:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 19:59:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:01:50 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:01:50 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:01:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:01:50 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:01:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:01:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:01:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:01:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:01:51 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:01:51 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:48:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:48:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:48:23 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:48:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:48:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:48:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:48:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:48:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:48:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:48:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:48:23 GMT
USER fluent
# Sun, 28 Dec 2025 05:48:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:48:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be30ced145e85067c62f7eafac5dd37427e58f49e3d9a78b72a6cb92cee47d50`  
		Last Modified: Tue, 09 Dec 2025 20:02:05 GMT  
		Size: 3.5 MB (3509689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad33bed68ecef7f0761d4f6f6fbc0e3d9db6eb02a4138fe0c16a996816671ebd`  
		Last Modified: Tue, 09 Dec 2025 20:02:04 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0d67719573c5da5766acc973d84a9753fdf20e7c4bbeced5bea08d3dbda27b`  
		Last Modified: Tue, 09 Dec 2025 20:02:18 GMT  
		Size: 36.0 MB (36007640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91650c12d185e0bf16248735a92cb70944d07c713dff39d307844fa7efd68e5`  
		Last Modified: Tue, 09 Dec 2025 20:02:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0970d6af829b1f518a7e70e67d4a0c6691deb3dc67f679f4a888934d5a1f190a`  
		Last Modified: Sun, 28 Dec 2025 05:48:39 GMT  
		Size: 14.3 MB (14291408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53954dab7140731fcfe1a6acd0dcf237c46226205442f7c879c9a6d5a411bca9`  
		Last Modified: Sun, 28 Dec 2025 05:48:37 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d5f0533db3ab04dd4ea0da780b45a4c64fe933e4dba77bacfc7b754954c462`  
		Last Modified: Sun, 28 Dec 2025 05:48:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5233b6ca22562efae7cd8190025ca28f69f142b7051175b207acdcb08ac20113`  
		Last Modified: Sun, 28 Dec 2025 05:48:37 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c7ca08a2155e5b38ac91bb6a5bd9952b19d0df7880c90243e911b4e9201ff00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4ac22a79fbbe5741119af43169e99130d77ed7389c30734a1fbe722758fa39`

```dockerfile
```

-	Layers:
	-	`sha256:58466d3d1ca81c45d2043ed22ad9593f311661bf7f62730fd04919623f5e0529`  
		Last Modified: Sun, 28 Dec 2025 06:28:42 GMT  
		Size: 2.7 MB (2671022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faec3396da495d1875acce3a4c9c1a341917c9903b6c8381f61c2af5509729f7`  
		Last Modified: Sun, 28 Dec 2025 06:28:46 GMT  
		Size: 21.1 KB (21066 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:30810df4f50b83ec5dab1e9caf44f524de68df3053faba02ee404ea173a86614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75437276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005f778cb1503bfcce52427bcd3da81ad3bb1494995c8fd48f2195eb35b32481`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 19:58:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 19:58:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:07:12 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:07:12 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:07:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:07:12 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:07:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:07:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:07:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:07:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:07:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:07:12 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:47:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:47:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:47:41 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:47:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:47:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:47:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:47:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:47:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:47:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:47:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:47:41 GMT
USER fluent
# Sun, 28 Dec 2025 05:47:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:47:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:20ca79728ab9e4eb574872cf271bd965c51cf4e8ac84660ef17b281a3aeb750e`  
		Last Modified: Mon, 08 Dec 2025 22:16:26 GMT  
		Size: 25.8 MB (25757588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2e19576652afa635083807e4dabe5f363645e40718b4d684b1b7decfb6d420`  
		Last Modified: Tue, 09 Dec 2025 20:01:11 GMT  
		Size: 3.1 MB (3079835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940545a1b85fe6cc39eab181ad6096b37c0b88c366e34a82e8781c24e6db946f`  
		Last Modified: Tue, 09 Dec 2025 20:01:10 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09abdb3c1380b0105ce7e7959b2078e646086335250b6a464db8a796a661f1ad`  
		Last Modified: Tue, 09 Dec 2025 20:07:31 GMT  
		Size: 32.3 MB (32327367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c08ddfacd35b3c840dbfef39572dd7bd21fdbb61ce14f97d90d154f1ca4a06`  
		Last Modified: Tue, 09 Dec 2025 20:07:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6d87a38cedc4f035e7f15794aec6fb7c6311ff1e15b790d7017c887f707ccf`  
		Last Modified: Sun, 28 Dec 2025 05:48:01 GMT  
		Size: 14.3 MB (14270096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c78395c8dc30fe32ea07e9beb51a4643d9b98381404458173bdf357f298c04`  
		Last Modified: Sun, 28 Dec 2025 05:47:59 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0ad41c2e1f036061ea9fac32a1c42d5c669d7146a084b68b3edab17d46624a`  
		Last Modified: Sun, 28 Dec 2025 05:47:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e06168d7a84dcdff2427da9de236942d2f2b0d32d801a1ea99d4dedfb40e2d`  
		Last Modified: Sun, 28 Dec 2025 05:47:58 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:3a7b66644466b6ab05d74288a97823882ee6e6589adac3e7e869ddfd6d97d353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49da231cab71f07172edece30d52a35708533ac2971aa6c15244a8a65d5a6ed5`

```dockerfile
```

-	Layers:
	-	`sha256:fca8b1aed65aba35b9cae23a51934b0d69402956c99b0cd73f426f357c8c30c7`  
		Last Modified: Sun, 28 Dec 2025 06:28:49 GMT  
		Size: 2.7 MB (2674817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc3659df20813731f88b1cd561147c71b610e314e2efde9cae5da5a53462387`  
		Last Modified: Sun, 28 Dec 2025 06:28:50 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:15602971940bb9c37969049b7664ffbe3f11f85231f7dec7fcc721e634c3ce9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73209700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa453e4ee8823ac5e6fe71f2e393e3489caa494550cc7c7978eb159ea745e97f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 20:04:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:04:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:09:02 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:09:02 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:09:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:09:02 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:09:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:09:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:09:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:09:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:09:02 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:09:02 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:48:37 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:48:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:48:37 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:48:37 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:48:37 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:48:37 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:48:37 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:48:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:48:37 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:48:37 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:48:37 GMT
USER fluent
# Sun, 28 Dec 2025 05:48:37 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:48:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426a3fe29be9b91d45f1095c331e18d3f7d252847a5cb17c41020ba773b9a782`  
		Last Modified: Tue, 09 Dec 2025 20:06:43 GMT  
		Size: 2.9 MB (2912812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429c23dfc81f34bc272eb3ddb5fb76c034c8732edafb34ae2bb8136ae444d075`  
		Last Modified: Tue, 09 Dec 2025 20:06:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498f5a384fec6b596077fbd9cb00c6c82321edb8858d917eaf1ad71a9b3f30a2`  
		Last Modified: Tue, 09 Dec 2025 20:09:21 GMT  
		Size: 32.2 MB (32161992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d721b24e067416c4f0fd48d901197dae569d651f059f68be97c81dd3c811f421`  
		Last Modified: Tue, 09 Dec 2025 20:09:15 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda8229a35f8b06bd7ebfa439208e7a992a962ac3f82c1338b03d510ace8312d`  
		Last Modified: Sun, 28 Dec 2025 05:48:52 GMT  
		Size: 14.2 MB (14198485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a72af59939027cf060adf8e40fcfd1652f10036a2fc05b9fcfab3bae5af8555`  
		Last Modified: Sun, 28 Dec 2025 05:48:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b77c2b0b0618487738ef0b6ada0ff2838aedf684b37602139cb1168cd8c80dc`  
		Last Modified: Sun, 28 Dec 2025 05:48:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4209316da5e048082b04dc48c93651747cf40371c8c449d82c88c98192a295c`  
		Last Modified: Sun, 28 Dec 2025 05:48:51 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0577f8fc57917cdcd30dbc93ab73b4c4c5348dacbbbe7f025f5680128530a5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825202924f919da85f73ab861290443d34a2819b020910719d13ad661e54f053`

```dockerfile
```

-	Layers:
	-	`sha256:fe03223f0dfed3b73296508cd5aa9d3fd2aa0cc77ddff0373da9e05ca7bcfda1`  
		Last Modified: Sun, 28 Dec 2025 06:28:53 GMT  
		Size: 2.7 MB (2673248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cea285a4bd70aa520f1eb4155a007d282dd2267ab829c68ca5c12e4d9a97c4d`  
		Last Modified: Sun, 28 Dec 2025 06:28:54 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:ff55959244d6428c98d0a00eb3b75b7d55b44145acf28e0f60f1a7a23c32d4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81652082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc605dd3cdcbca78dc453be1a69c7435c8e3781a46ced51fcde3705bcdd2018b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 19:59:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 19:59:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:01:52 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:01:52 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:01:52 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:01:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:01:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:01:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:01:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:01:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:01:52 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:48:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:48:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:48:42 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:48:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:48:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:48:43 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:48:43 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:48:43 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:48:43 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:48:43 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:48:43 GMT
USER fluent
# Sun, 28 Dec 2025 05:48:43 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:48:43 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c402d753c2b0c7dfdc7b34f827d46ebd3cb9ffbea8f03fbc745b504bd17b61f`  
		Last Modified: Tue, 09 Dec 2025 20:02:09 GMT  
		Size: 3.3 MB (3340642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f48c8155a74d53cdfc78b141b3a4a68c80c79eeb8273891f1fc657f3926035`  
		Last Modified: Tue, 09 Dec 2025 20:02:09 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521fd0034dcefb8bdaeeedb9980aa21612b7addc44e1923a4115b24d1ab375e`  
		Last Modified: Tue, 09 Dec 2025 20:02:17 GMT  
		Size: 35.9 MB (35909006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e84b09a0a13bfbca9d703b3f1dbacd109f036b0e543479192e27d5d6d7e37f`  
		Last Modified: Tue, 09 Dec 2025 20:02:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f6104315a290980b07a5279d01f57849219d7e6ce0e90fe251bde39164a7c5`  
		Last Modified: Sun, 28 Dec 2025 05:48:58 GMT  
		Size: 14.3 MB (14297810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5872adabbcbac44aa08fcbae1e128e56dcdae8da1a2a89fee54a4f43bc1b7f`  
		Last Modified: Sun, 28 Dec 2025 05:48:57 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b6b3373b82be67d776251fd3895ccc974f57e4c9278763ec6eba2b175b926`  
		Last Modified: Sun, 28 Dec 2025 05:48:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06be7e41865d40a818f963a34310d23de6dfc5dab62bff7d77f14d8f0895f139`  
		Last Modified: Sun, 28 Dec 2025 05:48:57 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b335affc54e691a66b42b1d268d9974eddb320cd8d7596c70fbbf3d1be900bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d1e414a13d17c8e7db5a110f22ba0b7d842d2ff12f364d6b7cd763a8f956bf`

```dockerfile
```

-	Layers:
	-	`sha256:6206cbbf5d29800fa26d2ced0dfca18d2895b99cf76939850593ad8b5d00b233`  
		Last Modified: Sun, 28 Dec 2025 06:28:58 GMT  
		Size: 2.7 MB (2671262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba6436c150333ae583139b49361963331db0ece1cd9c6b99d3bdf1176575fad3`  
		Last Modified: Sun, 28 Dec 2025 06:28:59 GMT  
		Size: 21.2 KB (21163 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:bbc9dcaeef05b448904073f2f1f8aed67c5e2fa0575f06d3758139ef2a66a9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd368a7476619ab4ad82b9b70025066e3e9b8ff327fdc829944e9433250ebed`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 20:00:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:00:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:02:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:02:38 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:02:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:02:38 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:02:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:02:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:02:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:02:38 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:47:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:47:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:47:51 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:47:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:47:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:47:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:47:52 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:47:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:47:52 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:47:52 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:47:52 GMT
USER fluent
# Sun, 28 Dec 2025 05:47:52 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:47:52 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f6b3ee474f0c33356d973f13524a092d7963f6c4e6ae26674d690fd2212c97`  
		Last Modified: Tue, 09 Dec 2025 20:02:53 GMT  
		Size: 3.5 MB (3511006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6f1e1b677ef366cfc335e7a05f50c82416a53b9000d351fde132c974c48e04`  
		Last Modified: Tue, 09 Dec 2025 20:02:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a280d36383e95254b0abe8108873ceafb576ec5c5a3a6d988ed3ce83429ea9e`  
		Last Modified: Tue, 09 Dec 2025 20:03:07 GMT  
		Size: 32.2 MB (32159987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18aa47e1506cc4d53b64991456b1155af1456f35b93aad3c3e24631d0a03079`  
		Last Modified: Tue, 09 Dec 2025 20:02:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f21abe61e76b875d773c2d14cb545ba36d73f58c9b7155c0d1df86c42f82c27`  
		Last Modified: Sun, 28 Dec 2025 05:48:06 GMT  
		Size: 14.1 MB (14081085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53f5f7ef88867d6fe1047b92e2e894a6351374ad227853e764b9f6b6d537bb`  
		Last Modified: Sun, 28 Dec 2025 05:48:05 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac6f8dc89a1a2c3fd76a40ef526ae43c3286aa03623000eb1ae3a3f5dcad2b4`  
		Last Modified: Sun, 28 Dec 2025 05:48:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed049c1fc314a16a56463133484ea4963977d937df9588fea7b7171a912230f`  
		Last Modified: Sun, 28 Dec 2025 05:48:05 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:42caf680cae9b37b66218af0e9932b864dc5ade3e4cc924488c2c2645a5ef60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e876366507579c457aa93fb9d713435174b84c1961916ebb12150ad7237409c`

```dockerfile
```

-	Layers:
	-	`sha256:04f7659a4c44574279dd04126dbde641ff70459924ae8587bdda143787f869f6`  
		Last Modified: Sun, 28 Dec 2025 06:29:02 GMT  
		Size: 2.7 MB (2668201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3035d9a4a6c0775fe7bb544c48d70e387eea1f7021b413b9f37773abc23783a`  
		Last Modified: Sun, 28 Dec 2025 06:29:03 GMT  
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
$ docker pull fluentd@sha256:cffab6393dfeed35e48e7851821b8e67178ee669cd0480ea719deca57d14bb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0911a2679cbdf1f86678754f5c398edad90d74a3ace880bd43c750b36c0d1343`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:20:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:15:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:15:42 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:15:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:15:42 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:15:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:15:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:15:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:15:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:15:43 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:15:43 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:47:32 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:47:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:47:32 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:47:32 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:47:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:47:32 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:47:32 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:47:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:47:32 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:47:32 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:47:32 GMT
USER fluent
# Sun, 28 Dec 2025 05:47:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:47:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c68f0ebe313b468387e42a6bbf8b5b855c42d1a9aecca5d1e79d1513386fde7`  
		Last Modified: Tue, 09 Dec 2025 01:23:28 GMT  
		Size: 3.2 MB (3170271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa348aa4bda397502f2be230364b9fab79e0917fc3a7af75372bb9389759fb2`  
		Last Modified: Tue, 09 Dec 2025 01:23:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343a6ecc44486c861e0a95c5dee4bf205c0d701e397c220be2981ce506d2e4e6`  
		Last Modified: Tue, 09 Dec 2025 20:16:08 GMT  
		Size: 33.1 MB (33099213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba29e3b57d8c7e9632afae140ec2be71dfe7e5f3a9452cae94d77020a75c9`  
		Last Modified: Tue, 09 Dec 2025 20:16:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bee0a60bb6c2724e9f8417b8693ad0cc99eceffe408698b773e817f8031241`  
		Last Modified: Sun, 28 Dec 2025 05:47:54 GMT  
		Size: 14.4 MB (14426723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5232c69f939bc97d7cf2fd342e98fa7c4a1f1964a8fca29abac6f8183004917c`  
		Last Modified: Sun, 28 Dec 2025 05:47:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaf072ce05c0c5ba5c572e2ea6d785995a67d071a7d8867cc7ae079d73b0459`  
		Last Modified: Sun, 28 Dec 2025 05:47:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a70c664199c2fd4b33fcf9607a2288c5678bc935fd6fbe59a7c366f838ae776`  
		Last Modified: Sun, 28 Dec 2025 05:47:59 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:78fa4159d1eee1581c097f3dc728c8781067e36cd73cdcfd584fc81bd3778fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6ea21e031621b2c965c4a3f62d971066798fdc125b012c0f53531c02d88bc6`

```dockerfile
```

-	Layers:
	-	`sha256:c1f2b281e5b9ad3d526de94047b5ef76ca80461a8b08f7114bde9f8270727788`  
		Last Modified: Sun, 28 Dec 2025 06:29:10 GMT  
		Size: 2.7 MB (2667847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b566bf3918d4f1868ff098bf93fef62c798c96b362863ee6c61b63ba5cc017`  
		Last Modified: Sun, 28 Dec 2025 06:29:12 GMT  
		Size: 21.1 KB (21068 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.16.11-debian-1.0`

```console
$ docker pull fluentd@sha256:845f06514e582e17742f173c13decf37172c11b8e072753a30218330c518cee7
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
$ docker pull fluentd@sha256:8a39ab4e78305c7b663ceca216fbc17991adbb817927ddac83d7a54faa820df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82039546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e15a6053367d0baacdfe07c6fc24441ff3a06cac6ead89fcb0011d41fac898`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 19:59:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 19:59:47 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:01:50 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:01:50 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:01:50 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:01:50 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:01:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:01:50 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:01:50 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:01:50 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:01:51 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:01:51 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:48:23 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:48:23 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:48:23 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:48:23 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:48:23 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:48:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:48:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:48:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:48:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:48:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:48:23 GMT
USER fluent
# Sun, 28 Dec 2025 05:48:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:48:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be30ced145e85067c62f7eafac5dd37427e58f49e3d9a78b72a6cb92cee47d50`  
		Last Modified: Tue, 09 Dec 2025 20:02:05 GMT  
		Size: 3.5 MB (3509689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad33bed68ecef7f0761d4f6f6fbc0e3d9db6eb02a4138fe0c16a996816671ebd`  
		Last Modified: Tue, 09 Dec 2025 20:02:04 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0d67719573c5da5766acc973d84a9753fdf20e7c4bbeced5bea08d3dbda27b`  
		Last Modified: Tue, 09 Dec 2025 20:02:18 GMT  
		Size: 36.0 MB (36007640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91650c12d185e0bf16248735a92cb70944d07c713dff39d307844fa7efd68e5`  
		Last Modified: Tue, 09 Dec 2025 20:02:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0970d6af829b1f518a7e70e67d4a0c6691deb3dc67f679f4a888934d5a1f190a`  
		Last Modified: Sun, 28 Dec 2025 05:48:39 GMT  
		Size: 14.3 MB (14291408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53954dab7140731fcfe1a6acd0dcf237c46226205442f7c879c9a6d5a411bca9`  
		Last Modified: Sun, 28 Dec 2025 05:48:37 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d5f0533db3ab04dd4ea0da780b45a4c64fe933e4dba77bacfc7b754954c462`  
		Last Modified: Sun, 28 Dec 2025 05:48:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5233b6ca22562efae7cd8190025ca28f69f142b7051175b207acdcb08ac20113`  
		Last Modified: Sun, 28 Dec 2025 05:48:37 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c7ca08a2155e5b38ac91bb6a5bd9952b19d0df7880c90243e911b4e9201ff00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4ac22a79fbbe5741119af43169e99130d77ed7389c30734a1fbe722758fa39`

```dockerfile
```

-	Layers:
	-	`sha256:58466d3d1ca81c45d2043ed22ad9593f311661bf7f62730fd04919623f5e0529`  
		Last Modified: Sun, 28 Dec 2025 06:28:42 GMT  
		Size: 2.7 MB (2671022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faec3396da495d1875acce3a4c9c1a341917c9903b6c8381f61c2af5509729f7`  
		Last Modified: Sun, 28 Dec 2025 06:28:46 GMT  
		Size: 21.1 KB (21066 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:30810df4f50b83ec5dab1e9caf44f524de68df3053faba02ee404ea173a86614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75437276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005f778cb1503bfcce52427bcd3da81ad3bb1494995c8fd48f2195eb35b32481`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 19:58:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 19:58:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:07:12 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:07:12 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:07:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:07:12 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:07:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:07:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:07:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:07:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:07:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:07:12 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:47:41 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:47:41 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:47:41 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:47:41 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:47:41 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:47:41 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:47:41 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:47:41 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:47:41 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:47:41 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:47:41 GMT
USER fluent
# Sun, 28 Dec 2025 05:47:41 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:47:41 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:20ca79728ab9e4eb574872cf271bd965c51cf4e8ac84660ef17b281a3aeb750e`  
		Last Modified: Mon, 08 Dec 2025 22:16:26 GMT  
		Size: 25.8 MB (25757588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2e19576652afa635083807e4dabe5f363645e40718b4d684b1b7decfb6d420`  
		Last Modified: Tue, 09 Dec 2025 20:01:11 GMT  
		Size: 3.1 MB (3079835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940545a1b85fe6cc39eab181ad6096b37c0b88c366e34a82e8781c24e6db946f`  
		Last Modified: Tue, 09 Dec 2025 20:01:10 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09abdb3c1380b0105ce7e7959b2078e646086335250b6a464db8a796a661f1ad`  
		Last Modified: Tue, 09 Dec 2025 20:07:31 GMT  
		Size: 32.3 MB (32327367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c08ddfacd35b3c840dbfef39572dd7bd21fdbb61ce14f97d90d154f1ca4a06`  
		Last Modified: Tue, 09 Dec 2025 20:07:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6d87a38cedc4f035e7f15794aec6fb7c6311ff1e15b790d7017c887f707ccf`  
		Last Modified: Sun, 28 Dec 2025 05:48:01 GMT  
		Size: 14.3 MB (14270096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c78395c8dc30fe32ea07e9beb51a4643d9b98381404458173bdf357f298c04`  
		Last Modified: Sun, 28 Dec 2025 05:47:59 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0ad41c2e1f036061ea9fac32a1c42d5c669d7146a084b68b3edab17d46624a`  
		Last Modified: Sun, 28 Dec 2025 05:47:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e06168d7a84dcdff2427da9de236942d2f2b0d32d801a1ea99d4dedfb40e2d`  
		Last Modified: Sun, 28 Dec 2025 05:47:58 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:3a7b66644466b6ab05d74288a97823882ee6e6589adac3e7e869ddfd6d97d353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49da231cab71f07172edece30d52a35708533ac2971aa6c15244a8a65d5a6ed5`

```dockerfile
```

-	Layers:
	-	`sha256:fca8b1aed65aba35b9cae23a51934b0d69402956c99b0cd73f426f357c8c30c7`  
		Last Modified: Sun, 28 Dec 2025 06:28:49 GMT  
		Size: 2.7 MB (2674817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebc3659df20813731f88b1cd561147c71b610e314e2efde9cae5da5a53462387`  
		Last Modified: Sun, 28 Dec 2025 06:28:50 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:15602971940bb9c37969049b7664ffbe3f11f85231f7dec7fcc721e634c3ce9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73209700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa453e4ee8823ac5e6fe71f2e393e3489caa494550cc7c7978eb159ea745e97f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 20:04:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:04:09 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:09:02 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:09:02 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:09:02 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:09:02 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:09:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:09:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:09:02 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:09:02 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:09:02 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:09:02 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:48:37 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:48:37 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:48:37 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:48:37 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:48:37 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:48:37 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:48:37 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:48:37 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:48:37 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:48:37 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:48:37 GMT
USER fluent
# Sun, 28 Dec 2025 05:48:37 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:48:37 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e12d446114182318769a6ca4adfc14d21fbb73f898de1d765662812d9f21c3a6`  
		Last Modified: Mon, 08 Dec 2025 22:16:03 GMT  
		Size: 23.9 MB (23934020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426a3fe29be9b91d45f1095c331e18d3f7d252847a5cb17c41020ba773b9a782`  
		Last Modified: Tue, 09 Dec 2025 20:06:43 GMT  
		Size: 2.9 MB (2912812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429c23dfc81f34bc272eb3ddb5fb76c034c8732edafb34ae2bb8136ae444d075`  
		Last Modified: Tue, 09 Dec 2025 20:06:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498f5a384fec6b596077fbd9cb00c6c82321edb8858d917eaf1ad71a9b3f30a2`  
		Last Modified: Tue, 09 Dec 2025 20:09:21 GMT  
		Size: 32.2 MB (32161992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d721b24e067416c4f0fd48d901197dae569d651f059f68be97c81dd3c811f421`  
		Last Modified: Tue, 09 Dec 2025 20:09:15 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda8229a35f8b06bd7ebfa439208e7a992a962ac3f82c1338b03d510ace8312d`  
		Last Modified: Sun, 28 Dec 2025 05:48:52 GMT  
		Size: 14.2 MB (14198485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a72af59939027cf060adf8e40fcfd1652f10036a2fc05b9fcfab3bae5af8555`  
		Last Modified: Sun, 28 Dec 2025 05:48:51 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b77c2b0b0618487738ef0b6ada0ff2838aedf684b37602139cb1168cd8c80dc`  
		Last Modified: Sun, 28 Dec 2025 05:48:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4209316da5e048082b04dc48c93651747cf40371c8c449d82c88c98192a295c`  
		Last Modified: Sun, 28 Dec 2025 05:48:51 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0577f8fc57917cdcd30dbc93ab73b4c4c5348dacbbbe7f025f5680128530a5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825202924f919da85f73ab861290443d34a2819b020910719d13ad661e54f053`

```dockerfile
```

-	Layers:
	-	`sha256:fe03223f0dfed3b73296508cd5aa9d3fd2aa0cc77ddff0373da9e05ca7bcfda1`  
		Last Modified: Sun, 28 Dec 2025 06:28:53 GMT  
		Size: 2.7 MB (2673248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cea285a4bd70aa520f1eb4155a007d282dd2267ab829c68ca5c12e4d9a97c4d`  
		Last Modified: Sun, 28 Dec 2025 06:28:54 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:ff55959244d6428c98d0a00eb3b75b7d55b44145acf28e0f60f1a7a23c32d4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81652082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc605dd3cdcbca78dc453be1a69c7435c8e3781a46ced51fcde3705bcdd2018b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 19:59:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 19:59:46 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:01:52 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:01:52 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:01:52 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:01:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:01:52 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:01:52 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:01:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:01:52 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:01:52 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:48:42 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:48:42 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:48:42 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:48:42 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:48:42 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:48:43 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:48:43 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:48:43 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:48:43 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:48:43 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:48:43 GMT
USER fluent
# Sun, 28 Dec 2025 05:48:43 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:48:43 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c402d753c2b0c7dfdc7b34f827d46ebd3cb9ffbea8f03fbc745b504bd17b61f`  
		Last Modified: Tue, 09 Dec 2025 20:02:09 GMT  
		Size: 3.3 MB (3340642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f48c8155a74d53cdfc78b141b3a4a68c80c79eeb8273891f1fc657f3926035`  
		Last Modified: Tue, 09 Dec 2025 20:02:09 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521fd0034dcefb8bdaeeedb9980aa21612b7addc44e1923a4115b24d1ab375e`  
		Last Modified: Tue, 09 Dec 2025 20:02:17 GMT  
		Size: 35.9 MB (35909006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e84b09a0a13bfbca9d703b3f1dbacd109f036b0e543479192e27d5d6d7e37f`  
		Last Modified: Tue, 09 Dec 2025 20:02:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f6104315a290980b07a5279d01f57849219d7e6ce0e90fe251bde39164a7c5`  
		Last Modified: Sun, 28 Dec 2025 05:48:58 GMT  
		Size: 14.3 MB (14297810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5872adabbcbac44aa08fcbae1e128e56dcdae8da1a2a89fee54a4f43bc1b7f`  
		Last Modified: Sun, 28 Dec 2025 05:48:57 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5b6b3373b82be67d776251fd3895ccc974f57e4c9278763ec6eba2b175b926`  
		Last Modified: Sun, 28 Dec 2025 05:48:57 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06be7e41865d40a818f963a34310d23de6dfc5dab62bff7d77f14d8f0895f139`  
		Last Modified: Sun, 28 Dec 2025 05:48:57 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b335affc54e691a66b42b1d268d9974eddb320cd8d7596c70fbbf3d1be900bba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d1e414a13d17c8e7db5a110f22ba0b7d842d2ff12f364d6b7cd763a8f956bf`

```dockerfile
```

-	Layers:
	-	`sha256:6206cbbf5d29800fa26d2ced0dfca18d2895b99cf76939850593ad8b5d00b233`  
		Last Modified: Sun, 28 Dec 2025 06:28:58 GMT  
		Size: 2.7 MB (2671262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba6436c150333ae583139b49361963331db0ece1cd9c6b99d3bdf1176575fad3`  
		Last Modified: Sun, 28 Dec 2025 06:28:59 GMT  
		Size: 21.2 KB (21163 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.11-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:bbc9dcaeef05b448904073f2f1f8aed67c5e2fa0575f06d3758139ef2a66a9d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78964202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd368a7476619ab4ad82b9b70025066e3e9b8ff327fdc829944e9433250ebed`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 20:00:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 20:00:34 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:02:38 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:02:38 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:02:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:02:38 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:02:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:02:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:02:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:02:38 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:02:38 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:47:51 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:47:51 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:47:51 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:47:51 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:47:51 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:47:51 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:47:52 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:47:52 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:47:52 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:47:52 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:47:52 GMT
USER fluent
# Sun, 28 Dec 2025 05:47:52 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:47:52 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:e28a7f622a043206041afc8ed0d2b3d1b9bbffe3b724b994051e9d6dbc2f8a1e`  
		Last Modified: Mon, 08 Dec 2025 22:16:30 GMT  
		Size: 29.2 MB (29209729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f6b3ee474f0c33356d973f13524a092d7963f6c4e6ae26674d690fd2212c97`  
		Last Modified: Tue, 09 Dec 2025 20:02:53 GMT  
		Size: 3.5 MB (3511006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6f1e1b677ef366cfc335e7a05f50c82416a53b9000d351fde132c974c48e04`  
		Last Modified: Tue, 09 Dec 2025 20:02:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a280d36383e95254b0abe8108873ceafb576ec5c5a3a6d988ed3ce83429ea9e`  
		Last Modified: Tue, 09 Dec 2025 20:03:07 GMT  
		Size: 32.2 MB (32159987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18aa47e1506cc4d53b64991456b1155af1456f35b93aad3c3e24631d0a03079`  
		Last Modified: Tue, 09 Dec 2025 20:02:53 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f21abe61e76b875d773c2d14cb545ba36d73f58c9b7155c0d1df86c42f82c27`  
		Last Modified: Sun, 28 Dec 2025 05:48:06 GMT  
		Size: 14.1 MB (14081085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c53f5f7ef88867d6fe1047b92e2e894a6351374ad227853e764b9f6b6d537bb`  
		Last Modified: Sun, 28 Dec 2025 05:48:05 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac6f8dc89a1a2c3fd76a40ef526ae43c3286aa03623000eb1ae3a3f5dcad2b4`  
		Last Modified: Sun, 28 Dec 2025 05:48:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed049c1fc314a16a56463133484ea4963977d937df9588fea7b7171a912230f`  
		Last Modified: Sun, 28 Dec 2025 05:48:05 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:42caf680cae9b37b66218af0e9932b864dc5ade3e4cc924488c2c2645a5ef60d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e876366507579c457aa93fb9d713435174b84c1961916ebb12150ad7237409c`

```dockerfile
```

-	Layers:
	-	`sha256:04f7659a4c44574279dd04126dbde641ff70459924ae8587bdda143787f869f6`  
		Last Modified: Sun, 28 Dec 2025 06:29:02 GMT  
		Size: 2.7 MB (2668201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3035d9a4a6c0775fe7bb544c48d70e387eea1f7021b413b9f37773abc23783a`  
		Last Modified: Sun, 28 Dec 2025 06:29:03 GMT  
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
$ docker pull fluentd@sha256:cffab6393dfeed35e48e7851821b8e67178ee669cd0480ea719deca57d14bb56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77583032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0911a2679cbdf1f86678754f5c398edad90d74a3ace880bd43c750b36c0d1343`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:20:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:20:17 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 09 Dec 2025 20:15:42 GMT
ENV LANG=C.UTF-8
# Tue, 09 Dec 2025 20:15:42 GMT
ENV RUBY_VERSION=3.2.9
# Tue, 09 Dec 2025 20:15:42 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.2/ruby-3.2.9.tar.xz
# Tue, 09 Dec 2025 20:15:42 GMT
ENV RUBY_DOWNLOAD_SHA256=cf6699d0084c588e7944d92e1a8edda28b1cc3ee471a1f0aebb4b3d32c9753b2
# Tue, 09 Dec 2025 20:15:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bison 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libreadline-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 09 Dec 2025 20:15:42 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 09 Dec 2025 20:15:42 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 09 Dec 2025 20:15:42 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 20:15:43 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 09 Dec 2025 20:15:43 GMT
CMD ["irb"]
# Sun, 28 Dec 2025 05:47:32 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Sun, 28 Dec 2025 05:47:32 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.16.11
# Sun, 28 Dec 2025 05:47:32 GMT
ENV TINI_VERSION=0.18.0
# Sun, 28 Dec 2025 05:47:32 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && gem install oj -v 3.16.1  && gem install json -v 2.6.3  && gem install rexml -v 3.4.4  && gem install async -v 1.31.0  && gem install async-http -v 0.60.2  && gem install fluentd -v 1.16.11  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch"  && wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/v$TINI_VERSION/tini-$dpkgArch.asc"  && export GNUPGHOME="$(mktemp -d)"  && gpg --batch --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5  && gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini  && rm -r /usr/local/bin/tini.asc  && chmod +x /usr/local/bin/tini  && tini -h  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* /usr/lib/ruby/gems/*/cache/*.gem /usr/lib/ruby/gems/3.*/gems/fluentd-*/test # buildkit
# Sun, 28 Dec 2025 05:47:32 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Sun, 28 Dec 2025 05:47:32 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Sun, 28 Dec 2025 05:47:32 GMT
COPY entrypoint.sh /bin/ # buildkit
# Sun, 28 Dec 2025 05:47:32 GMT
ENV FLUENTD_CONF=fluent.conf
# Sun, 28 Dec 2025 05:47:32 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Sun, 28 Dec 2025 05:47:32 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Sun, 28 Dec 2025 05:47:32 GMT
USER fluent
# Sun, 28 Dec 2025 05:47:32 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Sun, 28 Dec 2025 05:47:32 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c68f0ebe313b468387e42a6bbf8b5b855c42d1a9aecca5d1e79d1513386fde7`  
		Last Modified: Tue, 09 Dec 2025 01:23:28 GMT  
		Size: 3.2 MB (3170271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa348aa4bda397502f2be230364b9fab79e0917fc3a7af75372bb9389759fb2`  
		Last Modified: Tue, 09 Dec 2025 01:23:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343a6ecc44486c861e0a95c5dee4bf205c0d701e397c220be2981ce506d2e4e6`  
		Last Modified: Tue, 09 Dec 2025 20:16:08 GMT  
		Size: 33.1 MB (33099213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332ba29e3b57d8c7e9632afae140ec2be71dfe7e5f3a9452cae94d77020a75c9`  
		Last Modified: Tue, 09 Dec 2025 20:16:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bee0a60bb6c2724e9f8417b8693ad0cc99eceffe408698b773e817f8031241`  
		Last Modified: Sun, 28 Dec 2025 05:47:54 GMT  
		Size: 14.4 MB (14426723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5232c69f939bc97d7cf2fd342e98fa7c4a1f1964a8fca29abac6f8183004917c`  
		Last Modified: Sun, 28 Dec 2025 05:47:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaf072ce05c0c5ba5c572e2ea6d785995a67d071a7d8867cc7ae079d73b0459`  
		Last Modified: Sun, 28 Dec 2025 05:47:52 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a70c664199c2fd4b33fcf9607a2288c5678bc935fd6fbe59a7c366f838ae776`  
		Last Modified: Sun, 28 Dec 2025 05:47:59 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.11-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:78fa4159d1eee1581c097f3dc728c8781067e36cd73cdcfd584fc81bd3778fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2688915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a6ea21e031621b2c965c4a3f62d971066798fdc125b012c0f53531c02d88bc6`

```dockerfile
```

-	Layers:
	-	`sha256:c1f2b281e5b9ad3d526de94047b5ef76ca80461a8b08f7114bde9f8270727788`  
		Last Modified: Sun, 28 Dec 2025 06:29:10 GMT  
		Size: 2.7 MB (2667847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b566bf3918d4f1868ff098bf93fef62c798c96b362863ee6c61b63ba5cc017`  
		Last Modified: Sun, 28 Dec 2025 06:29:12 GMT  
		Size: 21.1 KB (21068 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:8c44f4b95a232eeb20682fd642f2262a04e3e0b5045f318cb707e0ce2ed03bea
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
$ docker pull fluentd@sha256:2e281a4d2bfd7389c89d191a4aa38a63211e08e4bab3372985c8829dd44552df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73016020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9132ce316ff971ffcd2aa7a5c5bd64785657f898d88dfd917a3438ccaf5b702c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:01:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:13:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:13:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:13:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:13:55 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:13:55 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:13:55 GMT
USER fluent
# Wed, 17 Dec 2025 20:13:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:13:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c694792a75e7d76b490ae53980be6c2ce4fc998b1abd1475632aff8287efc`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 1.3 MB (1263015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6f6bf8da6225045c47fd91b956dedced5d22858a41d4abd24faf97bf3a73b1`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce54dc660a317ab44a20bbca82fcf472e5460a5d00afcef3157a0d661358c4`  
		Last Modified: Wed, 17 Dec 2025 20:05:49 GMT  
		Size: 37.9 MB (37906221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a63170ee86c30b036e6a19e4b2d3d7ece095f2f01bd32210c30d85fb115c84`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a81dcfbd2a86e33e6f2983a02b97705257c256b6c8d59a82f6a1c1870c1d5f`  
		Last Modified: Wed, 17 Dec 2025 20:14:16 GMT  
		Size: 5.9 MB (5900202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928044fa3186dc09088e6022988048179ee0956fa6539e4e7e777079c95941b`  
		Last Modified: Wed, 17 Dec 2025 20:14:15 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad673d7a54829730a1d99e1f482693639c90181e8dba554c614f17ae9391eb10`  
		Last Modified: Wed, 17 Dec 2025 20:14:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f53e6794061ca3f128990137a16356b70a815fc1281616fee26354fad9cf238`  
		Last Modified: Wed, 17 Dec 2025 20:14:14 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5822791d2c146c240a6db34cf3091234b74db0c763a30cfc4a2b91f098bd76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38999837f8a8c8ec535dbe53874b8e6b31181ce2795aa6a5917d527f1415791e`

```dockerfile
```

-	Layers:
	-	`sha256:ee6f93f01dc397e5a393ec3833092a9d10645e0946184ea1e02102d2618742e5`  
		Last Modified: Wed, 17 Dec 2025 21:28:39 GMT  
		Size: 2.3 MB (2283076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db50f75d562b56c401d9d075cb4616765c5c60a312532db20c8647447a6f8f0`  
		Last Modified: Wed, 17 Dec 2025 21:28:40 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:52386d9fbca5e4b5cc088352526c0e3c4cf51be51e0f26b3603a3e07641dfd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70882759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220a27933802ea4c11ac8beef173d524db5fc07324dcb4a439b26f9e68a93de`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:07:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:07:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:10:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:10:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:10:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:10:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:13:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 21:13:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 21:13:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 21:13:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 21:13:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 21:13:20 GMT
USER fluent
# Wed, 17 Dec 2025 21:13:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 21:13:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af25235a6de2f73e167fe9d88cdb35738f38330c0c1adb0a191c1fc872a9a364`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 1.2 MB (1236507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1bb323f42cea80e196b1c113bbf05dc2ffc74c425a95add0955e6d63de14d8`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179e797e543eb082ba216f703bd38c73f866328fa552cbcf520c594c28d80306`  
		Last Modified: Wed, 17 Dec 2025 20:10:35 GMT  
		Size: 37.8 MB (37766875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c92a6a12306fa8638515dcae5b2813033ff5ffb720ea29cd55a4c2a33e8efa`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7f61ef88bae3b047c2cfc4a457c18c71c6811f2684cc81717061d6354ac9b`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 5.7 MB (5666971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea2617a74be904e505d34f84800b1264f38db650537a2e9f0e91a8270bdf71`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d71df345b8a5d1f1a637ac1bfc24f1f25d50bbece4d887a3f3aafc5bfe9971`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333971b0001af4916c9dde13bf2ae6b47f0abc68a5520106bdf314d5fdff0024`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:dbcd5fb56afa1e0e644dd7830aa1f96e9511a441854f1db4d8a8dbcc76edf221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95c721314f5ce0fa6462b3644eb511bed426d68bacc782ae9b81452b7fe36ff`

```dockerfile
```

-	Layers:
	-	`sha256:a20ad8df9e4981fb7f1004b28b0319ea519b5572f91ca2c71c18e906c4cff0eb`  
		Last Modified: Thu, 18 Dec 2025 00:28:54 GMT  
		Size: 2.3 MB (2281517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ef7f8dd08cef21651402ee0ac9d1340826bbce65c398a8da68760f7876588a`  
		Last Modified: Thu, 18 Dec 2025 00:28:55 GMT  
		Size: 21.4 KB (21426 bytes)  
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
$ docker pull fluentd@sha256:73be61587891d374d3c979debd8a69f833a0f85de1eb94114b1f047bc27b7927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76212297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351f56953b1c30bd87baf457bfe140e4c16e8f8a40754ec76384ff82d6c33077`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:03:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:54 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:11:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:11:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:11:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:11:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:11:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:11:20 GMT
USER fluent
# Wed, 17 Dec 2025 20:11:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:11:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf1defef1ae1276b0248a3c76741c1891939a1305af2224f030f0be43e9db41`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 1.3 MB (1287235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cce8366db0dd679385b27b26e792754efc6013e1eda6246ee7ca02f922319a`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b00e55c71100d0de4f564dfcb1fc8490be93fe4f8103e8d52dfa969a36734`  
		Last Modified: Wed, 17 Dec 2025 20:06:12 GMT  
		Size: 37.7 MB (37660989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fc4a019eaaef42d87bc0513d35218ffa99b699068a12455d4242dcdaf38d72`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb78718a1133db063b1ce75239c860b6f2f0f6122eb5dfc1991f9641b2be050`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 6.0 MB (5968610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781fd9850d76b1d666d28ef26adb2d39c4c05eb608589dbed770ee0547e69a26`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2df57eb74f0355cd0eb5f946b505243377a86644076d239e11995bbec6d39f`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6872d4ffa7a906ea417de17f24dead0e2ef3a08572e1b8efac674ede0da3b9`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:08cfd12ad67134dcd23de31a90ae0862508c0ab3701f98bcfd15b299f48541f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aec5ba6d2aa7c291a1d4723fc3b3b42e6fa9a831d491b806449a2e2370e6a76`

```dockerfile
```

-	Layers:
	-	`sha256:3f503c9d2868e3e13b005f645397720ccdc305fd4000a78a1fe573585211f18d`  
		Last Modified: Wed, 17 Dec 2025 21:28:53 GMT  
		Size: 2.3 MB (2277293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d22ded427958d01913dcfdd1170d7f316e3dce1f47b36b13dbcb6365337bc42`  
		Last Modified: Wed, 17 Dec 2025 21:28:54 GMT  
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
$ docker pull fluentd@sha256:df866d45e9c42990004664ebbbc84a5da8226c60a6812f38e4b35c72f4427a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76710384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173e4062a59954573ad08ea80deac1a44ee4999e1b9be3718d12f03ecd9cb272`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:20:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:16 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:17 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:12:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:12:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:12:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:12:34 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:12:34 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:12:34 GMT
USER fluent
# Wed, 17 Dec 2025 20:12:34 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:12:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662846f86a973652ecbddd619140820b878a10b24d506301b3ff40bc977f649e`  
		Last Modified: Tue, 09 Dec 2025 01:23:20 GMT  
		Size: 1.3 MB (1294298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2be1d5814f3adfc26d3329bfeb07a0dbe2c41e30e37cdde13ed72d5f1998a3`  
		Last Modified: Tue, 09 Dec 2025 01:23:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04baeba94b0b05b3cf0c2e16ea2c3ac0481ca6c567133c5ca75d2542df991405`  
		Last Modified: Wed, 17 Dec 2025 20:05:43 GMT  
		Size: 39.2 MB (39205556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f033f95cdad94e516803e0f39534b1a9074ec1415305ce0c686e9285abed1d60`  
		Last Modified: Wed, 17 Dec 2025 20:05:37 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cdc8fab2b07dd1273cac69e76b0defaf389454ffd9bc8dccc4190b27d8406`  
		Last Modified: Wed, 17 Dec 2025 20:12:52 GMT  
		Size: 6.4 MB (6373737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbf8ce3f8a45fc259f69c3379222b09ffe7156593fd4b2eeec78322ec41170a`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b391fd190f6e8a6eb073e8ce5c63d71b77532e3a1cb00b9ba54cca6d4159df`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767a525eb440c984de5ff08e89df817785fb9ab54ef788bfae5d00f2cd0ee644`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b2aef20825bca4e726f8ca8ddf40961cf371e014e7a786e5005100af0b3a6636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6700b757d6ba83e04526bcd96d2f5c5ab3b3c057fef86aba3c1b971ab881158`

```dockerfile
```

-	Layers:
	-	`sha256:df7914f5a0a1b027ccec3f33313de14f71942676edacc8fb99c60c58a6a6a7e2`  
		Last Modified: Wed, 17 Dec 2025 21:29:01 GMT  
		Size: 2.3 MB (2281550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4dd252f3d08c04e4907e55e076b0eca323f1f974c5fb38d38191ab3a58c75`  
		Last Modified: Wed, 17 Dec 2025 21:29:02 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:8c44f4b95a232eeb20682fd642f2262a04e3e0b5045f318cb707e0ce2ed03bea
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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:2e281a4d2bfd7389c89d191a4aa38a63211e08e4bab3372985c8829dd44552df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73016020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9132ce316ff971ffcd2aa7a5c5bd64785657f898d88dfd917a3438ccaf5b702c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:01:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:13:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:13:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:13:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:13:55 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:13:55 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:13:55 GMT
USER fluent
# Wed, 17 Dec 2025 20:13:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:13:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c694792a75e7d76b490ae53980be6c2ce4fc998b1abd1475632aff8287efc`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 1.3 MB (1263015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6f6bf8da6225045c47fd91b956dedced5d22858a41d4abd24faf97bf3a73b1`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce54dc660a317ab44a20bbca82fcf472e5460a5d00afcef3157a0d661358c4`  
		Last Modified: Wed, 17 Dec 2025 20:05:49 GMT  
		Size: 37.9 MB (37906221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a63170ee86c30b036e6a19e4b2d3d7ece095f2f01bd32210c30d85fb115c84`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a81dcfbd2a86e33e6f2983a02b97705257c256b6c8d59a82f6a1c1870c1d5f`  
		Last Modified: Wed, 17 Dec 2025 20:14:16 GMT  
		Size: 5.9 MB (5900202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928044fa3186dc09088e6022988048179ee0956fa6539e4e7e777079c95941b`  
		Last Modified: Wed, 17 Dec 2025 20:14:15 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad673d7a54829730a1d99e1f482693639c90181e8dba554c614f17ae9391eb10`  
		Last Modified: Wed, 17 Dec 2025 20:14:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f53e6794061ca3f128990137a16356b70a815fc1281616fee26354fad9cf238`  
		Last Modified: Wed, 17 Dec 2025 20:14:14 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:5822791d2c146c240a6db34cf3091234b74db0c763a30cfc4a2b91f098bd76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38999837f8a8c8ec535dbe53874b8e6b31181ce2795aa6a5917d527f1415791e`

```dockerfile
```

-	Layers:
	-	`sha256:ee6f93f01dc397e5a393ec3833092a9d10645e0946184ea1e02102d2618742e5`  
		Last Modified: Wed, 17 Dec 2025 21:28:39 GMT  
		Size: 2.3 MB (2283076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db50f75d562b56c401d9d075cb4616765c5c60a312532db20c8647447a6f8f0`  
		Last Modified: Wed, 17 Dec 2025 21:28:40 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:52386d9fbca5e4b5cc088352526c0e3c4cf51be51e0f26b3603a3e07641dfd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70882759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220a27933802ea4c11ac8beef173d524db5fc07324dcb4a439b26f9e68a93de`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:07:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:07:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:10:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:10:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:10:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:10:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:13:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 21:13:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 21:13:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 21:13:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 21:13:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 21:13:20 GMT
USER fluent
# Wed, 17 Dec 2025 21:13:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 21:13:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af25235a6de2f73e167fe9d88cdb35738f38330c0c1adb0a191c1fc872a9a364`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 1.2 MB (1236507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1bb323f42cea80e196b1c113bbf05dc2ffc74c425a95add0955e6d63de14d8`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179e797e543eb082ba216f703bd38c73f866328fa552cbcf520c594c28d80306`  
		Last Modified: Wed, 17 Dec 2025 20:10:35 GMT  
		Size: 37.8 MB (37766875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c92a6a12306fa8638515dcae5b2813033ff5ffb720ea29cd55a4c2a33e8efa`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7f61ef88bae3b047c2cfc4a457c18c71c6811f2684cc81717061d6354ac9b`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 5.7 MB (5666971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea2617a74be904e505d34f84800b1264f38db650537a2e9f0e91a8270bdf71`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d71df345b8a5d1f1a637ac1bfc24f1f25d50bbece4d887a3f3aafc5bfe9971`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333971b0001af4916c9dde13bf2ae6b47f0abc68a5520106bdf314d5fdff0024`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:dbcd5fb56afa1e0e644dd7830aa1f96e9511a441854f1db4d8a8dbcc76edf221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95c721314f5ce0fa6462b3644eb511bed426d68bacc782ae9b81452b7fe36ff`

```dockerfile
```

-	Layers:
	-	`sha256:a20ad8df9e4981fb7f1004b28b0319ea519b5572f91ca2c71c18e906c4cff0eb`  
		Last Modified: Thu, 18 Dec 2025 00:28:54 GMT  
		Size: 2.3 MB (2281517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ef7f8dd08cef21651402ee0ac9d1340826bbce65c398a8da68760f7876588a`  
		Last Modified: Thu, 18 Dec 2025 00:28:55 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

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

### `fluentd:v1.19-debian-1` - unknown; unknown

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

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:73be61587891d374d3c979debd8a69f833a0f85de1eb94114b1f047bc27b7927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76212297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351f56953b1c30bd87baf457bfe140e4c16e8f8a40754ec76384ff82d6c33077`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:03:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:54 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:11:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:11:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:11:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:11:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:11:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:11:20 GMT
USER fluent
# Wed, 17 Dec 2025 20:11:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:11:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf1defef1ae1276b0248a3c76741c1891939a1305af2224f030f0be43e9db41`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 1.3 MB (1287235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cce8366db0dd679385b27b26e792754efc6013e1eda6246ee7ca02f922319a`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b00e55c71100d0de4f564dfcb1fc8490be93fe4f8103e8d52dfa969a36734`  
		Last Modified: Wed, 17 Dec 2025 20:06:12 GMT  
		Size: 37.7 MB (37660989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fc4a019eaaef42d87bc0513d35218ffa99b699068a12455d4242dcdaf38d72`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb78718a1133db063b1ce75239c860b6f2f0f6122eb5dfc1991f9641b2be050`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 6.0 MB (5968610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781fd9850d76b1d666d28ef26adb2d39c4c05eb608589dbed770ee0547e69a26`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2df57eb74f0355cd0eb5f946b505243377a86644076d239e11995bbec6d39f`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6872d4ffa7a906ea417de17f24dead0e2ef3a08572e1b8efac674ede0da3b9`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:08cfd12ad67134dcd23de31a90ae0862508c0ab3701f98bcfd15b299f48541f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aec5ba6d2aa7c291a1d4723fc3b3b42e6fa9a831d491b806449a2e2370e6a76`

```dockerfile
```

-	Layers:
	-	`sha256:3f503c9d2868e3e13b005f645397720ccdc305fd4000a78a1fe573585211f18d`  
		Last Modified: Wed, 17 Dec 2025 21:28:53 GMT  
		Size: 2.3 MB (2277293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d22ded427958d01913dcfdd1170d7f316e3dce1f47b36b13dbcb6365337bc42`  
		Last Modified: Wed, 17 Dec 2025 21:28:54 GMT  
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
$ docker pull fluentd@sha256:df866d45e9c42990004664ebbbc84a5da8226c60a6812f38e4b35c72f4427a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76710384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173e4062a59954573ad08ea80deac1a44ee4999e1b9be3718d12f03ecd9cb272`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:20:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:16 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:17 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:12:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:12:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:12:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:12:34 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:12:34 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:12:34 GMT
USER fluent
# Wed, 17 Dec 2025 20:12:34 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:12:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662846f86a973652ecbddd619140820b878a10b24d506301b3ff40bc977f649e`  
		Last Modified: Tue, 09 Dec 2025 01:23:20 GMT  
		Size: 1.3 MB (1294298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2be1d5814f3adfc26d3329bfeb07a0dbe2c41e30e37cdde13ed72d5f1998a3`  
		Last Modified: Tue, 09 Dec 2025 01:23:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04baeba94b0b05b3cf0c2e16ea2c3ac0481ca6c567133c5ca75d2542df991405`  
		Last Modified: Wed, 17 Dec 2025 20:05:43 GMT  
		Size: 39.2 MB (39205556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f033f95cdad94e516803e0f39534b1a9074ec1415305ce0c686e9285abed1d60`  
		Last Modified: Wed, 17 Dec 2025 20:05:37 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cdc8fab2b07dd1273cac69e76b0defaf389454ffd9bc8dccc4190b27d8406`  
		Last Modified: Wed, 17 Dec 2025 20:12:52 GMT  
		Size: 6.4 MB (6373737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbf8ce3f8a45fc259f69c3379222b09ffe7156593fd4b2eeec78322ec41170a`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b391fd190f6e8a6eb073e8ce5c63d71b77532e3a1cb00b9ba54cca6d4159df`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767a525eb440c984de5ff08e89df817785fb9ab54ef788bfae5d00f2cd0ee644`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b2aef20825bca4e726f8ca8ddf40961cf371e014e7a786e5005100af0b3a6636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6700b757d6ba83e04526bcd96d2f5c5ab3b3c057fef86aba3c1b971ab881158`

```dockerfile
```

-	Layers:
	-	`sha256:df7914f5a0a1b027ccec3f33313de14f71942676edacc8fb99c60c58a6a6a7e2`  
		Last Modified: Wed, 17 Dec 2025 21:29:01 GMT  
		Size: 2.3 MB (2281550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4dd252f3d08c04e4907e55e076b0eca323f1f974c5fb38d38191ab3a58c75`  
		Last Modified: Wed, 17 Dec 2025 21:29:02 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.0-1.0`

```console
$ docker pull fluentd@sha256:8c44f4b95a232eeb20682fd642f2262a04e3e0b5045f318cb707e0ce2ed03bea
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

### `fluentd:v1.19.0-1.0` - unknown; unknown

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

### `fluentd:v1.19.0-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:2e281a4d2bfd7389c89d191a4aa38a63211e08e4bab3372985c8829dd44552df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73016020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9132ce316ff971ffcd2aa7a5c5bd64785657f898d88dfd917a3438ccaf5b702c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:01:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:13:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:13:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:13:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:13:55 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:13:55 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:13:55 GMT
USER fluent
# Wed, 17 Dec 2025 20:13:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:13:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c694792a75e7d76b490ae53980be6c2ce4fc998b1abd1475632aff8287efc`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 1.3 MB (1263015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6f6bf8da6225045c47fd91b956dedced5d22858a41d4abd24faf97bf3a73b1`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce54dc660a317ab44a20bbca82fcf472e5460a5d00afcef3157a0d661358c4`  
		Last Modified: Wed, 17 Dec 2025 20:05:49 GMT  
		Size: 37.9 MB (37906221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a63170ee86c30b036e6a19e4b2d3d7ece095f2f01bd32210c30d85fb115c84`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a81dcfbd2a86e33e6f2983a02b97705257c256b6c8d59a82f6a1c1870c1d5f`  
		Last Modified: Wed, 17 Dec 2025 20:14:16 GMT  
		Size: 5.9 MB (5900202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928044fa3186dc09088e6022988048179ee0956fa6539e4e7e777079c95941b`  
		Last Modified: Wed, 17 Dec 2025 20:14:15 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad673d7a54829730a1d99e1f482693639c90181e8dba554c614f17ae9391eb10`  
		Last Modified: Wed, 17 Dec 2025 20:14:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f53e6794061ca3f128990137a16356b70a815fc1281616fee26354fad9cf238`  
		Last Modified: Wed, 17 Dec 2025 20:14:14 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5822791d2c146c240a6db34cf3091234b74db0c763a30cfc4a2b91f098bd76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38999837f8a8c8ec535dbe53874b8e6b31181ce2795aa6a5917d527f1415791e`

```dockerfile
```

-	Layers:
	-	`sha256:ee6f93f01dc397e5a393ec3833092a9d10645e0946184ea1e02102d2618742e5`  
		Last Modified: Wed, 17 Dec 2025 21:28:39 GMT  
		Size: 2.3 MB (2283076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db50f75d562b56c401d9d075cb4616765c5c60a312532db20c8647447a6f8f0`  
		Last Modified: Wed, 17 Dec 2025 21:28:40 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:52386d9fbca5e4b5cc088352526c0e3c4cf51be51e0f26b3603a3e07641dfd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70882759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220a27933802ea4c11ac8beef173d524db5fc07324dcb4a439b26f9e68a93de`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:07:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:07:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:10:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:10:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:10:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:10:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:13:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 21:13:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 21:13:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 21:13:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 21:13:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 21:13:20 GMT
USER fluent
# Wed, 17 Dec 2025 21:13:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 21:13:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af25235a6de2f73e167fe9d88cdb35738f38330c0c1adb0a191c1fc872a9a364`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 1.2 MB (1236507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1bb323f42cea80e196b1c113bbf05dc2ffc74c425a95add0955e6d63de14d8`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179e797e543eb082ba216f703bd38c73f866328fa552cbcf520c594c28d80306`  
		Last Modified: Wed, 17 Dec 2025 20:10:35 GMT  
		Size: 37.8 MB (37766875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c92a6a12306fa8638515dcae5b2813033ff5ffb720ea29cd55a4c2a33e8efa`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7f61ef88bae3b047c2cfc4a457c18c71c6811f2684cc81717061d6354ac9b`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 5.7 MB (5666971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea2617a74be904e505d34f84800b1264f38db650537a2e9f0e91a8270bdf71`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d71df345b8a5d1f1a637ac1bfc24f1f25d50bbece4d887a3f3aafc5bfe9971`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333971b0001af4916c9dde13bf2ae6b47f0abc68a5520106bdf314d5fdff0024`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:dbcd5fb56afa1e0e644dd7830aa1f96e9511a441854f1db4d8a8dbcc76edf221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95c721314f5ce0fa6462b3644eb511bed426d68bacc782ae9b81452b7fe36ff`

```dockerfile
```

-	Layers:
	-	`sha256:a20ad8df9e4981fb7f1004b28b0319ea519b5572f91ca2c71c18e906c4cff0eb`  
		Last Modified: Thu, 18 Dec 2025 00:28:54 GMT  
		Size: 2.3 MB (2281517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ef7f8dd08cef21651402ee0ac9d1340826bbce65c398a8da68760f7876588a`  
		Last Modified: Thu, 18 Dec 2025 00:28:55 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm64 variant v8

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

### `fluentd:v1.19.0-1.0` - unknown; unknown

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

### `fluentd:v1.19.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:73be61587891d374d3c979debd8a69f833a0f85de1eb94114b1f047bc27b7927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76212297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351f56953b1c30bd87baf457bfe140e4c16e8f8a40754ec76384ff82d6c33077`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:03:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:54 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:11:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:11:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:11:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:11:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:11:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:11:20 GMT
USER fluent
# Wed, 17 Dec 2025 20:11:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:11:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf1defef1ae1276b0248a3c76741c1891939a1305af2224f030f0be43e9db41`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 1.3 MB (1287235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cce8366db0dd679385b27b26e792754efc6013e1eda6246ee7ca02f922319a`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b00e55c71100d0de4f564dfcb1fc8490be93fe4f8103e8d52dfa969a36734`  
		Last Modified: Wed, 17 Dec 2025 20:06:12 GMT  
		Size: 37.7 MB (37660989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fc4a019eaaef42d87bc0513d35218ffa99b699068a12455d4242dcdaf38d72`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb78718a1133db063b1ce75239c860b6f2f0f6122eb5dfc1991f9641b2be050`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 6.0 MB (5968610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781fd9850d76b1d666d28ef26adb2d39c4c05eb608589dbed770ee0547e69a26`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2df57eb74f0355cd0eb5f946b505243377a86644076d239e11995bbec6d39f`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6872d4ffa7a906ea417de17f24dead0e2ef3a08572e1b8efac674ede0da3b9`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:08cfd12ad67134dcd23de31a90ae0862508c0ab3701f98bcfd15b299f48541f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aec5ba6d2aa7c291a1d4723fc3b3b42e6fa9a831d491b806449a2e2370e6a76`

```dockerfile
```

-	Layers:
	-	`sha256:3f503c9d2868e3e13b005f645397720ccdc305fd4000a78a1fe573585211f18d`  
		Last Modified: Wed, 17 Dec 2025 21:28:53 GMT  
		Size: 2.3 MB (2277293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d22ded427958d01913dcfdd1170d7f316e3dce1f47b36b13dbcb6365337bc42`  
		Last Modified: Wed, 17 Dec 2025 21:28:54 GMT  
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
$ docker pull fluentd@sha256:df866d45e9c42990004664ebbbc84a5da8226c60a6812f38e4b35c72f4427a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76710384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173e4062a59954573ad08ea80deac1a44ee4999e1b9be3718d12f03ecd9cb272`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:20:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:16 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:17 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:12:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:12:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:12:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:12:34 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:12:34 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:12:34 GMT
USER fluent
# Wed, 17 Dec 2025 20:12:34 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:12:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662846f86a973652ecbddd619140820b878a10b24d506301b3ff40bc977f649e`  
		Last Modified: Tue, 09 Dec 2025 01:23:20 GMT  
		Size: 1.3 MB (1294298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2be1d5814f3adfc26d3329bfeb07a0dbe2c41e30e37cdde13ed72d5f1998a3`  
		Last Modified: Tue, 09 Dec 2025 01:23:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04baeba94b0b05b3cf0c2e16ea2c3ac0481ca6c567133c5ca75d2542df991405`  
		Last Modified: Wed, 17 Dec 2025 20:05:43 GMT  
		Size: 39.2 MB (39205556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f033f95cdad94e516803e0f39534b1a9074ec1415305ce0c686e9285abed1d60`  
		Last Modified: Wed, 17 Dec 2025 20:05:37 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cdc8fab2b07dd1273cac69e76b0defaf389454ffd9bc8dccc4190b27d8406`  
		Last Modified: Wed, 17 Dec 2025 20:12:52 GMT  
		Size: 6.4 MB (6373737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbf8ce3f8a45fc259f69c3379222b09ffe7156593fd4b2eeec78322ec41170a`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b391fd190f6e8a6eb073e8ce5c63d71b77532e3a1cb00b9ba54cca6d4159df`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767a525eb440c984de5ff08e89df817785fb9ab54ef788bfae5d00f2cd0ee644`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b2aef20825bca4e726f8ca8ddf40961cf371e014e7a786e5005100af0b3a6636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6700b757d6ba83e04526bcd96d2f5c5ab3b3c057fef86aba3c1b971ab881158`

```dockerfile
```

-	Layers:
	-	`sha256:df7914f5a0a1b027ccec3f33313de14f71942676edacc8fb99c60c58a6a6a7e2`  
		Last Modified: Wed, 17 Dec 2025 21:29:01 GMT  
		Size: 2.3 MB (2281550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4dd252f3d08c04e4907e55e076b0eca323f1f974c5fb38d38191ab3a58c75`  
		Last Modified: Wed, 17 Dec 2025 21:29:02 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.1-debian-1.0`

```console
$ docker pull fluentd@sha256:8c44f4b95a232eeb20682fd642f2262a04e3e0b5045f318cb707e0ce2ed03bea
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

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.1-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:2e281a4d2bfd7389c89d191a4aa38a63211e08e4bab3372985c8829dd44552df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73016020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9132ce316ff971ffcd2aa7a5c5bd64785657f898d88dfd917a3438ccaf5b702c`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:01:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:01:59 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:09 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:09 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:09 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:09 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:09 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:13:55 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:13:55 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:13:55 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:13:55 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:13:55 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:13:55 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:13:55 GMT
USER fluent
# Wed, 17 Dec 2025 20:13:55 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:13:55 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c694792a75e7d76b490ae53980be6c2ce4fc998b1abd1475632aff8287efc`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 1.3 MB (1263015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6f6bf8da6225045c47fd91b956dedced5d22858a41d4abd24faf97bf3a73b1`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce54dc660a317ab44a20bbca82fcf472e5460a5d00afcef3157a0d661358c4`  
		Last Modified: Wed, 17 Dec 2025 20:05:49 GMT  
		Size: 37.9 MB (37906221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a63170ee86c30b036e6a19e4b2d3d7ece095f2f01bd32210c30d85fb115c84`  
		Last Modified: Wed, 17 Dec 2025 20:05:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a81dcfbd2a86e33e6f2983a02b97705257c256b6c8d59a82f6a1c1870c1d5f`  
		Last Modified: Wed, 17 Dec 2025 20:14:16 GMT  
		Size: 5.9 MB (5900202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a928044fa3186dc09088e6022988048179ee0956fa6539e4e7e777079c95941b`  
		Last Modified: Wed, 17 Dec 2025 20:14:15 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad673d7a54829730a1d99e1f482693639c90181e8dba554c614f17ae9391eb10`  
		Last Modified: Wed, 17 Dec 2025 20:14:14 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f53e6794061ca3f128990137a16356b70a815fc1281616fee26354fad9cf238`  
		Last Modified: Wed, 17 Dec 2025 20:14:14 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:5822791d2c146c240a6db34cf3091234b74db0c763a30cfc4a2b91f098bd76a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38999837f8a8c8ec535dbe53874b8e6b31181ce2795aa6a5917d527f1415791e`

```dockerfile
```

-	Layers:
	-	`sha256:ee6f93f01dc397e5a393ec3833092a9d10645e0946184ea1e02102d2618742e5`  
		Last Modified: Wed, 17 Dec 2025 21:28:39 GMT  
		Size: 2.3 MB (2283076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db50f75d562b56c401d9d075cb4616765c5c60a312532db20c8647447a6f8f0`  
		Last Modified: Wed, 17 Dec 2025 21:28:40 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:52386d9fbca5e4b5cc088352526c0e3c4cf51be51e0f26b3603a3e07641dfd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70882759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4220a27933802ea4c11ac8beef173d524db5fc07324dcb4a439b26f9e68a93de`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:07:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:07:29 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:10:11 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:10:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:10:11 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:10:11 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:10:11 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:10:11 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 21:13:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 21:13:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 21:13:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 21:13:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 21:13:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 21:13:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 21:13:20 GMT
USER fluent
# Wed, 17 Dec 2025 21:13:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 21:13:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af25235a6de2f73e167fe9d88cdb35738f38330c0c1adb0a191c1fc872a9a364`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 1.2 MB (1236507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1bb323f42cea80e196b1c113bbf05dc2ffc74c425a95add0955e6d63de14d8`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179e797e543eb082ba216f703bd38c73f866328fa552cbcf520c594c28d80306`  
		Last Modified: Wed, 17 Dec 2025 20:10:35 GMT  
		Size: 37.8 MB (37766875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c92a6a12306fa8638515dcae5b2813033ff5ffb720ea29cd55a4c2a33e8efa`  
		Last Modified: Wed, 17 Dec 2025 20:10:27 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d7f61ef88bae3b047c2cfc4a457c18c71c6811f2684cc81717061d6354ac9b`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 5.7 MB (5666971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea2617a74be904e505d34f84800b1264f38db650537a2e9f0e91a8270bdf71`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d71df345b8a5d1f1a637ac1bfc24f1f25d50bbece4d887a3f3aafc5bfe9971`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333971b0001af4916c9dde13bf2ae6b47f0abc68a5520106bdf314d5fdff0024`  
		Last Modified: Wed, 17 Dec 2025 21:13:40 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:dbcd5fb56afa1e0e644dd7830aa1f96e9511a441854f1db4d8a8dbcc76edf221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95c721314f5ce0fa6462b3644eb511bed426d68bacc782ae9b81452b7fe36ff`

```dockerfile
```

-	Layers:
	-	`sha256:a20ad8df9e4981fb7f1004b28b0319ea519b5572f91ca2c71c18e906c4cff0eb`  
		Last Modified: Thu, 18 Dec 2025 00:28:54 GMT  
		Size: 2.3 MB (2281517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ef7f8dd08cef21651402ee0ac9d1340826bbce65c398a8da68760f7876588a`  
		Last Modified: Thu, 18 Dec 2025 00:28:55 GMT  
		Size: 21.4 KB (21426 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.1-debian-1.0` - linux; arm64 variant v8

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

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

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

### `fluentd:v1.19.1-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:73be61587891d374d3c979debd8a69f833a0f85de1eb94114b1f047bc27b7927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76212297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:351f56953b1c30bd87baf457bfe140e4c16e8f8a40754ec76384ff82d6c33077`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Wed, 17 Dec 2025 20:03:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 17 Dec 2025 20:03:28 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:53 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:53 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:53 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:53 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:54 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:54 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:11:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:11:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:11:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:11:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:11:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:11:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:11:20 GMT
USER fluent
# Wed, 17 Dec 2025 20:11:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:11:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf1defef1ae1276b0248a3c76741c1891939a1305af2224f030f0be43e9db41`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 1.3 MB (1287235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cce8366db0dd679385b27b26e792754efc6013e1eda6246ee7ca02f922319a`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b00e55c71100d0de4f564dfcb1fc8490be93fe4f8103e8d52dfa969a36734`  
		Last Modified: Wed, 17 Dec 2025 20:06:12 GMT  
		Size: 37.7 MB (37660989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fc4a019eaaef42d87bc0513d35218ffa99b699068a12455d4242dcdaf38d72`  
		Last Modified: Wed, 17 Dec 2025 20:06:09 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb78718a1133db063b1ce75239c860b6f2f0f6122eb5dfc1991f9641b2be050`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 6.0 MB (5968610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781fd9850d76b1d666d28ef26adb2d39c4c05eb608589dbed770ee0547e69a26`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2df57eb74f0355cd0eb5f946b505243377a86644076d239e11995bbec6d39f`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6872d4ffa7a906ea417de17f24dead0e2ef3a08572e1b8efac674ede0da3b9`  
		Last Modified: Wed, 17 Dec 2025 20:11:35 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:08cfd12ad67134dcd23de31a90ae0862508c0ab3701f98bcfd15b299f48541f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2298580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aec5ba6d2aa7c291a1d4723fc3b3b42e6fa9a831d491b806449a2e2370e6a76`

```dockerfile
```

-	Layers:
	-	`sha256:3f503c9d2868e3e13b005f645397720ccdc305fd4000a78a1fe573585211f18d`  
		Last Modified: Wed, 17 Dec 2025 21:28:53 GMT  
		Size: 2.3 MB (2277293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d22ded427958d01913dcfdd1170d7f316e3dce1f47b36b13dbcb6365337bc42`  
		Last Modified: Wed, 17 Dec 2025 21:28:54 GMT  
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
$ docker pull fluentd@sha256:df866d45e9c42990004664ebbbc84a5da8226c60a6812f38e4b35c72f4427a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76710384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173e4062a59954573ad08ea80deac1a44ee4999e1b9be3718d12f03ecd9cb272`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 01:20:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:20:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 17 Dec 2025 20:05:16 GMT
ENV LANG=C.UTF-8
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_VERSION=3.4.8
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.8.tar.xz
# Wed, 17 Dec 2025 20:05:16 GMT
ENV RUBY_DOWNLOAD_SHA256=53a8ec71111449cbbd42224d8d27c493fa6ded228636731051c48604d4255d68
# Wed, 17 Dec 2025 20:05:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='20a06e644b0d9bd2fbdbfd52d42540bdde820ea7df86e92e533c073da0cdd43c' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.28.2/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='e3853c5a252fca15252d07cb23a1bdd9377a8c6f3efa01531109281ae47f841c' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.91.1' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 17 Dec 2025 20:05:16 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:16 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 17 Dec 2025 20:05:16 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Dec 2025 20:05:17 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 17 Dec 2025 20:05:17 GMT
CMD ["irb"]
# Wed, 17 Dec 2025 20:12:34 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Wed, 17 Dec 2025 20:12:34 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Wed, 17 Dec 2025 20:12:34 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
COPY entrypoint.sh /bin/ # buildkit
# Wed, 17 Dec 2025 20:12:34 GMT
ENV FLUENTD_CONF=fluent.conf
# Wed, 17 Dec 2025 20:12:34 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Wed, 17 Dec 2025 20:12:34 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Wed, 17 Dec 2025 20:12:34 GMT
USER fluent
# Wed, 17 Dec 2025 20:12:34 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Wed, 17 Dec 2025 20:12:34 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662846f86a973652ecbddd619140820b878a10b24d506301b3ff40bc977f649e`  
		Last Modified: Tue, 09 Dec 2025 01:23:20 GMT  
		Size: 1.3 MB (1294298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2be1d5814f3adfc26d3329bfeb07a0dbe2c41e30e37cdde13ed72d5f1998a3`  
		Last Modified: Tue, 09 Dec 2025 01:23:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04baeba94b0b05b3cf0c2e16ea2c3ac0481ca6c567133c5ca75d2542df991405`  
		Last Modified: Wed, 17 Dec 2025 20:05:43 GMT  
		Size: 39.2 MB (39205556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f033f95cdad94e516803e0f39534b1a9074ec1415305ce0c686e9285abed1d60`  
		Last Modified: Wed, 17 Dec 2025 20:05:37 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222cdc8fab2b07dd1273cac69e76b0defaf389454ffd9bc8dccc4190b27d8406`  
		Last Modified: Wed, 17 Dec 2025 20:12:52 GMT  
		Size: 6.4 MB (6373737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbf8ce3f8a45fc259f69c3379222b09ffe7156593fd4b2eeec78322ec41170a`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b391fd190f6e8a6eb073e8ce5c63d71b77532e3a1cb00b9ba54cca6d4159df`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767a525eb440c984de5ff08e89df817785fb9ab54ef788bfae5d00f2cd0ee644`  
		Last Modified: Wed, 17 Dec 2025 20:12:51 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.1-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b2aef20825bca4e726f8ca8ddf40961cf371e014e7a786e5005100af0b3a6636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6700b757d6ba83e04526bcd96d2f5c5ab3b3c057fef86aba3c1b971ab881158`

```dockerfile
```

-	Layers:
	-	`sha256:df7914f5a0a1b027ccec3f33313de14f71942676edacc8fb99c60c58a6a6a7e2`  
		Last Modified: Wed, 17 Dec 2025 21:29:01 GMT  
		Size: 2.3 MB (2281550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec4dd252f3d08c04e4907e55e076b0eca323f1f974c5fb38d38191ab3a58c75`  
		Last Modified: Wed, 17 Dec 2025 21:29:02 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
