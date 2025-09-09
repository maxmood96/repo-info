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
$ docker pull fluentd@sha256:406eab0c90b337ea508a282d4917b61d046b740c7387c1dbb82c187e0b3d3716
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
$ docker pull fluentd@sha256:ba2a2644e30105d97209fa493cd9f9975f852353f7e4cffe9d67a2136fbea108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79117410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40476c6d4a4d9a86b707cf50405ed9380e4ec5b117499123be9cc96fb1c6165a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907bb64ed55e33da933ebd9b77bfa9382670074deb815d2e0d4f7d3067842ed1`  
		Last Modified: Mon, 08 Sep 2025 22:08:24 GMT  
		Size: 1.3 MB (1277837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676f670b77091f6f737a85b5792a0639bc680e827f931c13cb7e2fbfd0a38ebe`  
		Last Modified: Mon, 08 Sep 2025 22:08:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631f0e31bb9254d7f56d53693835aeb8d61c1c864ab85670b8997fb62d740e4f`  
		Last Modified: Mon, 08 Sep 2025 22:08:30 GMT  
		Size: 42.0 MB (42036169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836288d7f92195b5daec740a66ff4dbb4b6df0742d4a949a8892d634d98e848`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbaeb18472eaacfce9887b025572c879a5fdb37ef68212abe07046d303bd94f`  
		Last Modified: Mon, 08 Sep 2025 23:28:31 GMT  
		Size: 6.0 MB (6027518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7db22461d213e9de126e16bfc9c9ba9314204a0e3d6112828ac67310a6c22c`  
		Last Modified: Mon, 08 Sep 2025 22:52:04 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15320385f8b32e2c3cac705007a3fca3bf191963c690b6f79b18d84be24ea1f7`  
		Last Modified: Mon, 08 Sep 2025 22:52:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347687b79accd4531a1f20a4d16e10213e48ba7eb55000fa59074a4fe31d4fb8`  
		Last Modified: Mon, 08 Sep 2025 22:52:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:f3dbb0c12125fda2e678bb6e8c376992841ba1138f1103a1c30422801813a84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96ef1b79be01b1c63c29b78846c18b5a0cfba1c0539c180e46906dbe510cc0f`

```dockerfile
```

-	Layers:
	-	`sha256:013bd6ed603a8a9a894d817420ff1abc446eb10e3586662937791a6b464b9586`  
		Last Modified: Mon, 08 Sep 2025 23:28:25 GMT  
		Size: 2.3 MB (2283480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f96015f264b3386498c253b2b0f6bd011b1bbc30d826bbea742df498d1803687`  
		Last Modified: Mon, 08 Sep 2025 23:28:26 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:cb88f99f892373ab4cf6ee16b64d26e2c9d9910d3cac26cbb72e78a8d758d53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72980218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005000d57a5c6400df86411b9981bef299deb1e8c973a350b11e8f3ac603a193`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2093fb76882879fc5517d526ca316eb05618850f5fd3daa8c950946e34fc24ce`  
		Last Modified: Wed, 13 Aug 2025 09:16:42 GMT  
		Size: 1.3 MB (1260194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8a596a6f7ae1c31f06473eb7f1d587ea75a7424b3dbecc7c0780422937852`  
		Last Modified: Wed, 13 Aug 2025 09:16:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5d0031eb3976169f0d81c7527effd0ffe4812bad7bcd0acfe66d6fa82fc0c0`  
		Last Modified: Wed, 13 Aug 2025 09:23:53 GMT  
		Size: 37.9 MB (37867541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff3dc5bb4af78e0ef402f8972ff060a4a925a1a4ace3e22550f797f1f31698`  
		Last Modified: Wed, 13 Aug 2025 09:23:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907ebaa06cd1295cb1a66ebbf912eafee334ce577246b80d4017e6d35a4dca7a`  
		Last Modified: Wed, 13 Aug 2025 22:17:48 GMT  
		Size: 5.9 MB (5908385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b853527fdeacadd65b23e9d37bfc5713a7241c43813edd3988441261522e5075`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab8f68f1e9e40bdda500351aa9e7a2b38d5906551ac8f5544a857f6d1b1e77`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032c6bd746e50e7b7c082621f667db99baac05330d4f52051ce6ba246a3e6b99`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:d931b5b333a78735cd3ada972ab68a630d64c5c8169a9f2c1a8da6ef586fa6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73249d122bcc9643379894b1b6531966a9e4380226da3eb3ed639c7fdcc9b99b`

```dockerfile
```

-	Layers:
	-	`sha256:48518b2d36214bf578297f00300b46e74f671be91457f130eb4d9336b069a5ff`  
		Last Modified: Wed, 13 Aug 2025 23:28:22 GMT  
		Size: 2.3 MB (2285603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5061202e874c8a9137a61cdd64e1e5408ecfc3f02e16298cc0de054b2c3df615`  
		Last Modified: Wed, 13 Aug 2025 23:28:23 GMT  
		Size: 21.2 KB (21242 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:3bfbaf7f1ffb22a981b5e7dda8dad06a5620b64435fc9bef7797edc507dcc415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90da0d29ff1d896601979f7f5ab2e7d42a6d2cb7fdcef82756b7e5879e67da8e`
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
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:7b61b1398597ae15881ff464a9579b0e6a36c2c892c8b1b57f2f7cdeabb0232d`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 1.2 MB (1234683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab266ffb9d0322ee0c80bf4525c58d869463342abc3ef4de1f8c403a60a01192`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bc1cec816e3a53f6dc51ab6695d3ec9c3cbe0f0b48985630ed8e62192ac43`  
		Last Modified: Tue, 09 Sep 2025 03:41:17 GMT  
		Size: 37.7 MB (37730394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef9a0402a43858b4b35159ce01cf7a59853a8d814ea1c28004db99d3dd6f97f`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e668e135a42ee05d0ba0a59770170ba0de2d3eed0baa19b30af660026f4faf`  
		Last Modified: Tue, 09 Sep 2025 04:49:50 GMT  
		Size: 5.7 MB (5690183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7025af5322f18d0d01eea3476f555dc9dadc025ead3897a85242c3b0790c62`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ac61abdc71f1b8471416535baa300fcd27dd8ecbb006effdfcb5eca3f30465`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afc6502698d3bb76e6826a752d1a062258466a3ecc5037be44badebf7ffe904`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:7141e369be10e7bdb7afca005e04f946b5b959d89b18f7da9e821aa52680eb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f72fc69dee6e025f1648a227bee99e377e7130fda9903824da531b6a5a512b`

```dockerfile
```

-	Layers:
	-	`sha256:8c36cfc11c8d0dfdf9b0e3522acf836a63225d6a6f638aaa3bc3102e391715be`  
		Last Modified: Tue, 09 Sep 2025 05:28:28 GMT  
		Size: 2.3 MB (2284892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a03a28068de559d2492658e68ed9e8a332d9c9f4f2f87c934795966e07b2c68`  
		Last Modified: Tue, 09 Sep 2025 05:28:29 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:60809130e540ba282fb497261ed202b534042d4c364e70ee99bedbf7b5049fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79478043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463289d853352175b0f583d4b62188d2bcbc5434b79dc5a9a472537a4d67800e`
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
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:1f3ed651bcf45dc8d6b2aa861f7982b10809d084dc996d19960a8fd6ae67679c`  
		Last Modified: Tue, 09 Sep 2025 01:03:25 GMT  
		Size: 1.3 MB (1259738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6f2d7d9697c7d27005eb8d0653bb31356a96aaf11157cd07fdc7122b9debd`  
		Last Modified: Tue, 09 Sep 2025 01:03:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca38028ecf75c470e6dcab31844c5e688b32b3588001bae7afcd1e568b8847`  
		Last Modified: Tue, 09 Sep 2025 01:48:01 GMT  
		Size: 42.1 MB (42063063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d674198437b5e8cab0a16102accad13d25d563c2a6d29e1dfdf8714bd57fe`  
		Last Modified: Tue, 09 Sep 2025 01:03:24 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea86b09599e70bddc9be118d14b4b2c0392947af222767c6ce9025749d7ec952`  
		Last Modified: Tue, 09 Sep 2025 02:29:43 GMT  
		Size: 6.0 MB (6016216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b99c977d6728cf8c1c24f2c6e9686030f04e43d8979f7194223785cb0b9209`  
		Last Modified: Tue, 09 Sep 2025 02:29:52 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac072aacd0d9972a7edd976c0cf04a4edf46e02b7e7d6b9e60e7a968e598286`  
		Last Modified: Tue, 09 Sep 2025 02:29:45 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f828884181523011879e6e9679c26555cc3034c75cfa41311604d7956b9d0a`  
		Last Modified: Tue, 09 Sep 2025 02:29:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:9955b78921ef3210c523d857c795d628516bb00d630cbb8fbc9d34ff8becf3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec60ef8580b127ce74a8e6435db5a947341415b6be7cfee48dffde653c288b7`

```dockerfile
```

-	Layers:
	-	`sha256:a089b320e9bca83e08249bb4eae5e08b32f17dd6097860eab11282783c8a4f40`  
		Last Modified: Tue, 09 Sep 2025 05:28:33 GMT  
		Size: 2.3 MB (2283752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b1300c153bb28f7264cb101bb67f3eb4f78c7f1e032601890e6d80c56981f84`  
		Last Modified: Tue, 09 Sep 2025 05:28:34 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; 386

```console
$ docker pull fluentd@sha256:00c0ba7d40714f8a264e5c5e2fe9864ed612c6b64b313da61f7f615b62741ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76237114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0096cd93dfb8cff0d95f3b241fcd0b819f5d92490964f62433dd194484ef96b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfb18ad48f85fd4ca43130c11b60c8dd156cb1815fd08233be2be9c36c6923`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 1.3 MB (1285592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ae728bed6a475a8811b8b0a9460889cb5e0b9c9882d24089f9b3f37ea0ec1`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f33d4089ac39c16a1eb1172c1fd597771702897fc5472ebd4524ee51d009b1`  
		Last Modified: Mon, 08 Sep 2025 22:02:16 GMT  
		Size: 37.7 MB (37657047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1143329072f08996cee8c8782335612b6460d9af2d9c7b80994a10330d6565`  
		Last Modified: Mon, 08 Sep 2025 21:42:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c9149010179ce2a7385b9f1d4bba0926ec1a8f760320ce1a18344605fdefb`  
		Last Modified: Mon, 08 Sep 2025 22:56:47 GMT  
		Size: 6.0 MB (6002305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ae9af9420adf087b905e7979604a6aa9bbc3a4ec10861d9343cf60105fd1f6`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec1b97fb2027b8b637569ad830d697f5bfbc90b8073821f7667ab74bf5a7ee9`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e572568dc6a854cf5d202e39d57adff848138401e921cd90b5517c03a03b56`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:c520f8feb045dc07ca91f1b801a18b3da2b99164328f5cea9e3d4617671fd805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a43abcc28180d678dd6fb3f2c34449f867fddd6ced15eca284444f3bed3254e`

```dockerfile
```

-	Layers:
	-	`sha256:4fd46796ac747472faab066b28d336aeb770dcd930f6a4574e047894e2f9c4e1`  
		Last Modified: Mon, 08 Sep 2025 23:28:40 GMT  
		Size: 2.3 MB (2280668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e027c0378727a4242ff878c5bf5d33ab554280d64bc99f99f42aa0b4ec277e`  
		Last Modified: Mon, 08 Sep 2025 23:28:41 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; ppc64le

```console
$ docker pull fluentd@sha256:578c42ba1e6fe6d220e34f814a6907ef7f0a68570a200cff2dad7b5be01a0063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80931845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554f74aaca5d4fb974f997565fce7312dc080508c46bcd65b969ad234174347d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ce8600c6aabffbd80bd501b7ac3a736f18377ed3e07f94e2ee78a82b4e4f36`  
		Last Modified: Wed, 13 Aug 2025 17:10:49 GMT  
		Size: 1.3 MB (1307302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beeaeb3c6936a2d2eb3b798f796525e15863a84f94eeac482b026abcf5e81681`  
		Last Modified: Wed, 13 Aug 2025 17:10:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff53e1f7034343e8070d6221a1160a532a7e0c29de8bbc1705dc7c38bedbb24`  
		Last Modified: Wed, 13 Aug 2025 17:20:51 GMT  
		Size: 39.5 MB (39501405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4abad74118dcd88bae1a1fab5137324bd11deded7bf240335b90943dcef30c`  
		Last Modified: Wed, 13 Aug 2025 17:20:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230e7efe3550ceb6d1b0edea559996448ddf4f137a78f786e726123946b0815c`  
		Last Modified: Thu, 14 Aug 2025 02:02:36 GMT  
		Size: 6.5 MB (6526530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d625b46b5e4f28fc6df5b2baa1399a290f56672bcc7d4558a66b3038c2232a33`  
		Last Modified: Thu, 14 Aug 2025 02:02:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711cdf0979bb42ee138c5cc2104ae40a16fc27e69d5ce3c47c4567168e8d15bc`  
		Last Modified: Thu, 14 Aug 2025 02:02:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af84d819228b1a405da1d867e01bf2775cafda73e14fd745cfa4323c8a4a1f1`  
		Last Modified: Thu, 14 Aug 2025 02:02:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:b73585cc3502a53d8faf8e455384d82b34e9c09bb912756fef13757893f63e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aee2b306d1c9a5e7cd4cdcfd9e5171841a4efb08f14de805ddf09716943abb9`

```dockerfile
```

-	Layers:
	-	`sha256:2f6801a230c74e4b9aed5d3e1951eea3fefc7f11bb2333e136ede64cbf5eadd2`  
		Last Modified: Thu, 14 Aug 2025 02:28:32 GMT  
		Size: 2.3 MB (2286167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c3a3456832f73a97de5511ae14d2bb183385c903d0eb55970dec799fd33b44`  
		Last Modified: Thu, 14 Aug 2025 02:28:33 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:latest` - linux; s390x

```console
$ docker pull fluentd@sha256:282b140069685c91b06cc70bd403db8dfc2175bf2114ccee46fef0f863576d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76691999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa2256db132f298feed82e53e31f7ba4e9a4ec15e6e001a81501b09c007b01b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56be941f806d82f4bf75185b333c5c589812220338507cb5d56baeeee8c5965`  
		Last Modified: Wed, 13 Aug 2025 06:50:22 GMT  
		Size: 1.3 MB (1292014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88df88585689c870b8cb13eccddc94febb777e8fb5f684a7ea31e4b5317929`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbba3b8727d5a05350927ba0dae09b37c2f43cf7ae85bf1a5ce90e04f03ab75`  
		Last Modified: Wed, 13 Aug 2025 05:54:45 GMT  
		Size: 39.2 MB (39180168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23cfe07c682626dbf88b68cf0822a38658eb00013c59f00bd48113d5788ecc`  
		Last Modified: Wed, 13 Aug 2025 05:54:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715644edf14c65a22fc17afc877e73e2481104398c62fc9f6612b110e99b19a2`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 6.4 MB (6384364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972751519e154187ceeadef8b4540fe82a0db5f10c3dfe19b879c762d3676ba9`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241a9530941b60d0de548b1cc1e87c8a4e1ad75c07e7f22d21aa4adcce58f039`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257fbad7ece230f4d601fe80c948945f942f732c27de9e5b66474557be69d0a`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:latest` - unknown; unknown

```console
$ docker pull fluentd@sha256:0e3124818a6163f62aa958c1bcdd89be51c6dceda624ad1ef20863b89ad31c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd5961f5539cf8ac1e04fa9048683b8d10d088bd24da21691b4d97caf254a36`

```dockerfile
```

-	Layers:
	-	`sha256:c7822c267d4e80f00ed3c7f2cdee4230a544030e32a353eef79105538eb19362`  
		Last Modified: Wed, 13 Aug 2025 11:28:35 GMT  
		Size: 2.3 MB (2284077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929c64c079132a48ce0d1077d129e2a262a05d1d5c89af9da4583077965fd2bc`  
		Last Modified: Wed, 13 Aug 2025 11:28:36 GMT  
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
$ docker pull fluentd@sha256:b78ff7745442f9ee333f3ae03b8ebcd020097176bc740955130a10d9c64d1cae
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
$ docker pull fluentd@sha256:2c0120a67b566043e46528ce60918fd53de2b21c8ed3dd5130a82aa4358fe601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81970565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f49483ecdda2a58cbb4a3f1a985d3414a4e35cdaf2eb15d1bd977a0106be12`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050c164b0e794afb46b646f882dba91fbed0930f2cb4fec546fa962ec38bcb51`  
		Last Modified: Mon, 08 Sep 2025 22:08:18 GMT  
		Size: 3.5 MB (3509711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b362a17c84b23e1c55f542c07580ffab9e0335a0681f17200dfe1589489d675`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5afa81e629f95c7942414938c5b78f2a61dbbe742eb7511fb1e1e47f9650d9`  
		Last Modified: Mon, 08 Sep 2025 22:09:02 GMT  
		Size: 36.0 MB (35963925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3dd000014f3ed9a7d255ba41df76318b6272495305e10504b182c902e66134`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658519265de037dac6ec062da9837fccd6143c3d8a23214255f7a96a59fcf6be`  
		Last Modified: Mon, 08 Sep 2025 23:16:56 GMT  
		Size: 14.3 MB (14266191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d35bb75e5ca21f9963d20b5c841ba29adf51662967e62ede6887ca65c79e9e2`  
		Last Modified: Mon, 08 Sep 2025 23:02:35 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3270f9ce8bbadd63a58efdc5d94831c2742323128bddfc2e9b9d7f7fdf6050f`  
		Last Modified: Mon, 08 Sep 2025 23:02:34 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3034afc29fe0e5b783a0183ce22b15270c7663feaec61b41a5a0838c37bb101`  
		Last Modified: Mon, 08 Sep 2025 23:02:34 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:47a3857e23350849c9a5cc370ff3b1306ae234dcbaaf8def4db1a174aebea443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430433e517ca60807ed63ff57ddd457d2e28661c700c0c44e9128531ee4f9d1e`

```dockerfile
```

-	Layers:
	-	`sha256:f60fdb30c29eb246e7036c0e36c67af2113e3895c7f7d198b16170acc4a33c9d`  
		Last Modified: Mon, 08 Sep 2025 23:28:37 GMT  
		Size: 2.7 MB (2668422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a77b544099b8919a4a18ad9ddf798f65c18d0cf1915663476b1815e857f873c0`  
		Last Modified: Mon, 08 Sep 2025 23:28:38 GMT  
		Size: 21.1 KB (21103 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:dd3fff06488f2862733c1e5183bac1655e75b16219533b943355d72b25ee5c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75410462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155e6f45e50a306b18c0166900e03b7f31c6ddd37d85ac81ff20aa3d0cfb6064`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
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
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcf5cc69aa8699ad571a9f58c06dc6316dfac082af57e4d09e6fb9aa9c637aa`  
		Last Modified: Tue, 12 Aug 2025 21:13:59 GMT  
		Size: 3.1 MB (3079825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fbc2364feff15170dc3218d0d933a3f9571e48b9a782d4e3a2b7470892f5d`  
		Last Modified: Wed, 13 Aug 2025 09:24:33 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7904098e3a5a9bb8fda0f1ed40117c73ce09dcbe9ddd78d461942225072ddb5`  
		Last Modified: Wed, 13 Aug 2025 22:41:05 GMT  
		Size: 32.3 MB (32326823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b39ce4507dba6e0263946412628a65baf20a0d170280a496bc065eaecc31f4e`  
		Last Modified: Wed, 13 Aug 2025 10:34:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4d9de4ddf2fb18f5788d1439c958676a27f30a5783384a5957fcb217864f86`  
		Last Modified: Wed, 13 Aug 2025 22:13:31 GMT  
		Size: 14.2 MB (14238700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d5548c8c85f51cc8c8e18b41f5b2e9913e492d73112c5e9b83367e12f7e4dd`  
		Last Modified: Wed, 13 Aug 2025 22:13:30 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ab250c9f41d38b5037d8396b72996277fcfae15dfdbbdf016796344c03d41e`  
		Last Modified: Wed, 13 Aug 2025 22:13:31 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c442bf0cd90ea40c33b226b920f25dfb81634b9a4d589768c227c50a58ec20c`  
		Last Modified: Wed, 13 Aug 2025 22:13:27 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:60cd352307aa74e2d739a0320423a1da6c8e26f146a8b6d78dce794281e98cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb862c52672faf9b5882af3ee931f680f4bea3449ed52089ebeb2ce952322d2`

```dockerfile
```

-	Layers:
	-	`sha256:d1a4876f5e1dbfa1c230e3107dcdfd75d4d51755bb2546c3f7f2600010432ad5`  
		Last Modified: Wed, 13 Aug 2025 23:28:31 GMT  
		Size: 2.7 MB (2670102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94af0f5c0b3697f8b53856e482e2991c24c99cfd21706fbedb59681d2a972cbf`  
		Last Modified: Wed, 13 Aug 2025 23:28:32 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:3c1bcf7b80c55c61c6be87a7fbde01ac7621dc3928314d02b4719723941fe5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73183001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a47d152c30976fa30c37da9e49093906a5f41605e57d477e86eaf0c243abd5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48bba6e989724d7ee613a13eba6e547923aad96f6bd9d666b23dcbbec0a0707`  
		Last Modified: Tue, 12 Aug 2025 21:13:53 GMT  
		Size: 2.9 MB (2912732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1d31d56ea7a161bf12a2238d311387788fdcf3f7fb00eb2d068699e6ee983e`  
		Last Modified: Wed, 13 Aug 2025 11:14:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0583ced8a44c08a5597f633fda828c658ff275c11da7b6606f91ee39f3539bc`  
		Last Modified: Wed, 13 Aug 2025 17:32:11 GMT  
		Size: 32.2 MB (32161821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da5fcfc349c61567d9c48a257f58eb95b7fefdc640802493d144ef86d5712e7`  
		Last Modified: Wed, 13 Aug 2025 11:15:01 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbf0d932512d7686e34e4c557b25ff33c7b58c798b58672bb037001c74a095e`  
		Last Modified: Wed, 13 Aug 2025 15:49:34 GMT  
		Size: 14.2 MB (14167123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f00998e2fd254a1d839a8347eaa76694f145afa466ba4db03e305afd50d43`  
		Last Modified: Wed, 13 Aug 2025 15:49:33 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181f839838750bf326092bf50532ce04496ce2a35f0a17b74a6cd5a209a23956`  
		Last Modified: Wed, 13 Aug 2025 15:49:33 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a709bbad028db52654afc6f3078177749b0e906571c7a3cdd74237674bb44099`  
		Last Modified: Wed, 13 Aug 2025 15:49:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b55521f1ac702d9502b564ceb770a11c9f2195f9ec9a9e9e4f3f9cfae0ada8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e4fe059966d8bbbc75202a07e91f896311507dbd85a966f33440c3bec5cbae`

```dockerfile
```

-	Layers:
	-	`sha256:8b09c4df09c468940eea1f22102c1a7e28a423e0753ebd1b1218987f134849ca`  
		Last Modified: Wed, 13 Aug 2025 17:28:34 GMT  
		Size: 2.7 MB (2668533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a667b6ebb37c5040d8c6c8ca680dfc05c48e3f1bd5812766ecb31a47f01a66a`  
		Last Modified: Wed, 13 Aug 2025 17:28:35 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a8623fd562344ba13ea2f10433f9bb7959b289bb0948e0a9bb2e8cd669fc15b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81617687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4287775213275823b3a6116158b83b9e530c9408bc7a30dac2c8c614491fed0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db621cf0180e66e8366f7c314573fb7deafa5c16b7222322e3988e1559e59f5f`  
		Last Modified: Tue, 09 Sep 2025 01:04:32 GMT  
		Size: 3.3 MB (3340617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6446e88d9e7957665d5a836ef3203901d1a2e3183dd2e95da526e1e6404f4bdd`  
		Last Modified: Tue, 09 Sep 2025 01:04:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458db9624c10a2feaf033d0d6f2453e13e1e47edef5911df81569b3c9850e032`  
		Last Modified: Tue, 09 Sep 2025 01:48:25 GMT  
		Size: 35.9 MB (35900702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6e86a95d226b9688f9b21a9275a78b21f970eb4a226d239d0488f81e48b8b1`  
		Last Modified: Tue, 09 Sep 2025 01:13:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b3eba46027a9aae30bbe0043be3d62c933413aaf6e0ce39eedd40ee789d80`  
		Last Modified: Tue, 09 Sep 2025 05:32:18 GMT  
		Size: 14.3 MB (14271880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90de710b4704eb867568ecf4883a81d955e6a51895194f9e4f72725246c6d08a`  
		Last Modified: Tue, 09 Sep 2025 02:28:13 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d21da04eb31f140c3a532d7aae568e820512b0f894e7aaa0ca57b0699c4c30`  
		Last Modified: Tue, 09 Sep 2025 02:28:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278c01e3b79fe20d3db4e3d6780636b3b9149720d50b0d216946a4689a6ba686`  
		Last Modified: Tue, 09 Sep 2025 02:28:13 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:17718128f718ea859caeeafbcec67499563d34067d3cf53f80ef1bdcbcf22f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44701e02288cba88e2edc02fc56971f968d7582777c1c1c67bee93caf4bb4dd9`

```dockerfile
```

-	Layers:
	-	`sha256:e432a9ae469e0b290086b23540c2da70e9365a166e89df54b8c467ce36f848df`  
		Last Modified: Tue, 09 Sep 2025 05:28:38 GMT  
		Size: 2.7 MB (2668662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:005d6729e4fd8921f9ed07478bba6d7475394e9b57951569744ed39b0ab4e5fe`  
		Last Modified: Tue, 09 Sep 2025 05:28:39 GMT  
		Size: 21.2 KB (21199 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:636e89802d74d2ae051ffc9e419dea78658286d870f532d6f2bb71515f01768d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78941267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a227ff7d42a50e7cd70cbc1744996dfe2901b65cc89ae6a56c95eea03600d25`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
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
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a484e87da105d0df20f5f37be4716fe4b158f66efdab63a221b4aad2b79d5e6`  
		Last Modified: Mon, 08 Sep 2025 22:02:00 GMT  
		Size: 3.5 MB (3511019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472089a4907fde2f37f8e7305ca87fc210bf33e7947c084d24b9f0ee595cf77b`  
		Last Modified: Mon, 08 Sep 2025 22:02:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9a7fafca6eba7e0b66175169d26872af3cd56b8b7d91040e3fb96b7d5a86db`  
		Last Modified: Mon, 08 Sep 2025 22:02:02 GMT  
		Size: 32.2 MB (32159724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8f8c0aca65d2393c207eb4de989231df4509bb105b8ca6e241739f11ced24c`  
		Last Modified: Mon, 08 Sep 2025 22:01:59 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469c3b3317e36461c2c2fbf16df21a9a30abcab4237080341e5927f5e962ca3`  
		Last Modified: Mon, 08 Sep 2025 22:04:57 GMT  
		Size: 14.1 MB (14058500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fd228721e05a1165768466bc704bb80a41d8663f6ca4306022440e634c7513`  
		Last Modified: Mon, 08 Sep 2025 22:59:08 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4368933d4114e5aa675f760f9b5c1643559ae56e2004ba35142de58ef9344ec3`  
		Last Modified: Mon, 08 Sep 2025 22:59:08 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23a7ca2ecd5c53fdc15d2daf5b59a12157643396a99bfd5d6378f9bb09a47a`  
		Last Modified: Mon, 08 Sep 2025 22:59:08 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:bbd2626ae5f4a12d257c049930f340adf0d94aa4ffa03f26b3f6d6ba3cf3c351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c285dd2831814bc749a4b91a42156eaafbae13de3f77433a04c6e9f3973001f`

```dockerfile
```

-	Layers:
	-	`sha256:cb787295072735e8e08b155184a4f143f4cc935bdf9dc42c8c4da5419604cde4`  
		Last Modified: Mon, 08 Sep 2025 23:28:53 GMT  
		Size: 2.7 MB (2665601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101555379799d83e2a4f12f310ca2a5d8025a3f81db57c59fa2a71ef59e2add6`  
		Last Modified: Mon, 08 Sep 2025 23:28:54 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:a2bc95b820b6f71df0f1a53f12440447902fbd3932a988ba3e97c15f5884b65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84277159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb389446d613f9faf64a89872a84e48f307846b2c0216181b2e9c192adeb830f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124a31acf9aaa7ef018c74e002166fc0bd461213e9182b7c9c4f12bc88e8c390`  
		Last Modified: Wed, 13 Aug 2025 17:15:53 GMT  
		Size: 3.7 MB (3709127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76641f014eec08baf6211599050e0e08aecdea1b4d3e2b864d2b85131b93c0d8`  
		Last Modified: Wed, 13 Aug 2025 17:15:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467456b434a4ff600a376a0381ade68c5d0ef61872bf058b8ea62a8fe5dfd8b1`  
		Last Modified: Wed, 13 Aug 2025 17:43:47 GMT  
		Size: 33.8 MB (33832731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288ee755229c684126614ff8e088f665347de8f1317f959c24ffbeed957de18c`  
		Last Modified: Wed, 13 Aug 2025 17:43:33 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586b1f43b63927854b63c4d66627a21330f0b385ac60a1e9e86b38ef88538c09`  
		Last Modified: Thu, 14 Aug 2025 01:56:44 GMT  
		Size: 14.7 MB (14659483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c09154d503660468031ced1a24486482f5df57ff06e4dd383f9ef8bbe2d18ae`  
		Last Modified: Thu, 14 Aug 2025 01:56:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800fb0cc695c299fec99701a919b9f4b923eae03b582976a93d3c91cc2f0ef3`  
		Last Modified: Thu, 14 Aug 2025 01:56:34 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14f7d695e39531f3ed7962e1e414a9584617d1ede842ac1a1620f00de97b905`  
		Last Modified: Thu, 14 Aug 2025 01:56:39 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:55344347013ada3dca2aaaab146d55d719766871da5fb8dd5d60ff4215900080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cf59d636dfd21eba85e8c72ff273cce357366a747d0f40b91ad9815960d1c1`

```dockerfile
```

-	Layers:
	-	`sha256:21af1606f6583c79a420ab401bbc34417e13d5f13c5eced276acbba8e96bd63f`  
		Last Modified: Thu, 14 Aug 2025 02:28:41 GMT  
		Size: 2.7 MB (2670724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:078f63dfa48906fd5fad3620cbba6088c1830234f6eae55887e70dac21eda8c0`  
		Last Modified: Thu, 14 Aug 2025 02:28:42 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:31b134dad32567770daf4e6dcb42c690fe2790c7e4c90f37269863845c787638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77556865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3c409fb99010f239e71d18f9da1d32f8149dffddb0df569831d7d2e61b5fc2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6e199e9098e65eb0b39c9931e15a8e537b5d5f6ad8f1a4d66db58f10a04d33`  
		Last Modified: Wed, 13 Aug 2025 18:06:31 GMT  
		Size: 3.2 MB (3170221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa49c76a78ba506c8cdea5ae1a7e04aebfb9fa3a9ffc0a6897995b663c0845d8`  
		Last Modified: Wed, 13 Aug 2025 18:06:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9961e65412c8a19bbe1e5fac7f30b5b3d44ebed11695ccae3c61880274afd5`  
		Last Modified: Wed, 13 Aug 2025 19:16:03 GMT  
		Size: 33.1 MB (33098669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fb2e2aabb7171a7993f81018bbf4ce9da7c593ed3ac239ad341f5174eca0c`  
		Last Modified: Wed, 13 Aug 2025 18:44:58 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1891eb1d263a2a28ec77346510c5868ef86256e0d7db4fcde9ab60719aabadc6`  
		Last Modified: Thu, 14 Aug 2025 02:17:54 GMT  
		Size: 14.4 MB (14397742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede9c681783be536d136ffd1b345802b5154063cd02c73d48721d0e1dc28585d`  
		Last Modified: Thu, 14 Aug 2025 02:17:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c194e19cc1c22c58d05306a042f62dd158bfd67b61584f2e67ae8f84229a442`  
		Last Modified: Thu, 14 Aug 2025 02:17:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6044407b3b6eb303c8d9109fd26cca94b2f2412410f5e7923aab167ef153b39f`  
		Last Modified: Thu, 14 Aug 2025 02:32:30 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c7d0a3ff5bfb22f915192010307be5cde2ba313a3ff8827089ffd3c279eee702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2684236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528401d86e86fe1f71f6e5379cba7ab7b39de231ec8754c7002c6160f72e5244`

```dockerfile
```

-	Layers:
	-	`sha256:5d3c62f2a29023e1deb98c493b8080cdd8530f3de233073cd469b397bd3efec1`  
		Last Modified: Thu, 14 Aug 2025 05:28:35 GMT  
		Size: 2.7 MB (2663132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ad10b10e959a6b57b09a66ddc9cc2e7560bbd84ee1638de78ed3c8ded62adfe`  
		Last Modified: Thu, 14 Aug 2025 05:28:36 GMT  
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
$ docker pull fluentd@sha256:b78ff7745442f9ee333f3ae03b8ebcd020097176bc740955130a10d9c64d1cae
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
$ docker pull fluentd@sha256:2c0120a67b566043e46528ce60918fd53de2b21c8ed3dd5130a82aa4358fe601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (81970565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f49483ecdda2a58cbb4a3f1a985d3414a4e35cdaf2eb15d1bd977a0106be12`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050c164b0e794afb46b646f882dba91fbed0930f2cb4fec546fa962ec38bcb51`  
		Last Modified: Mon, 08 Sep 2025 22:08:18 GMT  
		Size: 3.5 MB (3509711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b362a17c84b23e1c55f542c07580ffab9e0335a0681f17200dfe1589489d675`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5afa81e629f95c7942414938c5b78f2a61dbbe742eb7511fb1e1e47f9650d9`  
		Last Modified: Mon, 08 Sep 2025 22:09:02 GMT  
		Size: 36.0 MB (35963925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3dd000014f3ed9a7d255ba41df76318b6272495305e10504b182c902e66134`  
		Last Modified: Mon, 08 Sep 2025 22:08:17 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658519265de037dac6ec062da9837fccd6143c3d8a23214255f7a96a59fcf6be`  
		Last Modified: Mon, 08 Sep 2025 23:16:56 GMT  
		Size: 14.3 MB (14266191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d35bb75e5ca21f9963d20b5c841ba29adf51662967e62ede6887ca65c79e9e2`  
		Last Modified: Mon, 08 Sep 2025 23:02:35 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3270f9ce8bbadd63a58efdc5d94831c2742323128bddfc2e9b9d7f7fdf6050f`  
		Last Modified: Mon, 08 Sep 2025 23:02:34 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3034afc29fe0e5b783a0183ce22b15270c7663feaec61b41a5a0838c37bb101`  
		Last Modified: Mon, 08 Sep 2025 23:02:34 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:47a3857e23350849c9a5cc370ff3b1306ae234dcbaaf8def4db1a174aebea443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430433e517ca60807ed63ff57ddd457d2e28661c700c0c44e9128531ee4f9d1e`

```dockerfile
```

-	Layers:
	-	`sha256:f60fdb30c29eb246e7036c0e36c67af2113e3895c7f7d198b16170acc4a33c9d`  
		Last Modified: Mon, 08 Sep 2025 23:28:37 GMT  
		Size: 2.7 MB (2668422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a77b544099b8919a4a18ad9ddf798f65c18d0cf1915663476b1815e857f873c0`  
		Last Modified: Mon, 08 Sep 2025 23:28:38 GMT  
		Size: 21.1 KB (21103 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:dd3fff06488f2862733c1e5183bac1655e75b16219533b943355d72b25ee5c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75410462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155e6f45e50a306b18c0166900e03b7f31c6ddd37d85ac81ff20aa3d0cfb6064`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
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
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcf5cc69aa8699ad571a9f58c06dc6316dfac082af57e4d09e6fb9aa9c637aa`  
		Last Modified: Tue, 12 Aug 2025 21:13:59 GMT  
		Size: 3.1 MB (3079825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00fbc2364feff15170dc3218d0d933a3f9571e48b9a782d4e3a2b7470892f5d`  
		Last Modified: Wed, 13 Aug 2025 09:24:33 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7904098e3a5a9bb8fda0f1ed40117c73ce09dcbe9ddd78d461942225072ddb5`  
		Last Modified: Wed, 13 Aug 2025 22:41:05 GMT  
		Size: 32.3 MB (32326823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b39ce4507dba6e0263946412628a65baf20a0d170280a496bc065eaecc31f4e`  
		Last Modified: Wed, 13 Aug 2025 10:34:26 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4d9de4ddf2fb18f5788d1439c958676a27f30a5783384a5957fcb217864f86`  
		Last Modified: Wed, 13 Aug 2025 22:13:31 GMT  
		Size: 14.2 MB (14238700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d5548c8c85f51cc8c8e18b41f5b2e9913e492d73112c5e9b83367e12f7e4dd`  
		Last Modified: Wed, 13 Aug 2025 22:13:30 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ab250c9f41d38b5037d8396b72996277fcfae15dfdbbdf016796344c03d41e`  
		Last Modified: Wed, 13 Aug 2025 22:13:31 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c442bf0cd90ea40c33b226b920f25dfb81634b9a4d589768c227c50a58ec20c`  
		Last Modified: Wed, 13 Aug 2025 22:13:27 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:60cd352307aa74e2d739a0320423a1da6c8e26f146a8b6d78dce794281e98cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb862c52672faf9b5882af3ee931f680f4bea3449ed52089ebeb2ce952322d2`

```dockerfile
```

-	Layers:
	-	`sha256:d1a4876f5e1dbfa1c230e3107dcdfd75d4d51755bb2546c3f7f2600010432ad5`  
		Last Modified: Wed, 13 Aug 2025 23:28:31 GMT  
		Size: 2.7 MB (2670102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94af0f5c0b3697f8b53856e482e2991c24c99cfd21706fbedb59681d2a972cbf`  
		Last Modified: Wed, 13 Aug 2025 23:28:32 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:3c1bcf7b80c55c61c6be87a7fbde01ac7621dc3928314d02b4719723941fe5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73183001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a47d152c30976fa30c37da9e49093906a5f41605e57d477e86eaf0c243abd5`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48bba6e989724d7ee613a13eba6e547923aad96f6bd9d666b23dcbbec0a0707`  
		Last Modified: Tue, 12 Aug 2025 21:13:53 GMT  
		Size: 2.9 MB (2912732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1d31d56ea7a161bf12a2238d311387788fdcf3f7fb00eb2d068699e6ee983e`  
		Last Modified: Wed, 13 Aug 2025 11:14:51 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0583ced8a44c08a5597f633fda828c658ff275c11da7b6606f91ee39f3539bc`  
		Last Modified: Wed, 13 Aug 2025 17:32:11 GMT  
		Size: 32.2 MB (32161821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da5fcfc349c61567d9c48a257f58eb95b7fefdc640802493d144ef86d5712e7`  
		Last Modified: Wed, 13 Aug 2025 11:15:01 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbf0d932512d7686e34e4c557b25ff33c7b58c798b58672bb037001c74a095e`  
		Last Modified: Wed, 13 Aug 2025 15:49:34 GMT  
		Size: 14.2 MB (14167123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03f00998e2fd254a1d839a8347eaa76694f145afa466ba4db03e305afd50d43`  
		Last Modified: Wed, 13 Aug 2025 15:49:33 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181f839838750bf326092bf50532ce04496ce2a35f0a17b74a6cd5a209a23956`  
		Last Modified: Wed, 13 Aug 2025 15:49:33 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a709bbad028db52654afc6f3078177749b0e906571c7a3cdd74237674bb44099`  
		Last Modified: Wed, 13 Aug 2025 15:49:34 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b55521f1ac702d9502b564ceb770a11c9f2195f9ec9a9e9e4f3f9cfae0ada8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e4fe059966d8bbbc75202a07e91f896311507dbd85a966f33440c3bec5cbae`

```dockerfile
```

-	Layers:
	-	`sha256:8b09c4df09c468940eea1f22102c1a7e28a423e0753ebd1b1218987f134849ca`  
		Last Modified: Wed, 13 Aug 2025 17:28:34 GMT  
		Size: 2.7 MB (2668533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a667b6ebb37c5040d8c6c8ca680dfc05c48e3f1bd5812766ecb31a47f01a66a`  
		Last Modified: Wed, 13 Aug 2025 17:28:35 GMT  
		Size: 21.2 KB (21177 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:a8623fd562344ba13ea2f10433f9bb7959b289bb0948e0a9bb2e8cd669fc15b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81617687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4287775213275823b3a6116158b83b9e530c9408bc7a30dac2c8c614491fed0`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
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
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db621cf0180e66e8366f7c314573fb7deafa5c16b7222322e3988e1559e59f5f`  
		Last Modified: Tue, 09 Sep 2025 01:04:32 GMT  
		Size: 3.3 MB (3340617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6446e88d9e7957665d5a836ef3203901d1a2e3183dd2e95da526e1e6404f4bdd`  
		Last Modified: Tue, 09 Sep 2025 01:04:31 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458db9624c10a2feaf033d0d6f2453e13e1e47edef5911df81569b3c9850e032`  
		Last Modified: Tue, 09 Sep 2025 01:48:25 GMT  
		Size: 35.9 MB (35900702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6e86a95d226b9688f9b21a9275a78b21f970eb4a226d239d0488f81e48b8b1`  
		Last Modified: Tue, 09 Sep 2025 01:13:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b3eba46027a9aae30bbe0043be3d62c933413aaf6e0ce39eedd40ee789d80`  
		Last Modified: Tue, 09 Sep 2025 05:32:18 GMT  
		Size: 14.3 MB (14271880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90de710b4704eb867568ecf4883a81d955e6a51895194f9e4f72725246c6d08a`  
		Last Modified: Tue, 09 Sep 2025 02:28:13 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d21da04eb31f140c3a532d7aae568e820512b0f894e7aaa0ca57b0699c4c30`  
		Last Modified: Tue, 09 Sep 2025 02:28:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278c01e3b79fe20d3db4e3d6780636b3b9149720d50b0d216946a4689a6ba686`  
		Last Modified: Tue, 09 Sep 2025 02:28:13 GMT  
		Size: 476.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:17718128f718ea859caeeafbcec67499563d34067d3cf53f80ef1bdcbcf22f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44701e02288cba88e2edc02fc56971f968d7582777c1c1c67bee93caf4bb4dd9`

```dockerfile
```

-	Layers:
	-	`sha256:e432a9ae469e0b290086b23540c2da70e9365a166e89df54b8c467ce36f848df`  
		Last Modified: Tue, 09 Sep 2025 05:28:38 GMT  
		Size: 2.7 MB (2668662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:005d6729e4fd8921f9ed07478bba6d7475394e9b57951569744ed39b0ab4e5fe`  
		Last Modified: Tue, 09 Sep 2025 05:28:39 GMT  
		Size: 21.2 KB (21199 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:636e89802d74d2ae051ffc9e419dea78658286d870f532d6f2bb71515f01768d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78941267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a227ff7d42a50e7cd70cbc1744996dfe2901b65cc89ae6a56c95eea03600d25`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
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
	-	`sha256:dc2a09b0db8b98044474925cacc9c009aa76e5883edf644cc36c3f6a2e3917ac`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 29.2 MB (29209634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a484e87da105d0df20f5f37be4716fe4b158f66efdab63a221b4aad2b79d5e6`  
		Last Modified: Mon, 08 Sep 2025 22:02:00 GMT  
		Size: 3.5 MB (3511019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472089a4907fde2f37f8e7305ca87fc210bf33e7947c084d24b9f0ee595cf77b`  
		Last Modified: Mon, 08 Sep 2025 22:02:00 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9a7fafca6eba7e0b66175169d26872af3cd56b8b7d91040e3fb96b7d5a86db`  
		Last Modified: Mon, 08 Sep 2025 22:02:02 GMT  
		Size: 32.2 MB (32159724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f8f8c0aca65d2393c207eb4de989231df4509bb105b8ca6e241739f11ced24c`  
		Last Modified: Mon, 08 Sep 2025 22:01:59 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6469c3b3317e36461c2c2fbf16df21a9a30abcab4237080341e5927f5e962ca3`  
		Last Modified: Mon, 08 Sep 2025 22:04:57 GMT  
		Size: 14.1 MB (14058500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fd228721e05a1165768466bc704bb80a41d8663f6ca4306022440e634c7513`  
		Last Modified: Mon, 08 Sep 2025 22:59:08 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4368933d4114e5aa675f760f9b5c1643559ae56e2004ba35142de58ef9344ec3`  
		Last Modified: Mon, 08 Sep 2025 22:59:08 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23a7ca2ecd5c53fdc15d2daf5b59a12157643396a99bfd5d6378f9bb09a47a`  
		Last Modified: Mon, 08 Sep 2025 22:59:08 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:bbd2626ae5f4a12d257c049930f340adf0d94aa4ffa03f26b3f6d6ba3cf3c351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c285dd2831814bc749a4b91a42156eaafbae13de3f77433a04c6e9f3973001f`

```dockerfile
```

-	Layers:
	-	`sha256:cb787295072735e8e08b155184a4f143f4cc935bdf9dc42c8c4da5419604cde4`  
		Last Modified: Mon, 08 Sep 2025 23:28:53 GMT  
		Size: 2.7 MB (2665601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101555379799d83e2a4f12f310ca2a5d8025a3f81db57c59fa2a71ef59e2add6`  
		Last Modified: Mon, 08 Sep 2025 23:28:54 GMT  
		Size: 21.1 KB (21080 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:a2bc95b820b6f71df0f1a53f12440447902fbd3932a988ba3e97c15f5884b65c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84277159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb389446d613f9faf64a89872a84e48f307846b2c0216181b2e9c192adeb830f`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124a31acf9aaa7ef018c74e002166fc0bd461213e9182b7c9c4f12bc88e8c390`  
		Last Modified: Wed, 13 Aug 2025 17:15:53 GMT  
		Size: 3.7 MB (3709127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76641f014eec08baf6211599050e0e08aecdea1b4d3e2b864d2b85131b93c0d8`  
		Last Modified: Wed, 13 Aug 2025 17:15:53 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467456b434a4ff600a376a0381ade68c5d0ef61872bf058b8ea62a8fe5dfd8b1`  
		Last Modified: Wed, 13 Aug 2025 17:43:47 GMT  
		Size: 33.8 MB (33832731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288ee755229c684126614ff8e088f665347de8f1317f959c24ffbeed957de18c`  
		Last Modified: Wed, 13 Aug 2025 17:43:33 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586b1f43b63927854b63c4d66627a21330f0b385ac60a1e9e86b38ef88538c09`  
		Last Modified: Thu, 14 Aug 2025 01:56:44 GMT  
		Size: 14.7 MB (14659483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c09154d503660468031ced1a24486482f5df57ff06e4dd383f9ef8bbe2d18ae`  
		Last Modified: Thu, 14 Aug 2025 01:56:39 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800fb0cc695c299fec99701a919b9f4b923eae03b582976a93d3c91cc2f0ef3`  
		Last Modified: Thu, 14 Aug 2025 01:56:34 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14f7d695e39531f3ed7962e1e414a9584617d1ede842ac1a1620f00de97b905`  
		Last Modified: Thu, 14 Aug 2025 01:56:39 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:55344347013ada3dca2aaaab146d55d719766871da5fb8dd5d60ff4215900080
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cf59d636dfd21eba85e8c72ff273cce357366a747d0f40b91ad9815960d1c1`

```dockerfile
```

-	Layers:
	-	`sha256:21af1606f6583c79a420ab401bbc34417e13d5f13c5eced276acbba8e96bd63f`  
		Last Modified: Thu, 14 Aug 2025 02:28:41 GMT  
		Size: 2.7 MB (2670724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:078f63dfa48906fd5fad3620cbba6088c1830234f6eae55887e70dac21eda8c0`  
		Last Modified: Thu, 14 Aug 2025 02:28:42 GMT  
		Size: 21.1 KB (21138 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.16.9-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:31b134dad32567770daf4e6dcb42c690fe2790c7e4c90f37269863845c787638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77556865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf3c409fb99010f239e71d18f9da1d32f8149dffddb0df569831d7d2e61b5fc2`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Fri, 23 May 2025 01:51:58 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6e199e9098e65eb0b39c9931e15a8e537b5d5f6ad8f1a4d66db58f10a04d33`  
		Last Modified: Wed, 13 Aug 2025 18:06:31 GMT  
		Size: 3.2 MB (3170221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa49c76a78ba506c8cdea5ae1a7e04aebfb9fa3a9ffc0a6897995b663c0845d8`  
		Last Modified: Wed, 13 Aug 2025 18:06:41 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9961e65412c8a19bbe1e5fac7f30b5b3d44ebed11695ccae3c61880274afd5`  
		Last Modified: Wed, 13 Aug 2025 19:16:03 GMT  
		Size: 33.1 MB (33098669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fb2e2aabb7171a7993f81018bbf4ce9da7c593ed3ac239ad341f5174eca0c`  
		Last Modified: Wed, 13 Aug 2025 18:44:58 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1891eb1d263a2a28ec77346510c5868ef86256e0d7db4fcde9ab60719aabadc6`  
		Last Modified: Thu, 14 Aug 2025 02:17:54 GMT  
		Size: 14.4 MB (14397742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede9c681783be536d136ffd1b345802b5154063cd02c73d48721d0e1dc28585d`  
		Last Modified: Thu, 14 Aug 2025 02:17:54 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c194e19cc1c22c58d05306a042f62dd158bfd67b61584f2e67ae8f84229a442`  
		Last Modified: Thu, 14 Aug 2025 02:17:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6044407b3b6eb303c8d9109fd26cca94b2f2412410f5e7923aab167ef153b39f`  
		Last Modified: Thu, 14 Aug 2025 02:32:30 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.16.9-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c7d0a3ff5bfb22f915192010307be5cde2ba313a3ff8827089ffd3c279eee702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2684236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528401d86e86fe1f71f6e5379cba7ab7b39de231ec8754c7002c6160f72e5244`

```dockerfile
```

-	Layers:
	-	`sha256:5d3c62f2a29023e1deb98c493b8080cdd8530f3de233073cd469b397bd3efec1`  
		Last Modified: Thu, 14 Aug 2025 05:28:35 GMT  
		Size: 2.7 MB (2663132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ad10b10e959a6b57b09a66ddc9cc2e7560bbd84ee1638de78ed3c8ded62adfe`  
		Last Modified: Thu, 14 Aug 2025 05:28:36 GMT  
		Size: 21.1 KB (21104 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-1`

```console
$ docker pull fluentd@sha256:406eab0c90b337ea508a282d4917b61d046b740c7387c1dbb82c187e0b3d3716
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
$ docker pull fluentd@sha256:ba2a2644e30105d97209fa493cd9f9975f852353f7e4cffe9d67a2136fbea108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79117410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40476c6d4a4d9a86b707cf50405ed9380e4ec5b117499123be9cc96fb1c6165a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907bb64ed55e33da933ebd9b77bfa9382670074deb815d2e0d4f7d3067842ed1`  
		Last Modified: Mon, 08 Sep 2025 22:08:24 GMT  
		Size: 1.3 MB (1277837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676f670b77091f6f737a85b5792a0639bc680e827f931c13cb7e2fbfd0a38ebe`  
		Last Modified: Mon, 08 Sep 2025 22:08:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631f0e31bb9254d7f56d53693835aeb8d61c1c864ab85670b8997fb62d740e4f`  
		Last Modified: Mon, 08 Sep 2025 22:08:30 GMT  
		Size: 42.0 MB (42036169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836288d7f92195b5daec740a66ff4dbb4b6df0742d4a949a8892d634d98e848`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbaeb18472eaacfce9887b025572c879a5fdb37ef68212abe07046d303bd94f`  
		Last Modified: Mon, 08 Sep 2025 23:28:31 GMT  
		Size: 6.0 MB (6027518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7db22461d213e9de126e16bfc9c9ba9314204a0e3d6112828ac67310a6c22c`  
		Last Modified: Mon, 08 Sep 2025 22:52:04 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15320385f8b32e2c3cac705007a3fca3bf191963c690b6f79b18d84be24ea1f7`  
		Last Modified: Mon, 08 Sep 2025 22:52:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347687b79accd4531a1f20a4d16e10213e48ba7eb55000fa59074a4fe31d4fb8`  
		Last Modified: Mon, 08 Sep 2025 22:52:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f3dbb0c12125fda2e678bb6e8c376992841ba1138f1103a1c30422801813a84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96ef1b79be01b1c63c29b78846c18b5a0cfba1c0539c180e46906dbe510cc0f`

```dockerfile
```

-	Layers:
	-	`sha256:013bd6ed603a8a9a894d817420ff1abc446eb10e3586662937791a6b464b9586`  
		Last Modified: Mon, 08 Sep 2025 23:28:25 GMT  
		Size: 2.3 MB (2283480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f96015f264b3386498c253b2b0f6bd011b1bbc30d826bbea742df498d1803687`  
		Last Modified: Mon, 08 Sep 2025 23:28:26 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:cb88f99f892373ab4cf6ee16b64d26e2c9d9910d3cac26cbb72e78a8d758d53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72980218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005000d57a5c6400df86411b9981bef299deb1e8c973a350b11e8f3ac603a193`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2093fb76882879fc5517d526ca316eb05618850f5fd3daa8c950946e34fc24ce`  
		Last Modified: Wed, 13 Aug 2025 09:16:42 GMT  
		Size: 1.3 MB (1260194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8a596a6f7ae1c31f06473eb7f1d587ea75a7424b3dbecc7c0780422937852`  
		Last Modified: Wed, 13 Aug 2025 09:16:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5d0031eb3976169f0d81c7527effd0ffe4812bad7bcd0acfe66d6fa82fc0c0`  
		Last Modified: Wed, 13 Aug 2025 09:23:53 GMT  
		Size: 37.9 MB (37867541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff3dc5bb4af78e0ef402f8972ff060a4a925a1a4ace3e22550f797f1f31698`  
		Last Modified: Wed, 13 Aug 2025 09:23:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907ebaa06cd1295cb1a66ebbf912eafee334ce577246b80d4017e6d35a4dca7a`  
		Last Modified: Wed, 13 Aug 2025 22:17:48 GMT  
		Size: 5.9 MB (5908385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b853527fdeacadd65b23e9d37bfc5713a7241c43813edd3988441261522e5075`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab8f68f1e9e40bdda500351aa9e7a2b38d5906551ac8f5544a857f6d1b1e77`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032c6bd746e50e7b7c082621f667db99baac05330d4f52051ce6ba246a3e6b99`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d931b5b333a78735cd3ada972ab68a630d64c5c8169a9f2c1a8da6ef586fa6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73249d122bcc9643379894b1b6531966a9e4380226da3eb3ed639c7fdcc9b99b`

```dockerfile
```

-	Layers:
	-	`sha256:48518b2d36214bf578297f00300b46e74f671be91457f130eb4d9336b069a5ff`  
		Last Modified: Wed, 13 Aug 2025 23:28:22 GMT  
		Size: 2.3 MB (2285603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5061202e874c8a9137a61cdd64e1e5408ecfc3f02e16298cc0de054b2c3df615`  
		Last Modified: Wed, 13 Aug 2025 23:28:23 GMT  
		Size: 21.2 KB (21242 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:3bfbaf7f1ffb22a981b5e7dda8dad06a5620b64435fc9bef7797edc507dcc415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90da0d29ff1d896601979f7f5ab2e7d42a6d2cb7fdcef82756b7e5879e67da8e`
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
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:7b61b1398597ae15881ff464a9579b0e6a36c2c892c8b1b57f2f7cdeabb0232d`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 1.2 MB (1234683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab266ffb9d0322ee0c80bf4525c58d869463342abc3ef4de1f8c403a60a01192`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bc1cec816e3a53f6dc51ab6695d3ec9c3cbe0f0b48985630ed8e62192ac43`  
		Last Modified: Tue, 09 Sep 2025 03:41:17 GMT  
		Size: 37.7 MB (37730394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef9a0402a43858b4b35159ce01cf7a59853a8d814ea1c28004db99d3dd6f97f`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e668e135a42ee05d0ba0a59770170ba0de2d3eed0baa19b30af660026f4faf`  
		Last Modified: Tue, 09 Sep 2025 04:49:50 GMT  
		Size: 5.7 MB (5690183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7025af5322f18d0d01eea3476f555dc9dadc025ead3897a85242c3b0790c62`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ac61abdc71f1b8471416535baa300fcd27dd8ecbb006effdfcb5eca3f30465`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afc6502698d3bb76e6826a752d1a062258466a3ecc5037be44badebf7ffe904`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7141e369be10e7bdb7afca005e04f946b5b959d89b18f7da9e821aa52680eb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f72fc69dee6e025f1648a227bee99e377e7130fda9903824da531b6a5a512b`

```dockerfile
```

-	Layers:
	-	`sha256:8c36cfc11c8d0dfdf9b0e3522acf836a63225d6a6f638aaa3bc3102e391715be`  
		Last Modified: Tue, 09 Sep 2025 05:28:28 GMT  
		Size: 2.3 MB (2284892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a03a28068de559d2492658e68ed9e8a332d9c9f4f2f87c934795966e07b2c68`  
		Last Modified: Tue, 09 Sep 2025 05:28:29 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:60809130e540ba282fb497261ed202b534042d4c364e70ee99bedbf7b5049fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79478043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463289d853352175b0f583d4b62188d2bcbc5434b79dc5a9a472537a4d67800e`
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
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:1f3ed651bcf45dc8d6b2aa861f7982b10809d084dc996d19960a8fd6ae67679c`  
		Last Modified: Tue, 09 Sep 2025 01:03:25 GMT  
		Size: 1.3 MB (1259738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6f2d7d9697c7d27005eb8d0653bb31356a96aaf11157cd07fdc7122b9debd`  
		Last Modified: Tue, 09 Sep 2025 01:03:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca38028ecf75c470e6dcab31844c5e688b32b3588001bae7afcd1e568b8847`  
		Last Modified: Tue, 09 Sep 2025 01:48:01 GMT  
		Size: 42.1 MB (42063063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d674198437b5e8cab0a16102accad13d25d563c2a6d29e1dfdf8714bd57fe`  
		Last Modified: Tue, 09 Sep 2025 01:03:24 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea86b09599e70bddc9be118d14b4b2c0392947af222767c6ce9025749d7ec952`  
		Last Modified: Tue, 09 Sep 2025 02:29:43 GMT  
		Size: 6.0 MB (6016216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b99c977d6728cf8c1c24f2c6e9686030f04e43d8979f7194223785cb0b9209`  
		Last Modified: Tue, 09 Sep 2025 02:29:52 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac072aacd0d9972a7edd976c0cf04a4edf46e02b7e7d6b9e60e7a968e598286`  
		Last Modified: Tue, 09 Sep 2025 02:29:45 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f828884181523011879e6e9679c26555cc3034c75cfa41311604d7956b9d0a`  
		Last Modified: Tue, 09 Sep 2025 02:29:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9955b78921ef3210c523d857c795d628516bb00d630cbb8fbc9d34ff8becf3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec60ef8580b127ce74a8e6435db5a947341415b6be7cfee48dffde653c288b7`

```dockerfile
```

-	Layers:
	-	`sha256:a089b320e9bca83e08249bb4eae5e08b32f17dd6097860eab11282783c8a4f40`  
		Last Modified: Tue, 09 Sep 2025 05:28:33 GMT  
		Size: 2.3 MB (2283752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b1300c153bb28f7264cb101bb67f3eb4f78c7f1e032601890e6d80c56981f84`  
		Last Modified: Tue, 09 Sep 2025 05:28:34 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; 386

```console
$ docker pull fluentd@sha256:00c0ba7d40714f8a264e5c5e2fe9864ed612c6b64b313da61f7f615b62741ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76237114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0096cd93dfb8cff0d95f3b241fcd0b819f5d92490964f62433dd194484ef96b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfb18ad48f85fd4ca43130c11b60c8dd156cb1815fd08233be2be9c36c6923`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 1.3 MB (1285592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ae728bed6a475a8811b8b0a9460889cb5e0b9c9882d24089f9b3f37ea0ec1`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f33d4089ac39c16a1eb1172c1fd597771702897fc5472ebd4524ee51d009b1`  
		Last Modified: Mon, 08 Sep 2025 22:02:16 GMT  
		Size: 37.7 MB (37657047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1143329072f08996cee8c8782335612b6460d9af2d9c7b80994a10330d6565`  
		Last Modified: Mon, 08 Sep 2025 21:42:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c9149010179ce2a7385b9f1d4bba0926ec1a8f760320ce1a18344605fdefb`  
		Last Modified: Mon, 08 Sep 2025 22:56:47 GMT  
		Size: 6.0 MB (6002305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ae9af9420adf087b905e7979604a6aa9bbc3a4ec10861d9343cf60105fd1f6`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec1b97fb2027b8b637569ad830d697f5bfbc90b8073821f7667ab74bf5a7ee9`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e572568dc6a854cf5d202e39d57adff848138401e921cd90b5517c03a03b56`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c520f8feb045dc07ca91f1b801a18b3da2b99164328f5cea9e3d4617671fd805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a43abcc28180d678dd6fb3f2c34449f867fddd6ced15eca284444f3bed3254e`

```dockerfile
```

-	Layers:
	-	`sha256:4fd46796ac747472faab066b28d336aeb770dcd930f6a4574e047894e2f9c4e1`  
		Last Modified: Mon, 08 Sep 2025 23:28:40 GMT  
		Size: 2.3 MB (2280668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e027c0378727a4242ff878c5bf5d33ab554280d64bc99f99f42aa0b4ec277e`  
		Last Modified: Mon, 08 Sep 2025 23:28:41 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:578c42ba1e6fe6d220e34f814a6907ef7f0a68570a200cff2dad7b5be01a0063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80931845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554f74aaca5d4fb974f997565fce7312dc080508c46bcd65b969ad234174347d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ce8600c6aabffbd80bd501b7ac3a736f18377ed3e07f94e2ee78a82b4e4f36`  
		Last Modified: Wed, 13 Aug 2025 17:10:49 GMT  
		Size: 1.3 MB (1307302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beeaeb3c6936a2d2eb3b798f796525e15863a84f94eeac482b026abcf5e81681`  
		Last Modified: Wed, 13 Aug 2025 17:10:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff53e1f7034343e8070d6221a1160a532a7e0c29de8bbc1705dc7c38bedbb24`  
		Last Modified: Wed, 13 Aug 2025 17:20:51 GMT  
		Size: 39.5 MB (39501405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4abad74118dcd88bae1a1fab5137324bd11deded7bf240335b90943dcef30c`  
		Last Modified: Wed, 13 Aug 2025 17:20:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230e7efe3550ceb6d1b0edea559996448ddf4f137a78f786e726123946b0815c`  
		Last Modified: Thu, 14 Aug 2025 02:02:36 GMT  
		Size: 6.5 MB (6526530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d625b46b5e4f28fc6df5b2baa1399a290f56672bcc7d4558a66b3038c2232a33`  
		Last Modified: Thu, 14 Aug 2025 02:02:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711cdf0979bb42ee138c5cc2104ae40a16fc27e69d5ce3c47c4567168e8d15bc`  
		Last Modified: Thu, 14 Aug 2025 02:02:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af84d819228b1a405da1d867e01bf2775cafda73e14fd745cfa4323c8a4a1f1`  
		Last Modified: Thu, 14 Aug 2025 02:02:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b73585cc3502a53d8faf8e455384d82b34e9c09bb912756fef13757893f63e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aee2b306d1c9a5e7cd4cdcfd9e5171841a4efb08f14de805ddf09716943abb9`

```dockerfile
```

-	Layers:
	-	`sha256:2f6801a230c74e4b9aed5d3e1951eea3fefc7f11bb2333e136ede64cbf5eadd2`  
		Last Modified: Thu, 14 Aug 2025 02:28:32 GMT  
		Size: 2.3 MB (2286167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c3a3456832f73a97de5511ae14d2bb183385c903d0eb55970dec799fd33b44`  
		Last Modified: Thu, 14 Aug 2025 02:28:33 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-1` - linux; s390x

```console
$ docker pull fluentd@sha256:282b140069685c91b06cc70bd403db8dfc2175bf2114ccee46fef0f863576d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76691999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa2256db132f298feed82e53e31f7ba4e9a4ec15e6e001a81501b09c007b01b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56be941f806d82f4bf75185b333c5c589812220338507cb5d56baeeee8c5965`  
		Last Modified: Wed, 13 Aug 2025 06:50:22 GMT  
		Size: 1.3 MB (1292014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88df88585689c870b8cb13eccddc94febb777e8fb5f684a7ea31e4b5317929`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbba3b8727d5a05350927ba0dae09b37c2f43cf7ae85bf1a5ce90e04f03ab75`  
		Last Modified: Wed, 13 Aug 2025 05:54:45 GMT  
		Size: 39.2 MB (39180168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23cfe07c682626dbf88b68cf0822a38658eb00013c59f00bd48113d5788ecc`  
		Last Modified: Wed, 13 Aug 2025 05:54:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715644edf14c65a22fc17afc877e73e2481104398c62fc9f6612b110e99b19a2`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 6.4 MB (6384364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972751519e154187ceeadef8b4540fe82a0db5f10c3dfe19b879c762d3676ba9`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241a9530941b60d0de548b1cc1e87c8a4e1ad75c07e7f22d21aa4adcce58f039`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257fbad7ece230f4d601fe80c948945f942f732c27de9e5b66474557be69d0a`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0e3124818a6163f62aa958c1bcdd89be51c6dceda624ad1ef20863b89ad31c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd5961f5539cf8ac1e04fa9048683b8d10d088bd24da21691b4d97caf254a36`

```dockerfile
```

-	Layers:
	-	`sha256:c7822c267d4e80f00ed3c7f2cdee4230a544030e32a353eef79105538eb19362`  
		Last Modified: Wed, 13 Aug 2025 11:28:35 GMT  
		Size: 2.3 MB (2284077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929c64c079132a48ce0d1077d129e2a262a05d1d5c89af9da4583077965fd2bc`  
		Last Modified: Wed, 13 Aug 2025 11:28:36 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19-debian-1`

```console
$ docker pull fluentd@sha256:406eab0c90b337ea508a282d4917b61d046b740c7387c1dbb82c187e0b3d3716
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
$ docker pull fluentd@sha256:ba2a2644e30105d97209fa493cd9f9975f852353f7e4cffe9d67a2136fbea108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79117410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40476c6d4a4d9a86b707cf50405ed9380e4ec5b117499123be9cc96fb1c6165a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907bb64ed55e33da933ebd9b77bfa9382670074deb815d2e0d4f7d3067842ed1`  
		Last Modified: Mon, 08 Sep 2025 22:08:24 GMT  
		Size: 1.3 MB (1277837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676f670b77091f6f737a85b5792a0639bc680e827f931c13cb7e2fbfd0a38ebe`  
		Last Modified: Mon, 08 Sep 2025 22:08:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631f0e31bb9254d7f56d53693835aeb8d61c1c864ab85670b8997fb62d740e4f`  
		Last Modified: Mon, 08 Sep 2025 22:08:30 GMT  
		Size: 42.0 MB (42036169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836288d7f92195b5daec740a66ff4dbb4b6df0742d4a949a8892d634d98e848`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbaeb18472eaacfce9887b025572c879a5fdb37ef68212abe07046d303bd94f`  
		Last Modified: Mon, 08 Sep 2025 23:28:31 GMT  
		Size: 6.0 MB (6027518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7db22461d213e9de126e16bfc9c9ba9314204a0e3d6112828ac67310a6c22c`  
		Last Modified: Mon, 08 Sep 2025 22:52:04 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15320385f8b32e2c3cac705007a3fca3bf191963c690b6f79b18d84be24ea1f7`  
		Last Modified: Mon, 08 Sep 2025 22:52:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347687b79accd4531a1f20a4d16e10213e48ba7eb55000fa59074a4fe31d4fb8`  
		Last Modified: Mon, 08 Sep 2025 22:52:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:f3dbb0c12125fda2e678bb6e8c376992841ba1138f1103a1c30422801813a84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96ef1b79be01b1c63c29b78846c18b5a0cfba1c0539c180e46906dbe510cc0f`

```dockerfile
```

-	Layers:
	-	`sha256:013bd6ed603a8a9a894d817420ff1abc446eb10e3586662937791a6b464b9586`  
		Last Modified: Mon, 08 Sep 2025 23:28:25 GMT  
		Size: 2.3 MB (2283480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f96015f264b3386498c253b2b0f6bd011b1bbc30d826bbea742df498d1803687`  
		Last Modified: Mon, 08 Sep 2025 23:28:26 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:cb88f99f892373ab4cf6ee16b64d26e2c9d9910d3cac26cbb72e78a8d758d53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72980218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005000d57a5c6400df86411b9981bef299deb1e8c973a350b11e8f3ac603a193`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2093fb76882879fc5517d526ca316eb05618850f5fd3daa8c950946e34fc24ce`  
		Last Modified: Wed, 13 Aug 2025 09:16:42 GMT  
		Size: 1.3 MB (1260194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8a596a6f7ae1c31f06473eb7f1d587ea75a7424b3dbecc7c0780422937852`  
		Last Modified: Wed, 13 Aug 2025 09:16:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5d0031eb3976169f0d81c7527effd0ffe4812bad7bcd0acfe66d6fa82fc0c0`  
		Last Modified: Wed, 13 Aug 2025 09:23:53 GMT  
		Size: 37.9 MB (37867541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff3dc5bb4af78e0ef402f8972ff060a4a925a1a4ace3e22550f797f1f31698`  
		Last Modified: Wed, 13 Aug 2025 09:23:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907ebaa06cd1295cb1a66ebbf912eafee334ce577246b80d4017e6d35a4dca7a`  
		Last Modified: Wed, 13 Aug 2025 22:17:48 GMT  
		Size: 5.9 MB (5908385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b853527fdeacadd65b23e9d37bfc5713a7241c43813edd3988441261522e5075`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab8f68f1e9e40bdda500351aa9e7a2b38d5906551ac8f5544a857f6d1b1e77`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032c6bd746e50e7b7c082621f667db99baac05330d4f52051ce6ba246a3e6b99`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:d931b5b333a78735cd3ada972ab68a630d64c5c8169a9f2c1a8da6ef586fa6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73249d122bcc9643379894b1b6531966a9e4380226da3eb3ed639c7fdcc9b99b`

```dockerfile
```

-	Layers:
	-	`sha256:48518b2d36214bf578297f00300b46e74f671be91457f130eb4d9336b069a5ff`  
		Last Modified: Wed, 13 Aug 2025 23:28:22 GMT  
		Size: 2.3 MB (2285603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5061202e874c8a9137a61cdd64e1e5408ecfc3f02e16298cc0de054b2c3df615`  
		Last Modified: Wed, 13 Aug 2025 23:28:23 GMT  
		Size: 21.2 KB (21242 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:3bfbaf7f1ffb22a981b5e7dda8dad06a5620b64435fc9bef7797edc507dcc415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90da0d29ff1d896601979f7f5ab2e7d42a6d2cb7fdcef82756b7e5879e67da8e`
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
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:7b61b1398597ae15881ff464a9579b0e6a36c2c892c8b1b57f2f7cdeabb0232d`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 1.2 MB (1234683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab266ffb9d0322ee0c80bf4525c58d869463342abc3ef4de1f8c403a60a01192`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bc1cec816e3a53f6dc51ab6695d3ec9c3cbe0f0b48985630ed8e62192ac43`  
		Last Modified: Tue, 09 Sep 2025 03:41:17 GMT  
		Size: 37.7 MB (37730394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef9a0402a43858b4b35159ce01cf7a59853a8d814ea1c28004db99d3dd6f97f`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e668e135a42ee05d0ba0a59770170ba0de2d3eed0baa19b30af660026f4faf`  
		Last Modified: Tue, 09 Sep 2025 04:49:50 GMT  
		Size: 5.7 MB (5690183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7025af5322f18d0d01eea3476f555dc9dadc025ead3897a85242c3b0790c62`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ac61abdc71f1b8471416535baa300fcd27dd8ecbb006effdfcb5eca3f30465`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afc6502698d3bb76e6826a752d1a062258466a3ecc5037be44badebf7ffe904`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:7141e369be10e7bdb7afca005e04f946b5b959d89b18f7da9e821aa52680eb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f72fc69dee6e025f1648a227bee99e377e7130fda9903824da531b6a5a512b`

```dockerfile
```

-	Layers:
	-	`sha256:8c36cfc11c8d0dfdf9b0e3522acf836a63225d6a6f638aaa3bc3102e391715be`  
		Last Modified: Tue, 09 Sep 2025 05:28:28 GMT  
		Size: 2.3 MB (2284892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a03a28068de559d2492658e68ed9e8a332d9c9f4f2f87c934795966e07b2c68`  
		Last Modified: Tue, 09 Sep 2025 05:28:29 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:60809130e540ba282fb497261ed202b534042d4c364e70ee99bedbf7b5049fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79478043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463289d853352175b0f583d4b62188d2bcbc5434b79dc5a9a472537a4d67800e`
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
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:1f3ed651bcf45dc8d6b2aa861f7982b10809d084dc996d19960a8fd6ae67679c`  
		Last Modified: Tue, 09 Sep 2025 01:03:25 GMT  
		Size: 1.3 MB (1259738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6f2d7d9697c7d27005eb8d0653bb31356a96aaf11157cd07fdc7122b9debd`  
		Last Modified: Tue, 09 Sep 2025 01:03:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca38028ecf75c470e6dcab31844c5e688b32b3588001bae7afcd1e568b8847`  
		Last Modified: Tue, 09 Sep 2025 01:48:01 GMT  
		Size: 42.1 MB (42063063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d674198437b5e8cab0a16102accad13d25d563c2a6d29e1dfdf8714bd57fe`  
		Last Modified: Tue, 09 Sep 2025 01:03:24 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea86b09599e70bddc9be118d14b4b2c0392947af222767c6ce9025749d7ec952`  
		Last Modified: Tue, 09 Sep 2025 02:29:43 GMT  
		Size: 6.0 MB (6016216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b99c977d6728cf8c1c24f2c6e9686030f04e43d8979f7194223785cb0b9209`  
		Last Modified: Tue, 09 Sep 2025 02:29:52 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac072aacd0d9972a7edd976c0cf04a4edf46e02b7e7d6b9e60e7a968e598286`  
		Last Modified: Tue, 09 Sep 2025 02:29:45 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f828884181523011879e6e9679c26555cc3034c75cfa41311604d7956b9d0a`  
		Last Modified: Tue, 09 Sep 2025 02:29:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:9955b78921ef3210c523d857c795d628516bb00d630cbb8fbc9d34ff8becf3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec60ef8580b127ce74a8e6435db5a947341415b6be7cfee48dffde653c288b7`

```dockerfile
```

-	Layers:
	-	`sha256:a089b320e9bca83e08249bb4eae5e08b32f17dd6097860eab11282783c8a4f40`  
		Last Modified: Tue, 09 Sep 2025 05:28:33 GMT  
		Size: 2.3 MB (2283752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b1300c153bb28f7264cb101bb67f3eb4f78c7f1e032601890e6d80c56981f84`  
		Last Modified: Tue, 09 Sep 2025 05:28:34 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; 386

```console
$ docker pull fluentd@sha256:00c0ba7d40714f8a264e5c5e2fe9864ed612c6b64b313da61f7f615b62741ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76237114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0096cd93dfb8cff0d95f3b241fcd0b819f5d92490964f62433dd194484ef96b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfb18ad48f85fd4ca43130c11b60c8dd156cb1815fd08233be2be9c36c6923`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 1.3 MB (1285592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ae728bed6a475a8811b8b0a9460889cb5e0b9c9882d24089f9b3f37ea0ec1`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f33d4089ac39c16a1eb1172c1fd597771702897fc5472ebd4524ee51d009b1`  
		Last Modified: Mon, 08 Sep 2025 22:02:16 GMT  
		Size: 37.7 MB (37657047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1143329072f08996cee8c8782335612b6460d9af2d9c7b80994a10330d6565`  
		Last Modified: Mon, 08 Sep 2025 21:42:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c9149010179ce2a7385b9f1d4bba0926ec1a8f760320ce1a18344605fdefb`  
		Last Modified: Mon, 08 Sep 2025 22:56:47 GMT  
		Size: 6.0 MB (6002305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ae9af9420adf087b905e7979604a6aa9bbc3a4ec10861d9343cf60105fd1f6`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec1b97fb2027b8b637569ad830d697f5bfbc90b8073821f7667ab74bf5a7ee9`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e572568dc6a854cf5d202e39d57adff848138401e921cd90b5517c03a03b56`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:c520f8feb045dc07ca91f1b801a18b3da2b99164328f5cea9e3d4617671fd805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a43abcc28180d678dd6fb3f2c34449f867fddd6ced15eca284444f3bed3254e`

```dockerfile
```

-	Layers:
	-	`sha256:4fd46796ac747472faab066b28d336aeb770dcd930f6a4574e047894e2f9c4e1`  
		Last Modified: Mon, 08 Sep 2025 23:28:40 GMT  
		Size: 2.3 MB (2280668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e027c0378727a4242ff878c5bf5d33ab554280d64bc99f99f42aa0b4ec277e`  
		Last Modified: Mon, 08 Sep 2025 23:28:41 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; ppc64le

```console
$ docker pull fluentd@sha256:578c42ba1e6fe6d220e34f814a6907ef7f0a68570a200cff2dad7b5be01a0063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80931845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554f74aaca5d4fb974f997565fce7312dc080508c46bcd65b969ad234174347d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ce8600c6aabffbd80bd501b7ac3a736f18377ed3e07f94e2ee78a82b4e4f36`  
		Last Modified: Wed, 13 Aug 2025 17:10:49 GMT  
		Size: 1.3 MB (1307302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beeaeb3c6936a2d2eb3b798f796525e15863a84f94eeac482b026abcf5e81681`  
		Last Modified: Wed, 13 Aug 2025 17:10:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff53e1f7034343e8070d6221a1160a532a7e0c29de8bbc1705dc7c38bedbb24`  
		Last Modified: Wed, 13 Aug 2025 17:20:51 GMT  
		Size: 39.5 MB (39501405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4abad74118dcd88bae1a1fab5137324bd11deded7bf240335b90943dcef30c`  
		Last Modified: Wed, 13 Aug 2025 17:20:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230e7efe3550ceb6d1b0edea559996448ddf4f137a78f786e726123946b0815c`  
		Last Modified: Thu, 14 Aug 2025 02:02:36 GMT  
		Size: 6.5 MB (6526530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d625b46b5e4f28fc6df5b2baa1399a290f56672bcc7d4558a66b3038c2232a33`  
		Last Modified: Thu, 14 Aug 2025 02:02:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711cdf0979bb42ee138c5cc2104ae40a16fc27e69d5ce3c47c4567168e8d15bc`  
		Last Modified: Thu, 14 Aug 2025 02:02:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af84d819228b1a405da1d867e01bf2775cafda73e14fd745cfa4323c8a4a1f1`  
		Last Modified: Thu, 14 Aug 2025 02:02:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:b73585cc3502a53d8faf8e455384d82b34e9c09bb912756fef13757893f63e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aee2b306d1c9a5e7cd4cdcfd9e5171841a4efb08f14de805ddf09716943abb9`

```dockerfile
```

-	Layers:
	-	`sha256:2f6801a230c74e4b9aed5d3e1951eea3fefc7f11bb2333e136ede64cbf5eadd2`  
		Last Modified: Thu, 14 Aug 2025 02:28:32 GMT  
		Size: 2.3 MB (2286167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c3a3456832f73a97de5511ae14d2bb183385c903d0eb55970dec799fd33b44`  
		Last Modified: Thu, 14 Aug 2025 02:28:33 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19-debian-1` - linux; s390x

```console
$ docker pull fluentd@sha256:282b140069685c91b06cc70bd403db8dfc2175bf2114ccee46fef0f863576d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76691999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa2256db132f298feed82e53e31f7ba4e9a4ec15e6e001a81501b09c007b01b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56be941f806d82f4bf75185b333c5c589812220338507cb5d56baeeee8c5965`  
		Last Modified: Wed, 13 Aug 2025 06:50:22 GMT  
		Size: 1.3 MB (1292014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88df88585689c870b8cb13eccddc94febb777e8fb5f684a7ea31e4b5317929`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbba3b8727d5a05350927ba0dae09b37c2f43cf7ae85bf1a5ce90e04f03ab75`  
		Last Modified: Wed, 13 Aug 2025 05:54:45 GMT  
		Size: 39.2 MB (39180168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23cfe07c682626dbf88b68cf0822a38658eb00013c59f00bd48113d5788ecc`  
		Last Modified: Wed, 13 Aug 2025 05:54:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715644edf14c65a22fc17afc877e73e2481104398c62fc9f6612b110e99b19a2`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 6.4 MB (6384364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972751519e154187ceeadef8b4540fe82a0db5f10c3dfe19b879c762d3676ba9`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241a9530941b60d0de548b1cc1e87c8a4e1ad75c07e7f22d21aa4adcce58f039`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257fbad7ece230f4d601fe80c948945f942f732c27de9e5b66474557be69d0a`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19-debian-1` - unknown; unknown

```console
$ docker pull fluentd@sha256:0e3124818a6163f62aa958c1bcdd89be51c6dceda624ad1ef20863b89ad31c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd5961f5539cf8ac1e04fa9048683b8d10d088bd24da21691b4d97caf254a36`

```dockerfile
```

-	Layers:
	-	`sha256:c7822c267d4e80f00ed3c7f2cdee4230a544030e32a353eef79105538eb19362`  
		Last Modified: Wed, 13 Aug 2025 11:28:35 GMT  
		Size: 2.3 MB (2284077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929c64c079132a48ce0d1077d129e2a262a05d1d5c89af9da4583077965fd2bc`  
		Last Modified: Wed, 13 Aug 2025 11:28:36 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.0-1.0`

```console
$ docker pull fluentd@sha256:406eab0c90b337ea508a282d4917b61d046b740c7387c1dbb82c187e0b3d3716
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
$ docker pull fluentd@sha256:ba2a2644e30105d97209fa493cd9f9975f852353f7e4cffe9d67a2136fbea108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79117410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40476c6d4a4d9a86b707cf50405ed9380e4ec5b117499123be9cc96fb1c6165a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907bb64ed55e33da933ebd9b77bfa9382670074deb815d2e0d4f7d3067842ed1`  
		Last Modified: Mon, 08 Sep 2025 22:08:24 GMT  
		Size: 1.3 MB (1277837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676f670b77091f6f737a85b5792a0639bc680e827f931c13cb7e2fbfd0a38ebe`  
		Last Modified: Mon, 08 Sep 2025 22:08:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631f0e31bb9254d7f56d53693835aeb8d61c1c864ab85670b8997fb62d740e4f`  
		Last Modified: Mon, 08 Sep 2025 22:08:30 GMT  
		Size: 42.0 MB (42036169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836288d7f92195b5daec740a66ff4dbb4b6df0742d4a949a8892d634d98e848`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbaeb18472eaacfce9887b025572c879a5fdb37ef68212abe07046d303bd94f`  
		Last Modified: Mon, 08 Sep 2025 23:28:31 GMT  
		Size: 6.0 MB (6027518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7db22461d213e9de126e16bfc9c9ba9314204a0e3d6112828ac67310a6c22c`  
		Last Modified: Mon, 08 Sep 2025 22:52:04 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15320385f8b32e2c3cac705007a3fca3bf191963c690b6f79b18d84be24ea1f7`  
		Last Modified: Mon, 08 Sep 2025 22:52:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347687b79accd4531a1f20a4d16e10213e48ba7eb55000fa59074a4fe31d4fb8`  
		Last Modified: Mon, 08 Sep 2025 22:52:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f3dbb0c12125fda2e678bb6e8c376992841ba1138f1103a1c30422801813a84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96ef1b79be01b1c63c29b78846c18b5a0cfba1c0539c180e46906dbe510cc0f`

```dockerfile
```

-	Layers:
	-	`sha256:013bd6ed603a8a9a894d817420ff1abc446eb10e3586662937791a6b464b9586`  
		Last Modified: Mon, 08 Sep 2025 23:28:25 GMT  
		Size: 2.3 MB (2283480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f96015f264b3386498c253b2b0f6bd011b1bbc30d826bbea742df498d1803687`  
		Last Modified: Mon, 08 Sep 2025 23:28:26 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:cb88f99f892373ab4cf6ee16b64d26e2c9d9910d3cac26cbb72e78a8d758d53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72980218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005000d57a5c6400df86411b9981bef299deb1e8c973a350b11e8f3ac603a193`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2093fb76882879fc5517d526ca316eb05618850f5fd3daa8c950946e34fc24ce`  
		Last Modified: Wed, 13 Aug 2025 09:16:42 GMT  
		Size: 1.3 MB (1260194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8a596a6f7ae1c31f06473eb7f1d587ea75a7424b3dbecc7c0780422937852`  
		Last Modified: Wed, 13 Aug 2025 09:16:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5d0031eb3976169f0d81c7527effd0ffe4812bad7bcd0acfe66d6fa82fc0c0`  
		Last Modified: Wed, 13 Aug 2025 09:23:53 GMT  
		Size: 37.9 MB (37867541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff3dc5bb4af78e0ef402f8972ff060a4a925a1a4ace3e22550f797f1f31698`  
		Last Modified: Wed, 13 Aug 2025 09:23:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907ebaa06cd1295cb1a66ebbf912eafee334ce577246b80d4017e6d35a4dca7a`  
		Last Modified: Wed, 13 Aug 2025 22:17:48 GMT  
		Size: 5.9 MB (5908385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b853527fdeacadd65b23e9d37bfc5713a7241c43813edd3988441261522e5075`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab8f68f1e9e40bdda500351aa9e7a2b38d5906551ac8f5544a857f6d1b1e77`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032c6bd746e50e7b7c082621f667db99baac05330d4f52051ce6ba246a3e6b99`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:d931b5b333a78735cd3ada972ab68a630d64c5c8169a9f2c1a8da6ef586fa6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73249d122bcc9643379894b1b6531966a9e4380226da3eb3ed639c7fdcc9b99b`

```dockerfile
```

-	Layers:
	-	`sha256:48518b2d36214bf578297f00300b46e74f671be91457f130eb4d9336b069a5ff`  
		Last Modified: Wed, 13 Aug 2025 23:28:22 GMT  
		Size: 2.3 MB (2285603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5061202e874c8a9137a61cdd64e1e5408ecfc3f02e16298cc0de054b2c3df615`  
		Last Modified: Wed, 13 Aug 2025 23:28:23 GMT  
		Size: 21.2 KB (21242 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:3bfbaf7f1ffb22a981b5e7dda8dad06a5620b64435fc9bef7797edc507dcc415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90da0d29ff1d896601979f7f5ab2e7d42a6d2cb7fdcef82756b7e5879e67da8e`
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
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:7b61b1398597ae15881ff464a9579b0e6a36c2c892c8b1b57f2f7cdeabb0232d`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 1.2 MB (1234683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab266ffb9d0322ee0c80bf4525c58d869463342abc3ef4de1f8c403a60a01192`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bc1cec816e3a53f6dc51ab6695d3ec9c3cbe0f0b48985630ed8e62192ac43`  
		Last Modified: Tue, 09 Sep 2025 03:41:17 GMT  
		Size: 37.7 MB (37730394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef9a0402a43858b4b35159ce01cf7a59853a8d814ea1c28004db99d3dd6f97f`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e668e135a42ee05d0ba0a59770170ba0de2d3eed0baa19b30af660026f4faf`  
		Last Modified: Tue, 09 Sep 2025 04:49:50 GMT  
		Size: 5.7 MB (5690183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7025af5322f18d0d01eea3476f555dc9dadc025ead3897a85242c3b0790c62`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ac61abdc71f1b8471416535baa300fcd27dd8ecbb006effdfcb5eca3f30465`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afc6502698d3bb76e6826a752d1a062258466a3ecc5037be44badebf7ffe904`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7141e369be10e7bdb7afca005e04f946b5b959d89b18f7da9e821aa52680eb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f72fc69dee6e025f1648a227bee99e377e7130fda9903824da531b6a5a512b`

```dockerfile
```

-	Layers:
	-	`sha256:8c36cfc11c8d0dfdf9b0e3522acf836a63225d6a6f638aaa3bc3102e391715be`  
		Last Modified: Tue, 09 Sep 2025 05:28:28 GMT  
		Size: 2.3 MB (2284892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a03a28068de559d2492658e68ed9e8a332d9c9f4f2f87c934795966e07b2c68`  
		Last Modified: Tue, 09 Sep 2025 05:28:29 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:60809130e540ba282fb497261ed202b534042d4c364e70ee99bedbf7b5049fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79478043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463289d853352175b0f583d4b62188d2bcbc5434b79dc5a9a472537a4d67800e`
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
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:1f3ed651bcf45dc8d6b2aa861f7982b10809d084dc996d19960a8fd6ae67679c`  
		Last Modified: Tue, 09 Sep 2025 01:03:25 GMT  
		Size: 1.3 MB (1259738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6f2d7d9697c7d27005eb8d0653bb31356a96aaf11157cd07fdc7122b9debd`  
		Last Modified: Tue, 09 Sep 2025 01:03:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca38028ecf75c470e6dcab31844c5e688b32b3588001bae7afcd1e568b8847`  
		Last Modified: Tue, 09 Sep 2025 01:48:01 GMT  
		Size: 42.1 MB (42063063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d674198437b5e8cab0a16102accad13d25d563c2a6d29e1dfdf8714bd57fe`  
		Last Modified: Tue, 09 Sep 2025 01:03:24 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea86b09599e70bddc9be118d14b4b2c0392947af222767c6ce9025749d7ec952`  
		Last Modified: Tue, 09 Sep 2025 02:29:43 GMT  
		Size: 6.0 MB (6016216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b99c977d6728cf8c1c24f2c6e9686030f04e43d8979f7194223785cb0b9209`  
		Last Modified: Tue, 09 Sep 2025 02:29:52 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac072aacd0d9972a7edd976c0cf04a4edf46e02b7e7d6b9e60e7a968e598286`  
		Last Modified: Tue, 09 Sep 2025 02:29:45 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f828884181523011879e6e9679c26555cc3034c75cfa41311604d7956b9d0a`  
		Last Modified: Tue, 09 Sep 2025 02:29:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9955b78921ef3210c523d857c795d628516bb00d630cbb8fbc9d34ff8becf3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec60ef8580b127ce74a8e6435db5a947341415b6be7cfee48dffde653c288b7`

```dockerfile
```

-	Layers:
	-	`sha256:a089b320e9bca83e08249bb4eae5e08b32f17dd6097860eab11282783c8a4f40`  
		Last Modified: Tue, 09 Sep 2025 05:28:33 GMT  
		Size: 2.3 MB (2283752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b1300c153bb28f7264cb101bb67f3eb4f78c7f1e032601890e6d80c56981f84`  
		Last Modified: Tue, 09 Sep 2025 05:28:34 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:00c0ba7d40714f8a264e5c5e2fe9864ed612c6b64b313da61f7f615b62741ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76237114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0096cd93dfb8cff0d95f3b241fcd0b819f5d92490964f62433dd194484ef96b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfb18ad48f85fd4ca43130c11b60c8dd156cb1815fd08233be2be9c36c6923`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 1.3 MB (1285592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ae728bed6a475a8811b8b0a9460889cb5e0b9c9882d24089f9b3f37ea0ec1`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f33d4089ac39c16a1eb1172c1fd597771702897fc5472ebd4524ee51d009b1`  
		Last Modified: Mon, 08 Sep 2025 22:02:16 GMT  
		Size: 37.7 MB (37657047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1143329072f08996cee8c8782335612b6460d9af2d9c7b80994a10330d6565`  
		Last Modified: Mon, 08 Sep 2025 21:42:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c9149010179ce2a7385b9f1d4bba0926ec1a8f760320ce1a18344605fdefb`  
		Last Modified: Mon, 08 Sep 2025 22:56:47 GMT  
		Size: 6.0 MB (6002305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ae9af9420adf087b905e7979604a6aa9bbc3a4ec10861d9343cf60105fd1f6`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec1b97fb2027b8b637569ad830d697f5bfbc90b8073821f7667ab74bf5a7ee9`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e572568dc6a854cf5d202e39d57adff848138401e921cd90b5517c03a03b56`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c520f8feb045dc07ca91f1b801a18b3da2b99164328f5cea9e3d4617671fd805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a43abcc28180d678dd6fb3f2c34449f867fddd6ced15eca284444f3bed3254e`

```dockerfile
```

-	Layers:
	-	`sha256:4fd46796ac747472faab066b28d336aeb770dcd930f6a4574e047894e2f9c4e1`  
		Last Modified: Mon, 08 Sep 2025 23:28:40 GMT  
		Size: 2.3 MB (2280668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e027c0378727a4242ff878c5bf5d33ab554280d64bc99f99f42aa0b4ec277e`  
		Last Modified: Mon, 08 Sep 2025 23:28:41 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:578c42ba1e6fe6d220e34f814a6907ef7f0a68570a200cff2dad7b5be01a0063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80931845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554f74aaca5d4fb974f997565fce7312dc080508c46bcd65b969ad234174347d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ce8600c6aabffbd80bd501b7ac3a736f18377ed3e07f94e2ee78a82b4e4f36`  
		Last Modified: Wed, 13 Aug 2025 17:10:49 GMT  
		Size: 1.3 MB (1307302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beeaeb3c6936a2d2eb3b798f796525e15863a84f94eeac482b026abcf5e81681`  
		Last Modified: Wed, 13 Aug 2025 17:10:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff53e1f7034343e8070d6221a1160a532a7e0c29de8bbc1705dc7c38bedbb24`  
		Last Modified: Wed, 13 Aug 2025 17:20:51 GMT  
		Size: 39.5 MB (39501405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4abad74118dcd88bae1a1fab5137324bd11deded7bf240335b90943dcef30c`  
		Last Modified: Wed, 13 Aug 2025 17:20:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230e7efe3550ceb6d1b0edea559996448ddf4f137a78f786e726123946b0815c`  
		Last Modified: Thu, 14 Aug 2025 02:02:36 GMT  
		Size: 6.5 MB (6526530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d625b46b5e4f28fc6df5b2baa1399a290f56672bcc7d4558a66b3038c2232a33`  
		Last Modified: Thu, 14 Aug 2025 02:02:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711cdf0979bb42ee138c5cc2104ae40a16fc27e69d5ce3c47c4567168e8d15bc`  
		Last Modified: Thu, 14 Aug 2025 02:02:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af84d819228b1a405da1d867e01bf2775cafda73e14fd745cfa4323c8a4a1f1`  
		Last Modified: Thu, 14 Aug 2025 02:02:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b73585cc3502a53d8faf8e455384d82b34e9c09bb912756fef13757893f63e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aee2b306d1c9a5e7cd4cdcfd9e5171841a4efb08f14de805ddf09716943abb9`

```dockerfile
```

-	Layers:
	-	`sha256:2f6801a230c74e4b9aed5d3e1951eea3fefc7f11bb2333e136ede64cbf5eadd2`  
		Last Modified: Thu, 14 Aug 2025 02:28:32 GMT  
		Size: 2.3 MB (2286167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c3a3456832f73a97de5511ae14d2bb183385c903d0eb55970dec799fd33b44`  
		Last Modified: Thu, 14 Aug 2025 02:28:33 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:282b140069685c91b06cc70bd403db8dfc2175bf2114ccee46fef0f863576d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76691999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa2256db132f298feed82e53e31f7ba4e9a4ec15e6e001a81501b09c007b01b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56be941f806d82f4bf75185b333c5c589812220338507cb5d56baeeee8c5965`  
		Last Modified: Wed, 13 Aug 2025 06:50:22 GMT  
		Size: 1.3 MB (1292014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88df88585689c870b8cb13eccddc94febb777e8fb5f684a7ea31e4b5317929`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbba3b8727d5a05350927ba0dae09b37c2f43cf7ae85bf1a5ce90e04f03ab75`  
		Last Modified: Wed, 13 Aug 2025 05:54:45 GMT  
		Size: 39.2 MB (39180168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23cfe07c682626dbf88b68cf0822a38658eb00013c59f00bd48113d5788ecc`  
		Last Modified: Wed, 13 Aug 2025 05:54:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715644edf14c65a22fc17afc877e73e2481104398c62fc9f6612b110e99b19a2`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 6.4 MB (6384364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972751519e154187ceeadef8b4540fe82a0db5f10c3dfe19b879c762d3676ba9`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241a9530941b60d0de548b1cc1e87c8a4e1ad75c07e7f22d21aa4adcce58f039`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257fbad7ece230f4d601fe80c948945f942f732c27de9e5b66474557be69d0a`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0e3124818a6163f62aa958c1bcdd89be51c6dceda624ad1ef20863b89ad31c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd5961f5539cf8ac1e04fa9048683b8d10d088bd24da21691b4d97caf254a36`

```dockerfile
```

-	Layers:
	-	`sha256:c7822c267d4e80f00ed3c7f2cdee4230a544030e32a353eef79105538eb19362`  
		Last Modified: Wed, 13 Aug 2025 11:28:35 GMT  
		Size: 2.3 MB (2284077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929c64c079132a48ce0d1077d129e2a262a05d1d5c89af9da4583077965fd2bc`  
		Last Modified: Wed, 13 Aug 2025 11:28:36 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

## `fluentd:v1.19.0-debian-1.0`

```console
$ docker pull fluentd@sha256:406eab0c90b337ea508a282d4917b61d046b740c7387c1dbb82c187e0b3d3716
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
$ docker pull fluentd@sha256:ba2a2644e30105d97209fa493cd9f9975f852353f7e4cffe9d67a2136fbea108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79117410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40476c6d4a4d9a86b707cf50405ed9380e4ec5b117499123be9cc96fb1c6165a`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907bb64ed55e33da933ebd9b77bfa9382670074deb815d2e0d4f7d3067842ed1`  
		Last Modified: Mon, 08 Sep 2025 22:08:24 GMT  
		Size: 1.3 MB (1277837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:676f670b77091f6f737a85b5792a0639bc680e827f931c13cb7e2fbfd0a38ebe`  
		Last Modified: Mon, 08 Sep 2025 22:08:23 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631f0e31bb9254d7f56d53693835aeb8d61c1c864ab85670b8997fb62d740e4f`  
		Last Modified: Mon, 08 Sep 2025 22:08:30 GMT  
		Size: 42.0 MB (42036169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7836288d7f92195b5daec740a66ff4dbb4b6df0742d4a949a8892d634d98e848`  
		Last Modified: Mon, 08 Sep 2025 22:08:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbaeb18472eaacfce9887b025572c879a5fdb37ef68212abe07046d303bd94f`  
		Last Modified: Mon, 08 Sep 2025 23:28:31 GMT  
		Size: 6.0 MB (6027518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7db22461d213e9de126e16bfc9c9ba9314204a0e3d6112828ac67310a6c22c`  
		Last Modified: Mon, 08 Sep 2025 22:52:04 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15320385f8b32e2c3cac705007a3fca3bf191963c690b6f79b18d84be24ea1f7`  
		Last Modified: Mon, 08 Sep 2025 22:52:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347687b79accd4531a1f20a4d16e10213e48ba7eb55000fa59074a4fe31d4fb8`  
		Last Modified: Mon, 08 Sep 2025 22:52:13 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:f3dbb0c12125fda2e678bb6e8c376992841ba1138f1103a1c30422801813a84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96ef1b79be01b1c63c29b78846c18b5a0cfba1c0539c180e46906dbe510cc0f`

```dockerfile
```

-	Layers:
	-	`sha256:013bd6ed603a8a9a894d817420ff1abc446eb10e3586662937791a6b464b9586`  
		Last Modified: Mon, 08 Sep 2025 23:28:25 GMT  
		Size: 2.3 MB (2283480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f96015f264b3386498c253b2b0f6bd011b1bbc30d826bbea742df498d1803687`  
		Last Modified: Mon, 08 Sep 2025 23:28:26 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm variant v5

```console
$ docker pull fluentd@sha256:cb88f99f892373ab4cf6ee16b64d26e2c9d9910d3cac26cbb72e78a8d758d53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72980218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005000d57a5c6400df86411b9981bef299deb1e8c973a350b11e8f3ac603a193`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2093fb76882879fc5517d526ca316eb05618850f5fd3daa8c950946e34fc24ce`  
		Last Modified: Wed, 13 Aug 2025 09:16:42 GMT  
		Size: 1.3 MB (1260194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ba8a596a6f7ae1c31f06473eb7f1d587ea75a7424b3dbecc7c0780422937852`  
		Last Modified: Wed, 13 Aug 2025 09:16:43 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5d0031eb3976169f0d81c7527effd0ffe4812bad7bcd0acfe66d6fa82fc0c0`  
		Last Modified: Wed, 13 Aug 2025 09:23:53 GMT  
		Size: 37.9 MB (37867541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff3dc5bb4af78e0ef402f8972ff060a4a925a1a4ace3e22550f797f1f31698`  
		Last Modified: Wed, 13 Aug 2025 09:23:44 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907ebaa06cd1295cb1a66ebbf912eafee334ce577246b80d4017e6d35a4dca7a`  
		Last Modified: Wed, 13 Aug 2025 22:17:48 GMT  
		Size: 5.9 MB (5908385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b853527fdeacadd65b23e9d37bfc5713a7241c43813edd3988441261522e5075`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab8f68f1e9e40bdda500351aa9e7a2b38d5906551ac8f5544a857f6d1b1e77`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032c6bd746e50e7b7c082621f667db99baac05330d4f52051ce6ba246a3e6b99`  
		Last Modified: Wed, 13 Aug 2025 22:17:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:d931b5b333a78735cd3ada972ab68a630d64c5c8169a9f2c1a8da6ef586fa6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73249d122bcc9643379894b1b6531966a9e4380226da3eb3ed639c7fdcc9b99b`

```dockerfile
```

-	Layers:
	-	`sha256:48518b2d36214bf578297f00300b46e74f671be91457f130eb4d9336b069a5ff`  
		Last Modified: Wed, 13 Aug 2025 23:28:22 GMT  
		Size: 2.3 MB (2285603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5061202e874c8a9137a61cdd64e1e5408ecfc3f02e16298cc0de054b2c3df615`  
		Last Modified: Wed, 13 Aug 2025 23:28:23 GMT  
		Size: 21.2 KB (21242 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm variant v7

```console
$ docker pull fluentd@sha256:3bfbaf7f1ffb22a981b5e7dda8dad06a5620b64435fc9bef7797edc507dcc415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70865498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90da0d29ff1d896601979f7f5ab2e7d42a6d2cb7fdcef82756b7e5879e67da8e`
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
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:7b61b1398597ae15881ff464a9579b0e6a36c2c892c8b1b57f2f7cdeabb0232d`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 1.2 MB (1234683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab266ffb9d0322ee0c80bf4525c58d869463342abc3ef4de1f8c403a60a01192`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1bc1cec816e3a53f6dc51ab6695d3ec9c3cbe0f0b48985630ed8e62192ac43`  
		Last Modified: Tue, 09 Sep 2025 03:41:17 GMT  
		Size: 37.7 MB (37730394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef9a0402a43858b4b35159ce01cf7a59853a8d814ea1c28004db99d3dd6f97f`  
		Last Modified: Tue, 09 Sep 2025 01:41:45 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7e668e135a42ee05d0ba0a59770170ba0de2d3eed0baa19b30af660026f4faf`  
		Last Modified: Tue, 09 Sep 2025 04:49:50 GMT  
		Size: 5.7 MB (5690183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7025af5322f18d0d01eea3476f555dc9dadc025ead3897a85242c3b0790c62`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ac61abdc71f1b8471416535baa300fcd27dd8ecbb006effdfcb5eca3f30465`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afc6502698d3bb76e6826a752d1a062258466a3ecc5037be44badebf7ffe904`  
		Last Modified: Tue, 09 Sep 2025 04:26:04 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:7141e369be10e7bdb7afca005e04f946b5b959d89b18f7da9e821aa52680eb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2306138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f72fc69dee6e025f1648a227bee99e377e7130fda9903824da531b6a5a512b`

```dockerfile
```

-	Layers:
	-	`sha256:8c36cfc11c8d0dfdf9b0e3522acf836a63225d6a6f638aaa3bc3102e391715be`  
		Last Modified: Tue, 09 Sep 2025 05:28:28 GMT  
		Size: 2.3 MB (2284892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a03a28068de559d2492658e68ed9e8a332d9c9f4f2f87c934795966e07b2c68`  
		Last Modified: Tue, 09 Sep 2025 05:28:29 GMT  
		Size: 21.2 KB (21246 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; arm64 variant v8

```console
$ docker pull fluentd@sha256:60809130e540ba282fb497261ed202b534042d4c364e70ee99bedbf7b5049fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79478043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463289d853352175b0f583d4b62188d2bcbc5434b79dc5a9a472537a4d67800e`
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
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:1f3ed651bcf45dc8d6b2aa861f7982b10809d084dc996d19960a8fd6ae67679c`  
		Last Modified: Tue, 09 Sep 2025 01:03:25 GMT  
		Size: 1.3 MB (1259738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b6f2d7d9697c7d27005eb8d0653bb31356a96aaf11157cd07fdc7122b9debd`  
		Last Modified: Tue, 09 Sep 2025 01:03:29 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca38028ecf75c470e6dcab31844c5e688b32b3588001bae7afcd1e568b8847`  
		Last Modified: Tue, 09 Sep 2025 01:48:01 GMT  
		Size: 42.1 MB (42063063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2d674198437b5e8cab0a16102accad13d25d563c2a6d29e1dfdf8714bd57fe`  
		Last Modified: Tue, 09 Sep 2025 01:03:24 GMT  
		Size: 142.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea86b09599e70bddc9be118d14b4b2c0392947af222767c6ce9025749d7ec952`  
		Last Modified: Tue, 09 Sep 2025 02:29:43 GMT  
		Size: 6.0 MB (6016216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b99c977d6728cf8c1c24f2c6e9686030f04e43d8979f7194223785cb0b9209`  
		Last Modified: Tue, 09 Sep 2025 02:29:52 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac072aacd0d9972a7edd976c0cf04a4edf46e02b7e7d6b9e60e7a968e598286`  
		Last Modified: Tue, 09 Sep 2025 02:29:45 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f828884181523011879e6e9679c26555cc3034c75cfa41311604d7956b9d0a`  
		Last Modified: Tue, 09 Sep 2025 02:29:53 GMT  
		Size: 478.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:9955b78921ef3210c523d857c795d628516bb00d630cbb8fbc9d34ff8becf3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec60ef8580b127ce74a8e6435db5a947341415b6be7cfee48dffde653c288b7`

```dockerfile
```

-	Layers:
	-	`sha256:a089b320e9bca83e08249bb4eae5e08b32f17dd6097860eab11282783c8a4f40`  
		Last Modified: Tue, 09 Sep 2025 05:28:33 GMT  
		Size: 2.3 MB (2283752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b1300c153bb28f7264cb101bb67f3eb4f78c7f1e032601890e6d80c56981f84`  
		Last Modified: Tue, 09 Sep 2025 05:28:34 GMT  
		Size: 21.3 KB (21276 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; 386

```console
$ docker pull fluentd@sha256:00c0ba7d40714f8a264e5c5e2fe9864ed612c6b64b313da61f7f615b62741ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76237114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0096cd93dfb8cff0d95f3b241fcd0b819f5d92490964f62433dd194484ef96b7`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bfb18ad48f85fd4ca43130c11b60c8dd156cb1815fd08233be2be9c36c6923`  
		Last Modified: Mon, 08 Sep 2025 21:42:44 GMT  
		Size: 1.3 MB (1285592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336ae728bed6a475a8811b8b0a9460889cb5e0b9c9882d24089f9b3f37ea0ec1`  
		Last Modified: Mon, 08 Sep 2025 21:42:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f33d4089ac39c16a1eb1172c1fd597771702897fc5472ebd4524ee51d009b1`  
		Last Modified: Mon, 08 Sep 2025 22:02:16 GMT  
		Size: 37.7 MB (37657047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1143329072f08996cee8c8782335612b6460d9af2d9c7b80994a10330d6565`  
		Last Modified: Mon, 08 Sep 2025 21:42:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012c9149010179ce2a7385b9f1d4bba0926ec1a8f760320ce1a18344605fdefb`  
		Last Modified: Mon, 08 Sep 2025 22:56:47 GMT  
		Size: 6.0 MB (6002305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ae9af9420adf087b905e7979604a6aa9bbc3a4ec10861d9343cf60105fd1f6`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec1b97fb2027b8b637569ad830d697f5bfbc90b8073821f7667ab74bf5a7ee9`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e572568dc6a854cf5d202e39d57adff848138401e921cd90b5517c03a03b56`  
		Last Modified: Mon, 08 Sep 2025 22:53:00 GMT  
		Size: 475.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:c520f8feb045dc07ca91f1b801a18b3da2b99164328f5cea9e3d4617671fd805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a43abcc28180d678dd6fb3f2c34449f867fddd6ced15eca284444f3bed3254e`

```dockerfile
```

-	Layers:
	-	`sha256:4fd46796ac747472faab066b28d336aeb770dcd930f6a4574e047894e2f9c4e1`  
		Last Modified: Mon, 08 Sep 2025 23:28:40 GMT  
		Size: 2.3 MB (2280668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e027c0378727a4242ff878c5bf5d33ab554280d64bc99f99f42aa0b4ec277e`  
		Last Modified: Mon, 08 Sep 2025 23:28:41 GMT  
		Size: 21.1 KB (21106 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; ppc64le

```console
$ docker pull fluentd@sha256:578c42ba1e6fe6d220e34f814a6907ef7f0a68570a200cff2dad7b5be01a0063
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80931845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554f74aaca5d4fb974f997565fce7312dc080508c46bcd65b969ad234174347d`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ce8600c6aabffbd80bd501b7ac3a736f18377ed3e07f94e2ee78a82b4e4f36`  
		Last Modified: Wed, 13 Aug 2025 17:10:49 GMT  
		Size: 1.3 MB (1307302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beeaeb3c6936a2d2eb3b798f796525e15863a84f94eeac482b026abcf5e81681`  
		Last Modified: Wed, 13 Aug 2025 17:10:48 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff53e1f7034343e8070d6221a1160a532a7e0c29de8bbc1705dc7c38bedbb24`  
		Last Modified: Wed, 13 Aug 2025 17:20:51 GMT  
		Size: 39.5 MB (39501405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c4abad74118dcd88bae1a1fab5137324bd11deded7bf240335b90943dcef30c`  
		Last Modified: Wed, 13 Aug 2025 17:20:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230e7efe3550ceb6d1b0edea559996448ddf4f137a78f786e726123946b0815c`  
		Last Modified: Thu, 14 Aug 2025 02:02:36 GMT  
		Size: 6.5 MB (6526530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d625b46b5e4f28fc6df5b2baa1399a290f56672bcc7d4558a66b3038c2232a33`  
		Last Modified: Thu, 14 Aug 2025 02:02:36 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711cdf0979bb42ee138c5cc2104ae40a16fc27e69d5ce3c47c4567168e8d15bc`  
		Last Modified: Thu, 14 Aug 2025 02:02:37 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af84d819228b1a405da1d867e01bf2775cafda73e14fd745cfa4323c8a4a1f1`  
		Last Modified: Thu, 14 Aug 2025 02:02:38 GMT  
		Size: 477.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:b73585cc3502a53d8faf8e455384d82b34e9c09bb912756fef13757893f63e0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aee2b306d1c9a5e7cd4cdcfd9e5171841a4efb08f14de805ddf09716943abb9`

```dockerfile
```

-	Layers:
	-	`sha256:2f6801a230c74e4b9aed5d3e1951eea3fefc7f11bb2333e136ede64cbf5eadd2`  
		Last Modified: Thu, 14 Aug 2025 02:28:32 GMT  
		Size: 2.3 MB (2286167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c3a3456832f73a97de5511ae14d2bb183385c903d0eb55970dec799fd33b44`  
		Last Modified: Thu, 14 Aug 2025 02:28:33 GMT  
		Size: 21.2 KB (21197 bytes)  
		MIME: application/vnd.in-toto+json

### `fluentd:v1.19.0-debian-1.0` - linux; s390x

```console
$ docker pull fluentd@sha256:282b140069685c91b06cc70bd403db8dfc2175bf2114ccee46fef0f863576d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76691999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa2256db132f298feed82e53e31f7ba4e9a4ec15e6e001a81501b09c007b01b`
-	Entrypoint: `["tini","--","\/bin\/entrypoint.sh"]`
-	Default Command: `["fluentd"]`

```dockerfile
# Thu, 31 Jul 2025 04:35:05 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 	; 	apt-get dist-clean # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
RUN set -eux; 	mkdir -p /usr/local/etc; 	echo 'gem: --no-document' >> /usr/local/etc/gemrc # buildkit
# Thu, 31 Jul 2025 04:35:05 GMT
ENV LANG=C.UTF-8
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_VERSION=3.4.5
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_URL=https://cache.ruby-lang.org/pub/ruby/3.4/ruby-3.4.5.tar.xz
# Thu, 31 Jul 2025 04:35:05 GMT
ENV RUBY_DOWNLOAD_SHA256=7b3a905b84b8777aa29f557bada695c3ce108390657e614d2cc9e2fb7e459536
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
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56be941f806d82f4bf75185b333c5c589812220338507cb5d56baeeee8c5965`  
		Last Modified: Wed, 13 Aug 2025 06:50:22 GMT  
		Size: 1.3 MB (1292014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc88df88585689c870b8cb13eccddc94febb777e8fb5f684a7ea31e4b5317929`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dbba3b8727d5a05350927ba0dae09b37c2f43cf7ae85bf1a5ce90e04f03ab75`  
		Last Modified: Wed, 13 Aug 2025 05:54:45 GMT  
		Size: 39.2 MB (39180168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca23cfe07c682626dbf88b68cf0822a38658eb00013c59f00bd48113d5788ecc`  
		Last Modified: Wed, 13 Aug 2025 05:54:43 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715644edf14c65a22fc17afc877e73e2481104398c62fc9f6612b110e99b19a2`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 6.4 MB (6384364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972751519e154187ceeadef8b4540fe82a0db5f10c3dfe19b879c762d3676ba9`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241a9530941b60d0de548b1cc1e87c8a4e1ad75c07e7f22d21aa4adcce58f039`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d257fbad7ece230f4d601fe80c948945f942f732c27de9e5b66474557be69d0a`  
		Last Modified: Wed, 13 Aug 2025 09:17:42 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `fluentd:v1.19.0-debian-1.0` - unknown; unknown

```console
$ docker pull fluentd@sha256:0e3124818a6163f62aa958c1bcdd89be51c6dceda624ad1ef20863b89ad31c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd5961f5539cf8ac1e04fa9048683b8d10d088bd24da21691b4d97caf254a36`

```dockerfile
```

-	Layers:
	-	`sha256:c7822c267d4e80f00ed3c7f2cdee4230a544030e32a353eef79105538eb19362`  
		Last Modified: Wed, 13 Aug 2025 11:28:35 GMT  
		Size: 2.3 MB (2284077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:929c64c079132a48ce0d1077d129e2a262a05d1d5c89af9da4583077965fd2bc`  
		Last Modified: Wed, 13 Aug 2025 11:28:36 GMT  
		Size: 21.1 KB (21145 bytes)  
		MIME: application/vnd.in-toto+json
