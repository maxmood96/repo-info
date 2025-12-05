## `fluentd:latest`

```console
$ docker pull fluentd@sha256:00aeea8046975151285dee7de06f37fbca859a48dd9afa6b948ae7f13ba28e59
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
$ docker pull fluentd@sha256:6240494942204615ec7b6afc505afe5251fd9447b9f97aa1d15147b3c101433f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79219006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd66d9d1a7d5268d13f4c183c9e2f0baffbc451a07a95d3a92aa413b15629db7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 06:00:57 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 06:03:23 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 06:03:23 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:03:23 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 06:03:23 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 18:58:44 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 04 Dec 2025 18:58:44 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Thu, 04 Dec 2025 18:58:44 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 04 Dec 2025 18:58:45 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 04 Dec 2025 18:58:45 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 04 Dec 2025 18:58:45 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 04 Dec 2025 18:58:45 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 04 Dec 2025 18:58:45 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 04 Dec 2025 18:58:45 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 04 Dec 2025 18:58:45 GMT
USER fluent
# Thu, 04 Dec 2025 18:58:45 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 04 Dec 2025 18:58:45 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb0562513a544d09b243cd53af17176ae058cdb46bab21dc80e6e0e176085ac`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 1.3 MB (1279393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2995c07ae76a079f87ad5194b6ae8ae189e2697989ee2ec3ff402c4bbdbaef98`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a8b74c7e9beb752e09eab60f51bfed7d4156be9c8a4cb31e65c1c593e477ad`  
		Last Modified: Tue, 18 Nov 2025 06:03:40 GMT  
		Size: 42.2 MB (42158682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50951878876ddf823dfebd9e0c1677361d53bec1ff62831466fd280b78c485e7`  
		Last Modified: Tue, 18 Nov 2025 06:03:38 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72585dd7596a87134366b4811336b292df351eb34419901e60defb1c412033a5`  
		Last Modified: Thu, 04 Dec 2025 18:59:08 GMT  
		Size: 6.0 MB (6002049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d21ae1bbd8cf7a5c81316fadc4c1d605148b8f29723da71bf2c957621f4b22`  
		Last Modified: Thu, 04 Dec 2025 18:59:07 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8fa2be93123d4ff3aaff45b160afa29dd535164e2fd743708e5c83ee822cf0`  
		Last Modified: Thu, 04 Dec 2025 18:59:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ccca90a00656c889b24dad43ee644103f1f035b2f65ce35b0f34d35451734c`  
		Last Modified: Thu, 04 Dec 2025 18:59:07 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:84fb8d8f71409aa4324f6d008d4a031861d8ec48f2cdd687031c4d9f1d0c01d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85d48d5d59e2d36d878a10af83b710812f3818fc348bf1863aca8c57d246639`

```dockerfile
```

-	Layers:
	-	`sha256:d37abc9e254151598cd02552918a94209b0571d5807e8e2354767fee2d26f799`  
		Last Modified: Thu, 04 Dec 2025 21:28:40 GMT  
		Size: 2.3 MB (2280658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e35172fe75a5483bc13670bb98f415318c4559e767f1a20689dff3cf3360c73`  
		Last Modified: Thu, 04 Dec 2025 21:28:41 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:aaebbb2d9630e58872361a78ea08ff2f9fd24ccb3c1144b05466e656087c1382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73104845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20088dbd13800e95c34338237e95cdad749f7d4f04f80ddf0604a06ed4eaf907`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:18:53 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:21:56 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:21:56 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:21:56 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:21:56 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 19:00:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 04 Dec 2025 19:00:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Thu, 04 Dec 2025 19:00:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 04 Dec 2025 19:00:20 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 04 Dec 2025 19:00:20 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 04 Dec 2025 19:00:20 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 04 Dec 2025 19:00:20 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 04 Dec 2025 19:00:20 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 04 Dec 2025 19:00:20 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 04 Dec 2025 19:00:20 GMT
USER fluent
# Thu, 04 Dec 2025 19:00:20 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 04 Dec 2025 19:00:20 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8bddf98d29f007597c2419ece53918ed2a02b6807f244eba291b11a115ce2f`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 1.3 MB (1263024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce6e0d17644462250ed0239ef347ef83d3d46d91cc236e61f5d1ee58840ebe6`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dba72f3360e3a96295c7cea72647313a78f2723776a3e529d977bc6fb38431`  
		Last Modified: Tue, 18 Nov 2025 04:22:15 GMT  
		Size: 38.0 MB (37994184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0930b6e7a3909c3d28136a1cc19c3a553fbbb2a2d33988cd25bd43effa0a140`  
		Last Modified: Tue, 18 Nov 2025 04:22:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be6bc7b989da34f73dc506d83cb9f48c37ee8105fe87bd7f52bca4542d7cee2`  
		Last Modified: Thu, 04 Dec 2025 19:00:42 GMT  
		Size: 5.9 MB (5901093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c6f3399ef20bf6be1ed6a2ca72c0a24e3ad0d84b16a9ef8a0709e1c7659f8f`  
		Last Modified: Thu, 04 Dec 2025 19:00:41 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70663e3166cf0a7abf84c4ed0eafa32f04846e2058e90a97ac3e06d24369d32`  
		Last Modified: Thu, 04 Dec 2025 19:00:41 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56bfbe0d3c92ea6b9ebb1c97197ffb757b2487720ce3d2ab6a5a0538ad7bf5b`  
		Last Modified: Thu, 04 Dec 2025 19:00:41 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:248114ee7add057b9522b312fa3eef5e127b5ce66321a1c70af7ebcf0361e2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb431f17e2b58f86b090040b8d1cbac7f7a09a0eb6151fd7d76271ab122db28d`

```dockerfile
```

-	Layers:
	-	`sha256:1253a50e411a8bc80c1968d6d9653822decb6287cafc575af11b24f9ca7d9304`  
		Last Modified: Thu, 04 Dec 2025 21:28:45 GMT  
		Size: 2.3 MB (2283629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6d735f6d01c1fac1cdb270eb1066ee221e9e96a36d6d1970722e33bce8fd801`  
		Last Modified: Thu, 04 Dec 2025 21:28:46 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:19368b5ced494adadbccad66e2b3d118db4c880ed6a2159f28dc54906d309884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70983027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4b6c0c43b2bade13a1281582e1f172afddcb1d640eabe2965dbe6d7f4cc2d4`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:59:14 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:01:55 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:01:55 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:01:55 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:01:55 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 19:00:07 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 04 Dec 2025 19:00:07 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Thu, 04 Dec 2025 19:00:07 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 04 Dec 2025 19:00:07 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 04 Dec 2025 19:00:08 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 04 Dec 2025 19:00:08 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 04 Dec 2025 19:00:08 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 04 Dec 2025 19:00:08 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 04 Dec 2025 19:00:08 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 04 Dec 2025 19:00:08 GMT
USER fluent
# Thu, 04 Dec 2025 19:00:08 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 04 Dec 2025 19:00:08 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64d8370801a134071a40fe32d3d2fa7e0e17d18b25e5289e7237638fa8e7778`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 1.2 MB (1236519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926b3223558fcb7b7da07de149d35cb77b0270a5ab9574f7885d63190a335526`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0053f0fd615ae9d3957c571c9b6d06b6a892f68a64ba86fcf53aa1540117bbac`  
		Last Modified: Tue, 18 Nov 2025 05:02:15 GMT  
		Size: 37.9 MB (37865819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f081e8cb5f13e31c833ade5ef8bd8bc86005b1083ad01fb5c19150cfe1b852`  
		Last Modified: Tue, 18 Nov 2025 05:02:10 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0deaf0ae9760f48e1ab076a5e92832ce7edb015a71b9617c411340ed2fabe3`  
		Last Modified: Thu, 04 Dec 2025 19:00:41 GMT  
		Size: 5.7 MB (5668328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a918df6a39f29e19adc2cfe7099cb1847628765d58e9f51891b9f7137ee0b33f`  
		Last Modified: Thu, 04 Dec 2025 19:00:40 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e71a32294b22c81555f0bda1421dd249067a446ecc482b86b1956785045a4ff`  
		Last Modified: Thu, 04 Dec 2025 19:00:40 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4645e19fd544b5af4ead15a19a0f7cb149338c69fe9e9cbb6765a8231b1afb9`  
		Last Modified: Thu, 04 Dec 2025 19:00:40 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:b33da86ad731f86d80dc973681026b8a368e7c5c123c8c652c25b2b67c383343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc49d110e1779f25424b64b75f867f39c651900ae1b12fc1badd05db7f4a56ee`

```dockerfile
```

-	Layers:
	-	`sha256:edc79561200a3cdc3d20f9abf1bf47a6fd9495dc898880e298c463f493da599c`  
		Last Modified: Thu, 04 Dec 2025 21:28:51 GMT  
		Size: 2.3 MB (2282070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e1c082bb1301e59ae044904c59fece993b0c269294fb4ebb29e5eba628915f1`  
		Last Modified: Thu, 04 Dec 2025 21:28:53 GMT  
		Size: 21.4 KB (21427 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:dad79d06105b9950b09ae6c76013f79685999c3df9cf739b0ab0d1e99ab90cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79536779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2d5d26e7dec9ed23e9d93d0f2e1be085b1eaab727fc6711b593b09c4c4723a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:45:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:45:58 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 04:48:38 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 04:48:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 04:48:38 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 04:48:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:48:39 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 04:48:39 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 18:59:13 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 04 Dec 2025 18:59:13 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Thu, 04 Dec 2025 18:59:13 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 04 Dec 2025 18:59:14 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 04 Dec 2025 18:59:14 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 04 Dec 2025 18:59:14 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 04 Dec 2025 18:59:14 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 04 Dec 2025 18:59:14 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 04 Dec 2025 18:59:14 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 04 Dec 2025 18:59:14 GMT
USER fluent
# Thu, 04 Dec 2025 18:59:14 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 04 Dec 2025 18:59:14 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623192602c00e918197dfe6e2a1def0175e7be0d446a268ed38b6b5a621d38e0`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 1.3 MB (1261685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5fe6e2e9edffda349665022b4300b140e6a85f15a0f7614134df0867bcd551`  
		Last Modified: Tue, 18 Nov 2025 04:48:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c522fdb9fff298474b76a11223cdcb250793d0c701b8cf389c0375800c7d5c`  
		Last Modified: Tue, 18 Nov 2025 04:48:57 GMT  
		Size: 42.1 MB (42145706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3907ba9f7c5e39a58b009710a158a43136020eb8b46dc729f4426b65e03945ab`  
		Last Modified: Tue, 18 Nov 2025 04:48:54 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62078078c49a19cbd32c8398ca08eb739eba2a5c8f7e3ec2cc12e2f4b8c3b2db`  
		Last Modified: Thu, 04 Dec 2025 18:59:44 GMT  
		Size: 6.0 MB (5988380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e731dcc3a52a3e4926909f34921ae4f16049058441be34d00049373c20519d`  
		Last Modified: Thu, 04 Dec 2025 18:59:46 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999b33ee39bc926af8f4930b89aa17f0a6b820c5ffa7479e1bfbe6d7c3b7509e`  
		Last Modified: Thu, 04 Dec 2025 18:59:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c311d60c665f9b731977ba41c34e0d299143e31b5709d86dda8eb3f392a54e6`  
		Last Modified: Thu, 04 Dec 2025 18:59:45 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:06771e235a93cdf7216de411468857b8d19c5b37a9904e274f563c4f84e8a9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2302387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bbb2a23905b39c605e81cd2c26ddfe82db37d5659170919172cbdfe9b8819f`

```dockerfile
```

-	Layers:
	-	`sha256:7eedf47456bd91301c20eb29396d34c6238567229f91c78d64a84385ba5b5c9b`  
		Last Modified: Thu, 04 Dec 2025 21:28:57 GMT  
		Size: 2.3 MB (2280930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f02e697a3cb8e25e5f9c19892fe981d521d4b20a5ae978535af0a692e681d6e4`  
		Last Modified: Thu, 04 Dec 2025 21:28:57 GMT  
		Size: 21.5 KB (21457 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:56c84a09c3ec5836ff8a1ecd8ebda47efc0d785ee4719a2920828714257f476c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76296093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341497361633166c5f1384541265cc4c337cdbd3c29ac2d729d25563dc2b4817`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 03:40:43 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 03:43:12 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 03:43:12 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 03:43:12 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 03:43:12 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 18:58:01 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 04 Dec 2025 18:58:01 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Thu, 04 Dec 2025 18:58:01 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 04 Dec 2025 18:58:01 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 04 Dec 2025 18:58:01 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 04 Dec 2025 18:58:01 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 04 Dec 2025 18:58:01 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 04 Dec 2025 18:58:01 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 04 Dec 2025 18:58:01 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 04 Dec 2025 18:58:01 GMT
USER fluent
# Thu, 04 Dec 2025 18:58:01 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 04 Dec 2025 18:58:01 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486bef966be95a2220ea41b52e0e83a8a622f90c5f320368a5f0d7284a00c503`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 1.3 MB (1287214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f45ed37d5457ae44f5b9a372ecc7bde1dd97d5be333bac0f4030719c7f0eca`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402fa9c5b261b8af75a607827e3e965cc7ce4351d91e3eba319a98783514bc3d`  
		Last Modified: Tue, 18 Nov 2025 03:43:29 GMT  
		Size: 37.7 MB (37740240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3646abfea40cabe9f48dabaff87823bc4de7febc7191871f992e8cdd29e5cc`  
		Last Modified: Tue, 18 Nov 2025 03:43:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee570408516d44060c51273b5d738a6205bde32c3fc376fd9ef14e4a4457dce`  
		Last Modified: Thu, 04 Dec 2025 18:58:23 GMT  
		Size: 6.0 MB (5973173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6275cd6a8a20192011b6e7b4404598eec9c28328967093f4ff56a0ed65ccaa13`  
		Last Modified: Thu, 04 Dec 2025 18:58:22 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b1d8dffa356f70d09c25d0a422654add5b105c3303262e90e092f928c0476`  
		Last Modified: Thu, 04 Dec 2025 18:58:22 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3b55019ddd93dad3e462ed7516328b0c240a97a4b8c4a23e529ed5be7854ad`  
		Last Modified: Thu, 04 Dec 2025 18:58:22 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:744c888b5dc6510967c83cc08cbce6f8dc8d337314c61a7a7dfbf1d1291665fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ee20af4a982057aade0f5e6c1d71ab447ef9f7b85bbff621c4e002211248bfa`

```dockerfile
```

-	Layers:
	-	`sha256:ffd30fcff8d76a898b59a12fe9d10b319b7a244e1cfb260572d112cd4569634c`  
		Last Modified: Thu, 04 Dec 2025 21:29:01 GMT  
		Size: 2.3 MB (2277846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e78909919782d8821393c595f47c30f5265a082863f5fc58e35484d98e0ca2a`  
		Last Modified: Thu, 04 Dec 2025 21:29:02 GMT  
		Size: 21.3 KB (21287 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:4356af620d578f7b734708e4822e0ce0cd9fe1f5b8a7143b1d002b717cb601ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81024475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b8076295bf7aff1ef9394f79e5a29c35e2369e88e4eb47a173016d50bcf0d27`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Wed, 19 Nov 2025 00:28:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Wed, 19 Nov 2025 00:28:26 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV LANG=C.UTF-8
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_VERSION=3.4.7
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Wed, 19 Nov 2025 00:42:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Wed, 19 Nov 2025 00:42:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Wed, 19 Nov 2025 00:42:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Wed, 19 Nov 2025 00:42:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Nov 2025 00:42:47 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Wed, 19 Nov 2025 00:42:47 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 19:00:20 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 04 Dec 2025 19:00:20 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Thu, 04 Dec 2025 19:00:20 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 04 Dec 2025 19:00:21 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 04 Dec 2025 19:00:21 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 04 Dec 2025 19:00:21 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 04 Dec 2025 19:00:21 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 04 Dec 2025 19:00:21 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 04 Dec 2025 19:00:21 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 04 Dec 2025 19:00:21 GMT
USER fluent
# Thu, 04 Dec 2025 19:00:21 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 04 Dec 2025 19:00:21 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbe0cbe7af169b8d7859f452f051f576ef4653fffd19a193922bbf502224d54`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 1.3 MB (1309674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e697a0a74191697331846ecf6cc860ffede09eafae29280e1dd04f2379b2dc07`  
		Last Modified: Wed, 19 Nov 2025 00:33:02 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1a0cff339fe641e08a65a97169cbbb4be8d7c4819ff50a706f2ed826916747`  
		Last Modified: Wed, 19 Nov 2025 00:43:23 GMT  
		Size: 39.6 MB (39601439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923e173b58f16848269bd5ce9e04bacdfaffeebd5dac19f837456978574583d6`  
		Last Modified: Wed, 19 Nov 2025 00:43:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0919a84d847589a19c306a2e713ff5fcbb69496e0ecdc0c3ae20b20a9ee5f7d`  
		Last Modified: Thu, 04 Dec 2025 19:00:56 GMT  
		Size: 6.5 MB (6514104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abed4a44915c395254058f27e40fc64c361c740620d399ac5bab681f1162f842`  
		Last Modified: Thu, 04 Dec 2025 19:00:53 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3112cfcd01f1688ffe2f05b713ff0913349c3edf9a757c70e421f63de5aa96d`  
		Last Modified: Thu, 04 Dec 2025 19:00:53 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd859a8b16a3a21d4c4d86d8806ed52010d2b7fa101dd7f506e211559d40539`  
		Last Modified: Thu, 04 Dec 2025 19:00:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:0d89113916b32c598de029868776a0abbf0be9b9054737578c9f96ee45f67d4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91cac08bd9ebebed7eee4012b62adcb23201f4a680c1a78e81f07cdc4f043922`

```dockerfile
```

-	Layers:
	-	`sha256:a216f2032cca520353440d0327487b61906447910dffc3094b0452a6e3911baa`  
		Last Modified: Thu, 04 Dec 2025 21:29:06 GMT  
		Size: 2.3 MB (2284193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23dd6d4baac5ea6b50bcf5dcdb206d9b51e3216777fd40511fba12a56e3ea6c3`  
		Last Modified: Thu, 04 Dec 2025 21:29:07 GMT  
		Size: 21.4 KB (21377 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:ed187389e39640b36c3ce9981c1cf8dd26a754d7f04203e455789fde6d108294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76792846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee430e9e1c0931135d40bd46f138b5f92d4fcd73fa1892a2b40a65ba99b8142d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 05:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 05:14:25 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_VERSION=3.4.7
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.7.tar.xz
# Tue, 18 Nov 2025 05:16:46 GMT
ENV RUBY_DOWNLOAD_SHA256=db425a86f6e07546957578f4946cc700a91e7fd51115a86c56e096f30e0530c7
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		libgdbm-dev 		ruby 		autoconf 		bzip2 		g++ 		gcc 		libbz2-dev 		libffi-dev 		libgdbm-compat-dev 		libglib2.0-dev 		libgmp-dev 		libncurses-dev 		libssl-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		wget 		xz-utils 		zlib1g-dev 	; 		rustArch=; 	dpkgArch="$(dpkg --print-architecture)"; 	case "$dpkgArch" in 		'amd64') rustArch='x86_64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/x86_64-unknown-linux-gnu/rustup-init'; rustupSha256='6aeece6993e902708983b209d04c0d1dbb14ebb405ddb87def578d41f920f56d' ;; 		'arm64') rustArch='aarch64-unknown-linux-gnu'; rustupUrl='https://static.rust-lang.org/rustup/archive/1.27.1/aarch64-unknown-linux-gnu/rustup-init'; rustupSha256='1cffbf51e63e634c746f741de50649bbbcbd9dbe1de363c9ecef64e278dba2b2' ;; 	esac; 		if [ -n "$rustArch" ]; then 		mkdir -p /tmp/rust; 				wget -O /tmp/rust/rustup-init "$rustupUrl"; 		echo "$rustupSha256 */tmp/rust/rustup-init" | sha256sum --check --strict; 		chmod +x /tmp/rust/rustup-init; 				export RUSTUP_HOME='/tmp/rust/rustup' CARGO_HOME='/tmp/rust/cargo'; 		export PATH="$CARGO_HOME/bin:$PATH"; 		/tmp/rust/rustup-init -y --no-modify-path --profile minimal --default-toolchain '1.84.0' --default-host "$rustArch"; 				rustc --version; 		cargo --version; 	fi; 		wget -O ruby.tar.xz "$RUBY_DOWNLOAD_URL"; 	echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum --check --strict; 		mkdir -p /usr/src/ruby; 	tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1; 	rm ruby.tar.xz; 		cd /usr/src/ruby; 		autoconf; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 		${rustArch:+--enable-yjit} 	; 	make -j "$(nproc)"; 	make install; 		rm -rf /tmp/rust; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		cd /; 	rm -r /usr/src/ruby; 	if dpkg -l | grep -i ruby; then exit 1; fi; 	[ "$(command -v ruby)" = '/usr/local/bin/ruby' ]; 	ruby --version; 	gem --version; 	bundle --version # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 18 Nov 2025 05:16:46 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 05:16:46 GMT
RUN set -eux; 	mkdir "$GEM_HOME"; 	chmod 1777 "$GEM_HOME" # buildkit
# Tue, 18 Nov 2025 05:16:46 GMT
CMD ["irb"]
# Thu, 04 Dec 2025 19:00:22 GMT
LABEL maintainer=Fluentd developers <fluentd@googlegroups.com>
# Thu, 04 Dec 2025 19:00:22 GMT
LABEL Description=Fluentd docker image Vendor=Fluent Organization Version=1.19.1
# Thu, 04 Dec 2025 19:00:22 GMT
RUN apt-get update  && apt-get install -y --no-install-recommends             ca-certificates tini  && buildDeps="       make gcc g++ libc-dev       wget bzip2 gnupg dirmngr     "  && apt-get install -y --no-install-recommends $buildDeps  && echo 'gem: --no-document' >> /etc/gemrc  && export MAKEFLAGS=-j$(nproc)  && gem install oj -v 3.16.11  && gem install json -v 2.13.2  && gem install rexml -v 3.4.4  && gem install async -v 2.24.0  && gem install async-http -v 0.89.0  && gem install fluentd -v 1.19.1  && unset MAKEFLAGS  && export GEM_DIR=$(ruby -e 'puts Gem.dir')  && echo GEM_DIR=$GEM_DIR  && rm -rf $GEM_DIR/cache/*.gem  && find $GEM_DIR -maxdepth 3 -type d -name test -or -name ext -or -name spec -or -name benchmark | xargs -r rm -rfv  && find $GEM_DIR -name "*.so" | xargs -r strip  && dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"  && wget -O /tmp/jemalloc-5.3.0.tar.bz2 https://github.com/jemalloc/jemalloc/releases/download/5.3.0/jemalloc-5.3.0.tar.bz2  && cd /tmp && tar -xjf jemalloc-5.3.0.tar.bz2 --no-same-owner && cd jemalloc-5.3.0/  && (echo "je_cv_madv_free=no" > config.cache) && ./configure -C && make  && mv lib/libjemalloc.so.2 /usr/lib  && apt-get purge -y --auto-remove                   -o APT::AutoRemove::RecommendsImportant=false                   $buildDeps                   '*-dev'  && rm -rf /var/lib/apt/lists/*  && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 04 Dec 2025 19:00:22 GMT
RUN groupadd -r fluent && useradd -r -g fluent fluent     && mkdir -p /fluentd/log     && mkdir -p /fluentd/etc /fluentd/plugins     && chown -R fluent /fluentd && chgrp -R fluent /fluentd # buildkit
# Thu, 04 Dec 2025 19:00:23 GMT
COPY fluent.conf /fluentd/etc/ # buildkit
# Thu, 04 Dec 2025 19:00:23 GMT
COPY entrypoint.sh /bin/ # buildkit
# Thu, 04 Dec 2025 19:00:23 GMT
ENV FLUENTD_CONF=fluent.conf
# Thu, 04 Dec 2025 19:00:23 GMT
ENV LD_PRELOAD=/usr/lib/libjemalloc.so.2
# Thu, 04 Dec 2025 19:00:23 GMT
EXPOSE map[24224/tcp:{} 5140/tcp:{}]
# Thu, 04 Dec 2025 19:00:23 GMT
USER fluent
# Thu, 04 Dec 2025 19:00:23 GMT
ENTRYPOINT ["tini" "--" "/bin/entrypoint.sh"]
# Thu, 04 Dec 2025 19:00:23 GMT
CMD ["fluentd"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5be0006390772cf7f9022344d107d52c9454ddfb26a9b6aa53e4f77a9bdc5e`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 1.3 MB (1294253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df3437f72c81d0de5473522e48eb46cf20ee4ae5ae981dfae54b48d71b07c5f`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f67960768c1f544671789085d4901deaf00ad13d073997065fbd38e41baef3e`  
		Last Modified: Tue, 18 Nov 2025 05:17:09 GMT  
		Size: 39.3 MB (39287189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22de67f11ad5b13189744a053b706d6a38590793d5b547a05561143636a6e794`  
		Last Modified: Tue, 18 Nov 2025 05:17:06 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dae3e7995bd0deb7b55500a6bd72b6da73d79ec0e7c0311d2a8ffe3b3a07937`  
		Last Modified: Thu, 04 Dec 2025 19:00:57 GMT  
		Size: 6.4 MB (6374635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44422c1d3698300c20c8d82b912869f2db389e052786cf236d58d4c070a52bb6`  
		Last Modified: Thu, 04 Dec 2025 19:00:55 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac31f9e4d8d6111baff1810add02a698b16ee337ebae0e5a04bccd34dc3d1007`  
		Last Modified: Thu, 04 Dec 2025 19:00:55 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f174a509e3b7c1f6a3be616887aede378dae2a6ff15ad0eecd695f67d8461275`  
		Last Modified: Thu, 04 Dec 2025 19:00:55 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:0dadfa6115c306234fc61d311151598224464a5b584da6589aa5d497360139a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f29918cffd01b2c59af6e28e2e0b4917359f9a0f89eda0ac5c64dd59b7dfb1e`

```dockerfile
```

-	Layers:
	-	`sha256:c79cd4563cae1c78685f758473a2ceab79b121ee11e164da1e6b7ab447e0d552`  
		Last Modified: Thu, 04 Dec 2025 21:29:11 GMT  
		Size: 2.3 MB (2282103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a21fae52c306fa690f842976aaaa9c786f47c33a5a87fa92d845c843d5e94942`  
		Last Modified: Thu, 04 Dec 2025 21:29:13 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
